---
name: aws-devops-engineer-professional-book
description: "AWS Certified DevOps Engineer Professional — Certification and Beyond (Adam Book): Well-Architected, IaC com CloudFormation/CDK, CI/CD com CodePipeline/CodeBuild/CodeDeploy, estratégias de deploy, monitoramento, logging, resposta a incidentes e alta disponibilidade. Use ao projetar pipelines DevOps na AWS ou estudar para DOP."
---

# AWS DevOps Engineer Professional — Adam Book

Livro-fonte: `LivrosDev/AWS Certified DevOps Engineer - Professional Certification and Beyond - Autor (Adam Book).pdf`

## Fundamentos
- **Well-Architected Framework:** excelência operacional (operações como código, mudanças pequenas e reversíveis, aprender com falhas), segurança (rastreabilidade, segurança em todas as camadas, proteger dados em trânsito/repouso), confiabilidade (recuperação automática, escalar horizontalmente, parar de adivinhar capacidade), eficiência de performance (serverless, experimentar), otimização de custos (modelo de consumo, medir eficiência).
- Bancos: relacionais, chave-valor, documentos, grafos — escolha pela forma do acesso.

## Infraestrutura como código
- **CloudFormation:** templates, parâmetros, outputs, nested stacks, StackSets (multi-conta/região), change sets, drift detection, políticas de stack.
- **CDK** para IaC com linguagens de programação.
- **Elastic Beanstalk** e **OpsWorks** (configuração) para PaaS.

## CI/CD
- **CodeCommit → CodeBuild (buildspec) → CodeDeploy (appspec, hooks de ciclo de vida) → CodePipeline.**
- Artefatos em S3; aprovações manuais; testes automatizados em estágios.
- **Estratégias de deploy:** all-at-once, rolling, rolling with batch, immutable, blue/green, canary, linear; Lambda aliases com traffic shifting.

## Operação
- **CloudWatch** (métricas, logs, alarmes, dashboards, Logs Insights), **X-Ray** (tracing), **EventBridge** para automação, **Systems Manager** (Run Command, Patch Manager, Parameter Store, Automation).
- **Auto Scaling**, lifecycle hooks, multi-AZ/multi-região, Route 53 failover.
- Segurança: IAM, Secrets Manager, KMS, Config rules com remediação, GuardDuty, Security Hub.

## Como aplicar ao projetar um pipeline
1. Tudo versionado (app + infra).
2. Build reprodutível com testes unitários e de integração.
3. Deploy progressivo (canary/blue-green) com rollback automático por alarme.
4. Observabilidade antes do primeiro deploy.
5. Runbooks automatizados via SSM/EventBridge.
