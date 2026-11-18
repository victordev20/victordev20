---
name: redes-forouzan
description: "Comunicação de Dados e Redes de Computadores (Behrouz A. Forouzan): modelos OSI e TCP/IP, camada física (sinais, transmissão, multiplexação, meios), enlace (detecção/correção de erros, controle de acesso, Ethernet, Wi-Fi), rede (IPv4/IPv6, endereçamento, roteamento), transporte (UDP, TCP, controle de congestionamento, QoS), aplicação (DNS, HTTP, e-mail) e segurança. Use para estudar ou explicar fundamentos de redes."
---

# Comunicação de Dados e Redes de Computadores — Behrouz A. Forouzan

Livro-fonte: `LivrosDev/Comunicação de Dados e Redes de Computadores - Autor (Behrouz A. Forouzan).pdf`

## Visão geral
- Componentes da comunicação (mensagem, emissor, receptor, meio, protocolo); fluxo simplex/half/full-duplex.
- Topologias, LAN/MAN/WAN, internetwork, padrões (IETF/RFCs, IEEE, ITU).
- **Modelos:** OSI (7 camadas) × TCP/IP; encapsulamento; endereços físico, lógico, porta e específicos.

## Por camada
1. **Física:** sinais analógicos/digitais, largura de banda, taxa de Nyquist e capacidade de Shannon, codificação (NRZ, Manchester), modulação (ASK, FSK, PSK, QAM), multiplexação (FDM, TDM, WDM), espalhamento espectral, meios guiados e não guiados, comutação (circuitos, pacotes).
2. **Enlace:** detecção/correção de erros (paridade, CRC, checksum, Hamming), controle de fluxo (Stop-and-Wait, Go-Back-N, Selective Repeat), HDLC/PPP, acesso múltiplo (ALOHA, CSMA/CD, CSMA/CA, token), **Ethernet**, **Wi-Fi 802.11**, Bluetooth, VLANs, switches.
3. **Rede:** IPv4 (classes, CIDR, sub-redes, NAT), IPv6, ARP, ICMP, **roteamento** (vetor de distância/RIP, estado de enlace/OSPF, BGP), multicast.
4. **Transporte:** UDP, **TCP** (handshake de 3 vias, janelas, retransmissão, controle de congestionamento: slow start, congestion avoidance), SCTP, QoS.
5. **Aplicação:** **DNS**, HTTP/WWW, SMTP/POP/IMAP, FTP, SNMP, multimídia.
6. **Segurança:** criptografia simétrica/assimétrica, assinaturas, IPSec, SSL/TLS, firewalls.

## Como usar
- Ao depurar problema de rede: localize a camada (física → aplicação), teste de baixo para cima (`ping`, `traceroute`, `dig`, `curl`).
- Ao estudar: faça os exercícios de cálculo (sub-rede, throughput, atraso de propagação).
