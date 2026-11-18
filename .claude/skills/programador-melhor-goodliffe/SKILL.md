---
name: programador-melhor-goodliffe
description: "Como ser um Programador Melhor (Pete Goodliffe): importar-se com o código, aparência e estilo, escrever menos e remover código, código legado, tratamento de erros, depuração, testes, complexidade, simplicidade, reutilização, versionamento, releases, aprendizado, ética e atitude. Use em code reviews, refatorações e reflexões sobre qualidade e postura profissional."
---

# Como ser um Programador Melhor — Pete Goodliffe

Livro-fonte: `LivrosDev/Como ser um Programador Melhor - um Manual Para Programadores que se Importam com Código - Autor (Pete Goodliffe).pdf`

## Parte I — você.escreve(código)
- **Importe-se com o código.** Atitude é o que separa bons programadores.
- **Mantenha as aparências:** formatação consistente, nomes claros, estilo do projeto > preferência pessoal.
- **Escreva menos código** e **melhore removendo código**: código morto, duplicado, comentários inúteis, especulação (YAGNI).
- **Fantasma do código passado:** aprenda com seu próprio código antigo.
- **Percorrendo um caminho / chafurdando na lama:** como entender e navegar código desconhecido ou ruim (comece pequeno, crie testes, melhore ao passar — regra do escoteiro).
- **Não ignore erros** e **espere o inesperado:** trate retornos, exceções, threads, recursos.
- **Caça aos bugs:** reproduza, isole, use ferramentas (debugger, logs, bisect), corrija a causa raiz, adicione teste.
- **É hora de testar:** testes rápidos, legíveis, independentes; TDD.
- **Lidando com complexidade** e **conto de dois sistemas:** desenho simples e coeso vence.

## Parte II — A prática leva à perfeição
- Desenvolvimento de software é arte, ciência, esporte, brincadeira…
- **Jogue segundo as regras** do time; **mantenha a simplicidade**; **use o cérebro** (não programe no automático).
- **Nada está gravado a ferro e fogo:** todo código pode mudar.
- **Reutilização** com cautela; **controle de versão** disciplinado (commits pequenos e com boas mensagens).
- **Marcando um gol / código congelado / releases:** entregas previsíveis e reproduzíveis.

## Partes III–V — Pessoal e pessoas
- Aprenda sempre (ler, experimentar, ensinar); prática deliberada.
- Ética, linguagem e comunicação; trabalhe bem em equipe; **atitude** acima de tudo.

## Checklist de code review (inspirado no livro)
- [ ] Há código que pode ser removido?
- [ ] Todos os erros são tratados de forma explícita?
- [ ] Nomes revelam intenção?
- [ ] O código está mais simples do que estava?
- [ ] Existe teste para o bug corrigido?
