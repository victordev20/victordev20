---
name: aws-developer-associate
description: "Guia AWS Certified Developer Associate (Jon Bonso & Adrian Formaran): desenvolvimento serverless, SDK/CLI, DynamoDB, S3, Lambda, API Gateway, SQS/SNS, Cognito, CI/CD, segurança e troubleshooting. Use ao programar aplicações na AWS ou estudar a certificação DVA."
---

# AWS Certified Developer Associate — Jon Bonso & Adrian Formaran

Livro-fonte: `LivrosDev/AWS Certified Developer Associate Exam - Autor (Jon Bonso and Adrian Formaran).pdf`

## Domínios
1. **Desenvolvimento com serviços AWS** — Lambda (concorrência, camadas, variáveis de ambiente, destinos, versões/aliases, cold start), API Gateway (estágios, autorizadores, throttling, cache), DynamoDB (chave de partição/ordenação, LSI/GSI, RCU/WCU, Query vs Scan, atributos projetados, Streams, DAX, TTL, transações, escrita condicional), S3 (presigned URLs, eventos, criptografia), SQS (standard vs FIFO, visibility timeout, long polling, DLQ), SNS, Step Functions, Kinesis.
2. **Segurança** — IAM roles para serviços, Cognito (User Pools vs Identity Pools), KMS (envelope encryption, GenerateDataKey), Secrets Manager vs Parameter Store, STS.
3. **Implantação** — Elastic Beanstalk (estratégias de deploy), SAM (`sam build/deploy`, transform), CloudFormation, CodeCommit/Build/Deploy/Pipeline, ECS/ECR.
4. **Troubleshooting e otimização** — CloudWatch (métricas customizadas, logs, Embedded Metric Format), X-Ray (segmentos, subsegmentos, anotações vs metadados), retries com **backoff exponencial**, caching (ElastiCache: lazy loading vs write-through).

## Regras práticas
- Credenciais: **nunca** no código; use papéis IAM.
- DynamoDB: projete pelos padrões de acesso; evite Scan; use GSI para consultas alternativas.
- Erros 429/ThrottlingException → backoff exponencial com jitter.
- Payload grande para SQS → S3 + ponteiro.
- Segredo com rotação automática → Secrets Manager.

## Cálculo de capacidade DynamoDB (cai muito)
- 1 RCU = 1 leitura fortemente consistente/s de até 4 KB (ou 2 eventualmente consistentes).
- 1 WCU = 1 escrita/s de até 1 KB.
