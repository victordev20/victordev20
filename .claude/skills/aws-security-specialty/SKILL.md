---
name: aws-security-specialty
description: "Guia AWS Certified Security Specialty (Jon Bonso & Carlo Acebedo): resposta a incidentes, logging e monitoramento, segurança de infraestrutura, IAM, proteção de dados e governança. Use ao endurecer contas AWS, investigar incidentes ou estudar para SCS."
---

# AWS Certified Security Specialty — Jon Bonso & Carlo Acebedo

Livro-fonte: `LivrosDev/AWS Certified Security Specialty Exam - Autor (Jon Bonso and Carlo Acebedo).pdf`

## Domínios
1. **Resposta a incidentes** — AWS Config rules com remediação automática; Trusted Advisor; **chave de acesso exposta**: desative/rotacione, revise CloudTrail, avalie impacto; GuardDuty (achados → EventBridge → Lambda); Inspector; SSM Patch Manager; EC2 com chave SSH comprometida (isolar via SG, snapshot para forense, substituir); Artifact para relatórios de conformidade; AWS Abuse.
2. **Logging e monitoramento** — CloudTrail (multi-região, validação de integridade do log, organização), CloudWatch Logs/alarmes/metric filters, VPC Flow Logs, logs de ELB/CloudFront/S3, Athena para consulta, Security Hub, Detective.
3. **Segurança de infraestrutura** — VPC (SGs stateful vs NACLs stateless), endpoints (gateway/interface), WAF, Shield/Advanced, CloudFront com OAC/OAI, Network Firewall, bastion vs Session Manager.
4. **Identidade e acesso** — políticas IAM (avaliação: deny explícito > allow), permission boundaries, SCPs, políticas de recurso, STS/AssumeRole, federação SAML/OIDC, IAM Identity Center, Cognito, condições (`aws:SourceIp`, `aws:PrincipalOrgID`, MFA).
5. **Proteção de dados** — KMS (CMKs, key policies, grants, rotação, envelope encryption), CloudHSM, criptografia S3 (SSE-S3, SSE-KMS, SSE-C, client-side), ACM, Secrets Manager, Macie.
6. **Governança** — Organizations, Control Tower, Config conformance packs, tagging.

## Playbook genérico de incidente
1. Conter (isolar recurso, revogar credenciais).
2. Preservar evidências (snapshots, logs).
3. Investigar (CloudTrail, Flow Logs, Detective).
4. Erradicar e recuperar.
5. Automatizar a detecção para a próxima vez.
