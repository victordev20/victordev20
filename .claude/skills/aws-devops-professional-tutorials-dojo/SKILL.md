---
name: aws-devops-professional-tutorials-dojo
description: "Guia de estudo AWS Certified DevOps Engineer Professional (Jon Bonso & Kenneth Samonte, Tutorials Dojo): domínios do exame, cenários comuns de CI/CD, blue/green, CodeDeploy hooks, monitoramento, governança e alta disponibilidade. Use para estudar DOP-C0x ou resolver cenários de automação na AWS."
---

# AWS DevOps Professional — Jon Bonso & Kenneth Samonte

Livro-fonte: `LivrosDev/AWS Certified DevOps Professional Engineer - Autor (Jon Bonso and Kenneth Samonte).pdf`

## Domínios
1. **Automação do SDLC** — CodeCommit (políticas AWSCodeCommitFullAccess/PowerUser/ReadOnly), CodeBuild (testes automáticos após PR, artefatos, logs e métricas no CloudWatch), CodeDeploy (hooks: ApplicationStop, BeforeInstall, AfterInstall, ApplicationStart, ValidateService; para ECS/Lambda: BeforeAllowTraffic/AfterAllowTraffic), CodePipeline.
2. **Configuração e IaC** — CloudFormation (cfn-init, cfn-signal, WaitCondition, CreationPolicy, UpdatePolicy, DeletionPolicy, custom resources), Elastic Beanstalk (.ebextensions, swap de URL), OpsWorks, Systems Manager.
3. **Monitoramento e logging** — CloudWatch Logs/métricas/alarmes, subscription filters → Kinesis/Lambda, CloudTrail, X-Ray.
4. **Políticas e padrões** — Organizations, SCPs, Config, Service Catalog, Trusted Advisor, tagging.
5. **Resposta a incidentes e eventos** — EventBridge + Lambda/SSM Automation, Auto Scaling lifecycle hooks, Health.
6. **Alta disponibilidade, tolerância a falhas e DR** — multi-AZ, réplicas, Route 53 health checks/failover, backups, RTO/RPO (backup & restore, pilot light, warm standby, multi-site).

## Padrões de blue/green citados
- Troca via **ELB**, **Route 53** (weighted), **Elastic Beanstalk** (swap CNAME), **stack clonada no OpsWorks**, **aliases do Lambda** com traffic shifting, **ECS** com CodeDeploy.

## Estratégia de prova
- Procure a solução **mais automatizada e com menor overhead operacional**.
- "Menor tempo de inatividade" → blue/green ou immutable.
- "Reverter automaticamente" → CodeDeploy com alarmes do CloudWatch.
- "Auditar mudanças de configuração" → AWS Config; "quem fez a chamada de API" → CloudTrail.
