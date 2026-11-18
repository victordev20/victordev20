---
name: ddd-rapido
description: "Domain-Driven Design Rapidamente (InfoQ, resumo de Eric Evans): linguagem ubíqua, design dirigido pelo modelo, arquitetura em camadas, entidades, objetos de valor, serviços, módulos, agregados, fábricas, repositórios, refatoração rumo a insight profundo e preservação da integridade (contexto delimitado, mapa de contextos, kernel compartilhado, cliente-fornecedor, conformista, camada anticorrupção, caminhos separados, serviço aberto, destilação). Use para aplicar DDD de forma introdutória."
---

# Domain-Driven Design Rapidamente

Livro-fonte: `LivrosDev/Domain Driven Design Rapido - Autor (Eric Evans).pdf`

## Conhecimento do domínio
- Desenvolvedores e especialistas de domínio constroem juntos um **modelo**.
- **Linguagem ubíqua:** a mesma linguagem nas conversas, diagramas e código. Se o nome muda na conversa, muda no código.

## Design dirigido pelo modelo
- O código reflete o modelo; **arquitetura em camadas** (UI, aplicação, domínio, infraestrutura) isolando o domínio.
- Blocos de construção:
  - **Entidades** (identidade contínua), **Objetos de valor** (imutáveis, definidos por atributos), **Serviços** (operações sem lugar natural em objetos, sem estado).
  - **Módulos** (alta coesão, nomes da linguagem ubíqua).
  - **Agregados** (raiz garante invariantes; referências externas só à raiz).
  - **Fábricas** (criação complexa), **Repositórios** (acesso a agregados como coleção).

## Refatorando rumo a insight profundo
- Refatoração contínua; torne **conceitos implícitos explícitos** (restrições, processos, especificações).

## Preservando a integridade do modelo
- **Contexto delimitado:** um modelo vale dentro de um limite explícito.
- **Integração contínua** dentro do contexto; **Mapa de contextos** entre eles.
- Padrões de relação: **Kernel Compartilhado**, **Cliente-Fornecedor**, **Conformista**, **Camada Anticorrupção**, **Caminhos Separados**, **Serviço de Host Aberto** (+ Linguagem Publicada).
- **Destilação:** identifique o **domínio principal (core)** e separe subdomínios genéricos.

## Como aplicar
1. Monte um glossário da linguagem ubíqua com especialistas.
2. Desenhe o mapa de contextos atual.
3. Modele agregados pequenos com invariantes explícitas.
4. Proteja o core com camada anticorrupção nas integrações.
