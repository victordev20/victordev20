---
name: but-how-do-it-know
description: "But How Do It Know? (J. Clark Scott): como um computador funciona do zero — portas NAND, memória (bit, byte, registradores, RAM), barramento, ALU, clock, stepper, CPU, instruções, linguagem de máquina e periféricos. Use para explicar fundamentos de hardware/arquitetura de computadores de forma simples ou entender o que o código vira no nível mais baixo."
---

# But How Do It Know? — J. Clark Scott

Livro-fonte: `LivrosDev/But How Do It Know - The Basic Principles of Computers for Everyone - Author (J. Clark Scott).pdf`

## Ideia central
Todo o computador é construído a partir de **uma única peça: a porta NAND**, combinada em camadas cada vez mais úteis. Cada capítulo apresenta uma ideia simples.

## Construção em camadas
1. **Bits e portas:** NAND → NOT, AND, OR, XOR.
2. **Memória de 1 bit:** duas NANDs realimentadas guardam um estado; com o sinal "set".
3. **Byte e registrador:** 8 bits + "enabler" que controla saída no **barramento**.
4. **RAM:** decodificador seleciona endereço (registrador de endereço de memória) → 256 bytes no exemplo.
5. **Números e códigos:** binário, ASCII — o significado depende do contexto.
6. **ALU:** somador, shift, AND, OR, XOR, NOT, comparador; flags (carry, a-maior, igual, zero).
7. **Clock e stepper:** cadência que gera etapas; sinais set/enable em cada passo.
8. **CPU:** registradores de propósito geral, IAR (instruction address register), IR (instruction register), ciclo **buscar → decodificar → executar**.
9. **Instruções:** ALU, LOAD/STORE, DATA, JUMP, JUMP IF (condicional), CLF, I/O.
10. **Periféricos:** teclado, tela, disco via barramento de I/O.
11. **Linguagem de máquina, assembly e linguagens de alto nível**; o sistema operacional como programa.

## Como usar
- Para explicar "como o computador sabe" algo: mostre que não sabe — ele só segue sinais set/enable em sequência ditada pelo clock.
- Para depuração conceitual (overflow, flags, saltos), relacione com a ALU e o ciclo de instrução.
- Ao ensinar iniciantes, siga a ordem do livro: porta → memória → barramento → ALU → CPU → programa.
