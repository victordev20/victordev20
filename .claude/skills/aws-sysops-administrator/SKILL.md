---
name: aws-sysops-administrator
description: "Guia AWS Certified SysOps Administrator Associate (Jon Bonso & Lervin John Obando): monitoramento, confiabilidade, deploy e automação, segurança, rede e custos do ponto de vista operacional. Use ao operar ambientes AWS no dia a dia, criar alarmes/automações ou estudar para SOA."
---

# AWS SysOps Administrator Associate — Jon Bonso & Lervin John Obando

Livro-fonte: `LivrosDev/AWS Certified SysOps Administrator Associate Version 2 - Autor (Jon Bonso and Lervin John Obando).pdf`

## Domínios
1. **Monitoramento, logging e remediação** — CloudWatch (métricas padrão vs customizadas, agente unificado para memória/disco, alarmes compostos, dashboards), CloudWatch Logs + metric filters, EventBridge, Config + remediação SSM, Health Dashboard.
2. **Confiabilidade e continuidade** — Auto Scaling (políticas target tracking/step/scheduled), ELB health checks, Multi-AZ RDS, read replicas, AWS Backup, snapshots EBS/RDS, S3 versionamento/replicação.
3. **Deploy, provisionamento e automação** — CloudFormation (troubleshooting de falhas de stack, rollback), AMIs e EC2 Image Builder, SSM (Run Command, Patch Manager, State Manager, Automation, Session Manager), OpsWorks, Elastic Beanstalk.
4. **Segurança e conformidade** — IAM, políticas, MFA, KMS, ACM, Trusted Advisor, Inspector, Security Hub, CloudTrail.
5. **Rede e entrega de conteúdo** — VPC, subnets, route tables, NAT gateway, SG/NACL, VPC Flow Logs para troubleshooting, Route 53 (registros, health checks, políticas), CloudFront.
6. **Custo e performance** — Cost Explorer, Budgets, tags de alocação, Compute Optimizer, tipos de EBS, placement groups.

## Troubleshooting rápido
- Instância inacessível: SG, NACL, rota, IP público/IGW, status checks (system vs instance).
- Alarme sem dados de memória: instale o agente CloudWatch.
- Stack falhou: veja eventos do CloudFormation; `DELETE_FAILED` costuma ser recurso não vazio.
- 503 no ALB: sem targets saudáveis.
