---
name: aws-for-beginners
description: "Fundamentos da AWS para iniciantes (Steve M. Burnett): o que é nuvem, conta e console, serviços básicos de computação, armazenamento, banco, rede e segurança. Use para explicar AWS a quem está começando ou montar um primeiro ambiente simples."
---

# AWS For Beginners — Steve M. Burnett

Livro-fonte: `LivrosDev/AWS For Beginners - The ultimate guide to the fundamentals of aws - Autor (Steve M Burnett).pdf`

## Conteúdo essencial
- **Por que nuvem:** pague pelo uso, elasticidade, alcance global, menos infraestrutura física para manter.
- **Primeiros passos:** criar conta, proteger o usuário root (MFA, não usar no dia a dia), criar usuários IAM, configurar alertas de faturamento.
- **Serviços básicos:**
  - Computação: **EC2** (tipos de instância, AMIs, key pairs, security groups), **Lambda**.
  - Armazenamento: **S3** (buckets, objetos, permissões), **EBS**.
  - Banco: **RDS**, **DynamoDB**.
  - Rede: **VPC**, **Route 53** (DNS), **CloudFront** (CDN).
  - Gestão: **CloudWatch**, **IAM**.

## Roteiro para um primeiro projeto
1. Conta + MFA + alerta de orçamento.
2. Usuário IAM com permissões mínimas.
3. Site estático no S3 (+ CloudFront).
4. Uma instância EC2 t-família com SG liberando só as portas necessárias.
5. Monitorar custos e desligar o que não usa.

## Erros comuns de iniciante
- Usar root para tudo; chaves de acesso no código.
- Bucket S3 público sem querer.
- Esquecer recursos ligados e receber cobrança.
- Abrir SSH (22) para 0.0.0.0/0.
