---
name: azure-cloud
description: "Azure — Coloque suas plataformas e serviços no cloud (Casa do Código): IaaS/PaaS/SaaS, Azure WebApps (deploy, escala vertical/horizontal, slots, SSL), máquinas virtuais, armazenamento, SQL Database, filas e serviços. Use ao hospedar e escalar aplicações no Microsoft Azure."
---

# Azure — Casa do Código

Livro-fonte: `LivrosDev/Azure - Coloque suas plataformas e serviços no cloud - Autor (Casa do Código).pdf`

## Conceitos
- Computação em nuvem: tipos (pública, privada, híbrida), **IaaS, PaaS, SaaS**, quando usar.
- Azure: computação, armazenamento, serviços integrados, diferenciais (integração com ecossistema Microsoft, híbrido).

## Azure App Service (WebApps)
1. Criar WebApp no portal; publicar via Visual Studio (perfil de publicação) ou Git/GitHub (deploy contínuo).
2. **Escalar verticalmente** (plano maior) ou **horizontalmente** (mais instâncias, autoscale por métricas).
3. **Slots de implantação** (staging → swap para produção sem downtime).
4. Monitoramento e diagnóstico de logs; WebApps da galeria; **domínio customizado + SSL**.

## Outros serviços abordados
- **Máquinas virtuais** (IaaS) quando precisa de controle do SO.
- **Storage:** Blobs, Tables, Queues, Files.
- **Azure SQL Database** (PaaS relacional) e alternativas NoSQL.
- Serviços de mensageria/filas para desacoplar.

## Boas práticas
- Prefira PaaS (App Service, SQL Database) para reduzir operação.
- Use slots + swap para deploys seguros e rollback rápido.
- Configurações e connection strings no App Settings, não no código.
- Defina alertas e autoscale com limites para controlar custos.
