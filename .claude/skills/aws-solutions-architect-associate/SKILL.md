---
name: aws-solutions-architect-associate
description: "Guia AWS Certified Solutions Architect Associate SAA-C03 (Jon Bonso, Tutorials Dojo): arquiteturas seguras, resilientes, de alta performance e custo-otimizadas. Use ao desenhar soluções na AWS, comparar serviços (S3/EBS/EFS, RDS/Aurora/DynamoDB, SQS/SNS/Kinesis) ou estudar para SAA."
---

# AWS Solutions Architect Associate (SAA-C03) — Jon Bonso

Livro-fonte: `LivrosDev/AWS Certified Solutions Architect Associate SAA-C03 - Autor (Jon Bonso).pdf`

## Domínios
1. **Arquiteturas seguras (30%)** — IAM, SCPs, KMS, Secrets Manager, VPC (subnets públicas/privadas, NAT, SG vs NACL, endpoints), WAF/Shield, Cognito.
2. **Arquiteturas resilientes (26%)** — multi-AZ, Auto Scaling, ELB (ALB/NLB/GWLB), SQS para desacoplar, Route 53 (políticas de roteamento), DR (backup/restore, pilot light, warm standby, active-active).
3. **Arquiteturas de alta performance (24%)** — escolha de armazenamento (S3, EBS gp3/io2, EFS, FSx), cache (CloudFront, ElastiCache, DAX), bancos (RDS + read replicas, Aurora, DynamoDB), streaming (Kinesis), compute (EC2, Lambda, Fargate).
4. **Arquiteturas custo-otimizadas (20%)** — modelos de compra, classes S3 e lifecycle, rightsizing, serverless, transferência de dados.

## Tabelas mentais de decisão
| Necessidade | Escolha típica |
|---|---|
| Arquivos compartilhados Linux | EFS |
| Arquivos Windows/SMB | FSx for Windows |
| HPC | FSx for Lustre |
| Armazenamento de objetos com acesso raro | S3 Standard-IA / Glacier |
| Chave-valor ms em escala | DynamoDB |
| SQL com HA gerenciada | RDS Multi-AZ / Aurora |
| Desacoplar produtor/consumidor | SQS |
| Fan-out de mensagens | SNS (+SQS) |
| Streaming em tempo real | Kinesis Data Streams |
| Conteúdo estático global | S3 + CloudFront |

## Método para responder
1. Sublinhe requisitos (custo, latência, HA, operação mínima).
2. Elimine alternativas que não atendem a um requisito obrigatório.
3. Entre as restantes, prefira **gerenciado** e **menos componentes**.
