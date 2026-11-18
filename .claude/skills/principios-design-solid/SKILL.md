---
name: principios-design-solid
description: "Princípios de Design e Padrões de Projeto (Robert C. Martin, 'Design Principles and Design Patterns'): sintomas de design podre (rigidez, fragilidade, imobilidade, viscosidade), gestão de dependências, princípios de classes (OCP, LSP, DIP, ISP), princípios de pacotes (REP, CCP, CRP, ADP, SDP, SAP) e padrões de arquitetura OO (Abstract Server, Adapter, Observer, Bridge, Abstract Factory). Use ao avaliar dependências e acoplamento de um design."
---

# Princípios de Design e Padrões de Projeto — Robert C. Martin

Livro-fonte: `LivrosDev/Princípios de Design e Padrões de Projeto - Autor (Robert C. Martin).pdf`

## Sintomas de design podre
- **Rigidez:** difícil mudar (efeito cascata).
- **Fragilidade:** quebra em lugares inesperados.
- **Imobilidade:** difícil reutilizar.
- **Viscosidade:** mais fácil fazer o errado (hack) do que o certo.
Causa principal: **mudanças de requisitos** atingindo **dependências mal gerenciadas**.

## Princípios de classes
- **OCP (Aberto/Fechado):** aberto para extensão, fechado para modificação — via abstração e polimorfismo.
- **LSP (Substituição de Liskov):** subclasses devem ser substituíveis pelas bases (ex.: Círculo/Elipse, Quadrado/Retângulo violam).
- **DIP (Inversão de Dependência):** dependa de abstrações, não de concreções.
- **ISP (Segregação de Interfaces):** muitas interfaces específicas são melhores que uma geral.

## Princípios de pacotes
- Coesão: **REP** (granularidade de reuso = granularidade de release), **CCP** (classes que mudam juntas ficam juntas), **CRP** (classes não reutilizadas juntas não devem ficar juntas).
- Acoplamento: **ADP** (sem ciclos no grafo de dependências — quebre com DIP ou novo pacote), **SDP** (dependa na direção da estabilidade), **SAP** (pacotes estáveis devem ser abstratos).
- Métricas: Instabilidade `I = Ce/(Ca+Ce)`, Abstração `A = abstratas/total`, distância `D = |A + I − 1|`.

## Padrões de arquitetura OO
- **Abstract Server** (cliente depende de interface — DIP), **Adapter** (quando não dá para alterar o servidor), **Observer**, **Bridge**, **Abstract Factory** (centraliza criação de concretos).

## Uso em revisão
1. Desenhe o grafo de dependências de pacotes; procure ciclos.
2. Calcule I e A dos pacotes centrais; pacotes muito estáveis e concretos são dolorosos de mudar.
3. Procure `instanceof`/downcasts (sinal de violação de LSP/OCP).
