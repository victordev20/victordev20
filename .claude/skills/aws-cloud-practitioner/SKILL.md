---
name: aws-cloud-practitioner
description: "Guia de estudo AWS Certified Cloud Practitioner (Jon Bonso & Adrian Formaran, Tutorials Dojo): conceitos de nuvem, serviços essenciais, segurança, preços e suporte. Use para estudar a certificação CLF, explicar fundamentos da AWS ou responder questões de exame no estilo cenário."
---

# AWS Certified Cloud Practitioner — Jon Bonso & Adrian Formaran

Livro-fonte: `LivrosDev/AWS Certified Cloud Practitioner Exam - Autor (Jon Bonso and Adrian Formaran).pdf`

## Domínios do exame
1. **Conceitos de nuvem** — vantagens (trocar CAPEX por OPEX, economia de escala, parar de adivinhar capacidade, velocidade/agilidade, global em minutos); modelos IaaS/PaaS/SaaS; implantação pública/híbrida/on-premises; Well-Architected (6 pilares).
2. **Segurança e conformidade** — **Modelo de Responsabilidade Compartilhada** (AWS: segurança *da* nuvem; cliente: segurança *na* nuvem); IAM (usuários, grupos, papéis, políticas, MFA, menor privilégio); Shield, WAF, GuardDuty, Inspector, Macie, KMS, CloudTrail, Config, Artifact.
3. **Tecnologia** — infraestrutura global (Regiões, AZs, Edge Locations); EC2, Lambda, ECS/EKS/Fargate, Elastic Beanstalk; S3 (classes), EBS, EFS, Glacier; RDS, Aurora, DynamoDB, Redshift; VPC, Route 53, CloudFront, Direct Connect, VPN; CloudWatch, SNS, SQS.
4. **Cobrança e preços** — On-Demand, Reserved, Savings Plans, Spot, Dedicated; Free Tier; Pricing Calculator, Cost Explorer, Budgets, Cost & Usage Report; Organizations e faturamento consolidado; planos de suporte (Basic, Developer, Business, Enterprise On-Ramp, Enterprise) e Trusted Advisor.

## Estratégia para responder questões
1. Identifique a palavra-chave do cenário (mais barato, mais disponível, menos operação, gerenciado).
2. Elimine respostas que exigem gestão manual quando há serviço gerenciado.
3. Em segurança, lembre quem é responsável pelo quê.
4. Em custos, mapeie padrão de uso → modelo de compra (estável = Reserved/Savings Plans; tolerante a interrupção = Spot).

## Dicas de estudo
- Use as "cheat sheets" de cada serviço e faça simulados até >80% de forma consistente.
- Revise o whitepaper "Overview of Amazon Web Services" e o Well-Architected Framework.
