---
name: aws-solutions-architect-professional
description: "Guia AWS Certified Solutions Architect Professional (Jon Bonso & Adrian Formaran): complexidade organizacional, multi-conta, rede híbrida, migração, modernização, DR e otimização de custos em larga escala. Use para arquiteturas AWS corporativas complexas ou estudar para SAP."
---

# AWS Solutions Architect Professional — Jon Bonso & Adrian Formaran

Livro-fonte: `LivrosDev/AWS Certified Solutions Architect Professional - Autor (Jon Bonso and Adrian Formaran).pdf`

## Domínios
1. **Complexidade organizacional** — AWS Organizations, OUs, SCPs, Control Tower/Landing Zone, IAM Identity Center, compartilhamento com RAM, faturamento consolidado, contas por ambiente/carga.
2. **Rede híbrida e multi-VPC** — Transit Gateway, VPC peering, PrivateLink, Direct Connect (+ VPN de backup, DX Gateway, LAG), Site-to-Site VPN, Route 53 Resolver (endpoints inbound/outbound), IPv6.
3. **Novas soluções** — requisitos de segurança, confiabilidade, performance e custo; event-driven (EventBridge, SNS/SQS, Step Functions), containers (ECS/EKS), dados (Aurora Global, DynamoDB Global Tables, Redshift, Lake Formation).
4. **Melhoria contínua** — observabilidade, automação, rightsizing, SSM, Config.
5. **Migração e modernização** — 7 Rs (retire, retain, rehost, relocate, replatform, repurchase, refactor), Migration Hub, Application Discovery Service, MGN, DMS + SCT, DataSync, Snow Family, Storage Gateway.

## Padrões recorrentes
- **DR:** escolha por RTO/RPO e custo: backup/restore < pilot light < warm standby < multi-site active/active.
- **Multi-região:** Route 53 (latency/failover), Aurora Global Database, S3 CRR, DynamoDB Global Tables.
- **Transferência massiva:** volume e prazo → Snowball/Snowmobile vs DX vs DataSync.
- **Governança de custo:** tags obrigatórias, Budgets, Savings Plans compartilhados na organização.

## Método
1. Leia o cenário inteiro; ele costuma ter 3–4 restrições escondidas.
2. Identifique o critério dominante (mais barato, mais rápido de migrar, menor esforço operacional).
3. Desconfie de respostas que funcionam mas violam uma restrição sutil (ex.: tráfego pela internet pública).
