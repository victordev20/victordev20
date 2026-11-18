---
name: ddd-referencia
description: "Domain-Driven Design Referência — Sumário de padrões e definições (Eric Evans): catálogo oficial dos padrões de DDD — modelo em ação, blocos de construção (inclui eventos de domínio), design flexível, mapeamento de contextos, destilação e estrutura em larga escala. Use como glossário/consulta rápida ao aplicar padrões táticos ou estratégicos de DDD."
---

# Domain-Driven Design Referência — Eric Evans

Livro-fonte: `LivrosDev/Domain-Driven Design Referência - Sumário de Padrões e Definições - Autor (Eric Evans).pdf`

## 1. Colocando o modelo em ação
Contexto Delimitado · Linguagem Onipresente · Integração Contínua · Design Dirigido por Modelos · Modeladores Envolvidos (hands-on) · Refatorando para uma Visão Mais Profunda.

## 2. Blocos de construção
Arquitetura em Camadas · Entidades · Objetos de Valor · **Eventos de Domínio** (algo que aconteceu e importa para especialistas; imutáveis, com timestamp) · Serviços · Módulos · Agregados · Repositórios · Fábricas.

## 3. Design flexível
Interfaces Reveladoras de Intenção · Funções Livres de Efeitos Colaterais · Asserções (pós-condições e invariantes) · Classes Autônomas · Fechamento de Operações (tipo de retorno = tipo do argumento) · Design Declarativo · Basear-se em Formalismos Estabelecidos · Contornos Conceituais.

## 4. Mapeamento de contextos (estratégico)
Mapa de Contextos · Parceria · Kernel Compartilhado · Desenvolvimento Cliente/Fornecedor · Conformista · Camada Anticorrupção · Serviço de Host Aberto · Linguagem Publicada · Caminhos Separados · Grande Bola de Lama.

## 5. Destilação
Domínio Principal · Subdomínios Genéricos · Declaração da Visão do Domínio · Núcleo Destacado · Mecanismos Coesos · Núcleo Segregado · Núcleo Abstrato.

## 6. Estrutura em larga escala
Ordem em Evolução · Metáfora do Sistema · Camadas de Responsabilidade · Nível de Conhecimento · Framework de Componentes Plugáveis.

## Uso como consulta
Para cada decisão de modelagem, identifique o padrão, leia sua definição ("Portanto, ...") e verifique se o código cumpre as consequências. Ao integrar sistemas, classifique cada relação no mapa de contextos antes de escolher a técnica.
