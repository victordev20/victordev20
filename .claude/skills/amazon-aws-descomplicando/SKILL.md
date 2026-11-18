---
name: amazon-aws-descomplicando
description: "Amazon AWS — Descomplicando a computação na nuvem (Jonathan Lamim, Casa do Código): tutorial prático de S3, EC2 (Apache, PHP, MySQL), RDS, ElastiCache, Route 53, CloudFront, SES, SNS e CloudWatch. Use para configurar passo a passo uma aplicação web tradicional na AWS."
---

# Amazon AWS — Descomplicando a Computação na Nuvem (Casa do Código)

Livro-fonte: `LivrosDev/Amazon AWS - Descomplicando a computação na nuvem - Autor (Casa do Código).pdf`

## Roteiro do livro (mão na massa)
1. **Introdução:** regiões e zonas de disponibilidade, vantagens, Free Tier, console.
2. **S3:** buckets, objetos, pastas, upload, logs de acesso, permissões, site estático, versionamento e lifecycle.
3. **EC2:** criar instância, key pair, security group, Elastic IP; instalar **Apache, PHP e MySQL**; acessar via SSH; snapshots/AMIs.
4. **RDS:** banco gerenciado, backups automáticos, Multi-AZ, conexão a partir do EC2.
5. **ElastiCache:** cache (Memcached/Redis) para aliviar o banco.
6. **Route 53:** zona hospedada, registros A/CNAME/MX, apontar domínio.
7. **CloudFront:** CDN na frente do S3/EC2.
8. **SES:** envio de e-mails transacionais (verificação de domínio, sair do sandbox).
9. **SNS:** notificações (tópicos, assinaturas).
10. **CloudWatch:** métricas, alarmes e notificações.

## Arquitetura de referência resultante
```
Usuário → Route 53 → CloudFront → EC2 (Apache/PHP) → RDS
                         ↘ S3 (estáticos)      ↘ ElastiCache
CloudWatch alarmes → SNS → e-mail/SMS     SES → e-mails da app
```

## Boas práticas reforçadas
- Separe estáticos (S3/CloudFront) de dinâmico (EC2).
- Banco fora da instância de aplicação (RDS).
- Security groups mínimos; RDS acessível só pelo SG da aplicação.
- Alarmes de CPU, status check e faturamento desde o primeiro dia.
