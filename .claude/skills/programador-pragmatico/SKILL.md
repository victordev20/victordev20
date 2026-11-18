---
name: programador-pragmatico
description: "O Programador Pragmático (Andrew Hunt & David Thomas): filosofia (responsabilidade, entropia/janelas quebradas, software satisfatório, carteira de conhecimento, comunicação), DRY, ortogonalidade, reversibilidade, projéteis luminosos, protótipos, linguagens de domínio, estimativas, ferramentas (texto simples, shell, controle de versão, depuração), paranoia pragmática (design by contract, programas que falham cedo, asserções), desacoplamento (Demeter), refatoração, testes e projetos pragmáticos. Use como guia geral de boas práticas e de decisões técnicas."
---

# O Programador Pragmático — Andrew Hunt & David Thomas

Livro-fonte: `LivrosDev/O Programador Pragmático - Autor (Andrew Hunt e David Thomas).pdf`

## 1. Filosofia pragmática
- **O gato comeu meu código-fonte:** assuma responsabilidade; ofereça opções, não desculpas.
- **Entropia de software:** não tolere janelas quebradas.
- **Sopa de pedras e sapos cozidos:** catalise mudanças; observe o quadro geral.
- **Software satisfatório:** envolva usuários no trade-off de qualidade; saiba quando parar.
- **Carteira de conhecimento:** invista regularmente, diversifique (uma linguagem nova por ano, um livro técnico por trimestre).
- **Comunique-se:** saiba o que quer dizer, conheça o público, escolha o momento.

## 2. Abordagem pragmática
- **DRY:** cada conhecimento com uma representação única e autoritativa.
- **Ortogonalidade:** elimine efeitos entre coisas não relacionadas.
- **Reversibilidade:** não há decisões finais.
- **Projéteis luminosos (tracer bullets):** esqueleto ponta a ponta funcionando cedo.
- **Protótipos e notas post-it:** para aprender, descartáveis.
- **Linguagens de domínio**; **estimativas** (unidades certas, aprenda com o histórico).

## 3. Ferramentas básicas
Texto simples · jogos de shell · edição avançada (domine um editor) · **controle de versão sempre** · **depuração** (corrija o problema, não a culpa; "select não está quebrado"; rubber duck) · manipulação de texto · geradores de código.

## 4. Paranoia pragmática
Você não consegue escrever software perfeito → **design by contract**; **programas mortos não mentem** (falhe cedo); **programação assertiva**; exceções para o excepcional; **termine o que começou** (recursos).

## 5. Dobre ou quebre
**Desacoplamento e Lei de Demeter**; metaprogramação (configure, não integre); acoplamento temporal; separe visões de modelos (MVC, publish/subscribe); quadros-negros.

## 6. Enquanto você codifica
Não programe por coincidência · velocidade do algoritmo (Big O) · **refatore cedo e com frequência** · código fácil de testar · cuidado com assistentes ("wizards") que você não entende.

## 7–8. Antes e durante o projeto
Poço de requisitos (documente abstrações, glossário) · resolva quebra-cabeças impossíveis · não comece até estar pronto · times pragmáticos · **automação ubíqua** · **teste implacavelmente** · documentação · grandes expectativas · orgulho e preconceito (assine seu trabalho).

## Dicas de uso rápido
- Revisão de código: procure violações de DRY, ortogonalidade e Demeter.
- Projeto novo: comece com um tracer bullet ponta a ponta.
- Bug: reproduza, isole, explique a alguém, corrija a causa, adicione teste.
