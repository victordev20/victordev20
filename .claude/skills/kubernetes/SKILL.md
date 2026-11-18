---
name: kubernetes
description: "Kubernetes — Tudo sobre orquestração de contêineres (Lucas Santos, Casa do Código): monólitos vs microsserviços, arquitetura do cluster (master/control plane, nodes), kubectl, Pods, ReplicaSets, Deployments, Services, volumes, ConfigMaps e Secrets, namespaces, clusters gerenciados no GCP (GKE) e Azure (AKS), escalabilidade, health checks e boas práticas. Use ao implantar ou depurar aplicações em Kubernetes."
---

# Kubernetes — Lucas Santos (Casa do Código)

Livro-fonte: `LivrosDev/Kubernetes - Tudo sobre orquestração de contêineres - Autor (Casa do Código).pdf`

## Conceitos
- **Monólitos** quebram ao escalar times e cargas → contêineres → **microsserviços** → necessidade de **orquestração**.
- **Cluster:** **control plane/master** (API Server, etcd, Scheduler, Controller Manager) + **nodes** (kubelet, kube-proxy, runtime).

## Mãos à obra
- Ambiente local (minikube/kind), **kubectl** (`get`, `describe`, `apply -f`, `logs`, `exec`, `port-forward`, `delete`).
- Clusters na nuvem: **GKE** (Google Cloud) e **AKS** (Azure) com SDK/CLI.

## Recursos
- **Pod:** menor unidade; um ou mais contêineres que compartilham rede/volume.
- **ReplicaSet** e **Deployment** (rolling update, rollback com `kubectl rollout undo`).
- **Service:** ClusterIP, NodePort, LoadBalancer; **Ingress** para HTTP.
- **Volumes**, PersistentVolume/PersistentVolumeClaim, StatefulSet para estado.
- **ConfigMaps** e **Secrets** para configuração.
- **Namespaces**, labels e selectors.
- **Probes:** liveness e readiness; **requests/limits**; **HorizontalPodAutoscaler**.

## Checklist de manifesto
- [ ] Imagem com tag imutável
- [ ] `resources.requests/limits` definidos
- [ ] readiness e liveness probes
- [ ] Config em ConfigMap/Secret, não na imagem
- [ ] ≥ 2 réplicas e PodDisruptionBudget para serviços críticos
- [ ] Labels consistentes (app, versão, ambiente)
