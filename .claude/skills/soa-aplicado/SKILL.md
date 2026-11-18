---
name: soa-aplicado
description: "SOA Aplicado — Integrando com web services e além (Alexandre Saudate, Casa do Código): começar um projeto SOA, formatos (CSV, XML, JSON), SOAP e WSDL (types, messages, portType, binding, service), JAX-WS e JAXB, contract-first, segurança (WS-Security), REST, ESB, orquestração com BPEL, governança e boas práticas de serviços. Use ao integrar sistemas via web services SOAP/REST ou desenhar arquitetura orientada a serviços."
---

# SOA Aplicado — Alexandre Saudate (Casa do Código)

Livro-fonte: `LivrosDev/SOA Aplicado - Integrando com web services e além - Autor (Casa do Código).pdf`

## Começando
- Coisas inesperadas acontecem em integração; escolha de formato (CSV vs linguagens de marcação), camada de transporte (HTTP, JMS), como testar um serviço (SoapUI), primeiro cliente Java.
- Web service ≠ SOA: SOA é **arquitetura** de serviços reutilizáveis, com contratos e governança.

## SOAP e WSDL
- Namespaces XML; envelope SOAP (header + body + fault).
- **WSDL:** `types` (XSD), `messages`, `portType` (operações), WSDL abstrato vs concreto, `binding` (estilo/encoding), `service` (endereço).
- **JAXB** para customizar o XML; resolver métodos com nomes iguais.
- **Contract-first** (WSDL primeiro) vs code-first: contract-first dá contratos estáveis.

## Além do básico
- Segurança: HTTPS, **WS-Security** (tokens, assinatura, criptografia).
- **REST** como alternativa mais simples.
- **ESB** (barramento): roteamento, transformação, mediação de protocolos.
- **Orquestração** com BPEL; coreografia.
- Governança: versionamento de contratos, registro de serviços, SLAs.

## Princípios de bons serviços
Contrato padronizado · baixo acoplamento · abstração · reusabilidade · autonomia · statelessness · descobrimento · composabilidade.

## Checklist de integração
- [ ] Contrato versionado e documentado
- [ ] Erros modelados (faults/status) e testados
- [ ] Timeouts, retries e idempotência definidos
- [ ] Segurança de transporte e mensagem
- [ ] Testes de contrato automatizados
