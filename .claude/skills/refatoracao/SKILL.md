---
name: refatoracao
description: "Refatoração — Aperfeiçoando o design de códigos existentes, 2ª ed. (Martin Fowler): primeiro exemplo, princípios (o que, por que, quando, quando não), maus cheiros no código, testes como rede de segurança e o catálogo de refatorações (extrair função/variável, encapsular, mover, organizar dados, simplificar condicionais, refatorar APIs, lidar com herança). Use ao refatorar código, identificar code smells ou planejar melhorias de design seguras."
---

# Refatoração (2ª ed.) — Martin Fowler

Livro-fonte: `LivrosDev/Refatoração - Aperfeiçoando o Design de Códigos Existentes - Autor (Martin Fowler).pdf`

## Princípios
- **Refatoração:** mudança na estrutura interna sem alterar o comportamento observável, em **passos pequenos**, com testes passando a cada passo.
- Os "dois chapéus": adicionar funcionalidade **ou** refatorar — nunca os dois ao mesmo tempo.
- **Quando:** regra de três; preparatória ("torne a mudança fácil, depois faça a mudança fácil"); para compreensão; limpeza de lixo; durante code review.
- **Quando não:** código que não precisa ser entendido/alterado, ou quando reescrever é mais barato.
- Exige **testes autoverificáveis** rápidos.

## Maus cheiros (cap. 3)
Nome misterioso · Código duplicado · Função longa · Lista longa de parâmetros · Dados globais · Dados mutáveis · Alteração divergente · Cirurgia com rifle · Inveja de recursos · Agrupamentos de dados · Obsessão por primitivos · Switches repetidos · Laços · Elemento ocioso · Generalidade especulativa · Campo temporário · Cadeias de mensagens · Intermediário · Trocas escusas · Classe grande · Classes alternativas com interfaces diferentes · Classe de dados · Herança recusada · Comentários (como desodorante).

## Catálogo (principais)
- **Primeiro conjunto:** Extrair Função / Internalizar Função, Extrair Variável / Internalizar Variável, Mudar Declaração de Função, Encapsular Variável, Renomear Variável, Introduzir Objeto de Parâmetro, Combinar Funções em Classe/Transformação, Separar em Fases.
- **Encapsulamento:** Encapsular Registro/Coleção, Substituir Primitivo por Objeto, Substituir Variável Temporária por Consulta, Extrair Classe, Ocultar Delegação, Substituir Algoritmo.
- **Mover recursos:** Mover Função/Campo, Mover Instruções, Dividir Laço, Substituir Laço por Pipeline, Remover Código Morto.
- **Organizar dados:** Separar Variável, Substituir Variável Derivada por Consulta, Mudar Referência para Valor (e vice-versa).
- **Condicionais:** Decompor Condicional, Consolidar Expressão Condicional, Substituir Condicional Aninhada por Cláusulas de Guarda, **Substituir Condicional por Polimorfismo**, Introduzir Caso Especial, Introduzir Asserção.
- **APIs:** Separar Consulta de Modificador, Parametrizar Função, Remover Argumento-Flag, Preservar Objeto Inteiro, Substituir Construtor por Função de Fábrica, Substituir Função por Comando.
- **Herança:** Subir/Descer Método/Campo, Substituir Código de Tipo por Subclasses, Extrair Superclasse, Substituir Subclasse/Superclasse por Delegação.

## Procedimento
1. Garanta testes cobrindo o comportamento.
2. Identifique o cheiro → escolha a refatoração do catálogo.
3. Aplique a mecânica em passos minúsculos; rode os testes a cada passo; commit frequente.
4. Pare quando o código estiver claro o suficiente para a mudança desejada.
