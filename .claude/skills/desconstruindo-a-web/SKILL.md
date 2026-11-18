---
name: desconstruindo-a-web
description: "Desconstruindo a Web — As tecnologias por trás de uma requisição (Willian Molinari, Casa do Código): o que acontece da barra de endereços até a página — URL, cache, resolução de nomes (glibc, DNS, UDP, sockets), IPv4/IPv6 e happy eyeballs, TCP e handshake, HTTP, TLS, servidor web, renderização no navegador. Use para explicar o caminho de uma requisição ou depurar problemas de rede/HTTP."
---

# Desconstruindo a Web — Willian Molinari (Casa do Código)

Livro-fonte: `LivrosDev/Desconstruindo a Web - As Tecnologias por Trás de uma Requisição - Autor (Casa do Código).pdf`

## O caminho de uma requisição
1. **Navegador:** interpreta a barra de endereços (busca vs URL), escolhe o protocolo (HSTS), consulta **cache** da URL.
2. **Sistema operacional:** chamada de sistema via **glibc** (`getaddrinfo`), `/etc/hosts`, `nsswitch`, cache local.
3. **Resolução DNS na rede:** resolvedor recursivo → raiz → TLD → autoritativo; registros A/AAAA/CNAME; DNS sobre **UDP** (porta 53); **sockets**.
4. **IP:** IPv4 e IPv6; **Happy Eyeballs** (tenta ambos e usa o mais rápido).
5. **TCP:** **three-way handshake** (SYN, SYN-ACK, ACK), janelas, retransmissão.
6. **TLS:** handshake, certificados, cadeia de confiança, SNI.
7. **HTTP:** requisição (método, path, headers como Host, User-Agent, Accept, Cookie), resposta (status, headers, corpo), keep-alive, HTTP/2.
8. **Servidor:** servidor web/proxy reverso → aplicação → banco → resposta.
9. **Navegador renderiza:** parse de HTML → DOM, CSS → CSSOM, JS, layout, paint; novas requisições para recursos.

## Ferramentas para inspecionar cada etapa
- `dig`/`nslookup` (DNS), `ping`/`traceroute` (IP), `tcpdump`/Wireshark (pacotes), `openssl s_client` (TLS), `curl -v` (HTTP), DevTools (rede e renderização), `strace` (syscalls).

## Uso
Ao depurar "o site não abre", percorra as etapas em ordem e confirme cada uma com a ferramenta correspondente.
