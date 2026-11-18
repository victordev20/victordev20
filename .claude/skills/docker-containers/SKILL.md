---
name: docker-containers
description: "Containers com Docker — Do desenvolvimento à produção (Daniel Romero, Casa do Código): containers vs VMs, namespaces, cgroups, union filesystems, comandos Docker, Dockerfile, volumes, redes, Docker Compose, Docker Hub/registry, Machine, Swarm e práticas para produção. Use ao conteinerizar aplicações, escrever Dockerfiles/compose ou depurar containers."
---

# Containers com Docker — Casa do Código

Livro-fonte: `LivrosDev/Containers com Docker - Do desenvolvimento à produção - Autor (Casa do Código).pdf`

## Conceitos
- Container ≠ VM: compartilha o kernel do host; isolamento via **namespaces** (pid, net, mnt, uts, ipc, user), limites via **cgroups**, camadas via **union file systems**.

## Uso básico
- `docker run -it --rm`, `-d`, `-p host:container`, `-v`, `--name`, `docker ps -a`, `logs -f`, `exec -it`, `stop/start`, `rm`, `rmi`, `images`, `inspect`.
- Exportar/importar containers; salvar/carregar imagens.

## Dockerfile
- `FROM`, `RUN`, `COPY/ADD`, `WORKDIR`, `EXPOSE`, `ENV`, `CMD`/`ENTRYPOINT`, `VOLUME`, `USER`.
- Cada instrução é uma camada → ordene do que muda menos para o que muda mais (cache).
- Logs para stdout/stderr.

## Volumes e redes
- Volumes nomeados ou bind mounts; `VOLUME` no Dockerfile; backup/restore com container auxiliar.
- Redes: bridge padrão, redes definidas pelo usuário (DNS por nome), comunicação entre hosts (overlay).

## Orquestração e distribuição
- **Docker Compose** para multi-container (`services`, `depends_on`, `volumes`, `networks`).
- **Docker Hub / registry privado**; **Docker Machine**; **Swarm** para cluster.
- Integração contínua e deploy com imagens versionadas.

## Boas práticas
- Imagens pequenas (base slim/alpine, **multi-stage build**), `.dockerignore`.
- Um processo por container; stateless; configuração por variável de ambiente.
- Não rodar como root; não embutir segredos na imagem.
- Tags imutáveis (não depender de `latest` em produção).
- Healthchecks e limites de CPU/memória.
