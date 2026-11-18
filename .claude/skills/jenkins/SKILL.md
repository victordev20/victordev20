---
name: jenkins
description: "Jenkins — Automatize tudo sem complicações (Fernando Boaglio, Casa do Código): integração contínua, instalação, conceitos (job, build, pipeline, plugin, artifact, dashboard/view, executor, nós master/slave, workspace), builds de pacotes web, testes e relatórios, qualidade de código, deploy, pipelines como código (Jenkinsfile), segurança e manutenção. Use ao configurar ou depurar jobs e pipelines no Jenkins."
---

# Jenkins — Fernando Boaglio (Casa do Código)

Livro-fonte: `LivrosDev/Jenkins - Automatize Tudo sem Complicações - Autor (Casa do Código).pdf`

## Conceitos fundamentais
- **Job:** tarefa configurada; **Build:** uma execução do job; **Pipeline:** sequência de estágios; **Plugin:** extensões (Git, Maven, JUnit, Slack...); **Artifact:** saída arquivada; **Dashboard/View:** organização visual; **Executor:** slot de execução; **Nó master/agentes (slaves):** distribuem builds; **Workspace:** diretório de trabalho do job.

## Jornada do livro
1. Por que integração contínua; instalação (WAR, pacote, Docker) e organização inicial.
2. **Builds** de pacote web (Maven/Gradle/npm), gatilhos (SCM polling, webhooks, agendamento cron).
3. **Testes e relatórios** (JUnit, cobertura), qualidade de código (SonarQube, Checkstyle).
4. **Deploy** automatizado para servidores/ambientes.
5. **Pipelines** encadeados e como código:
```groovy
pipeline {
  agent any
  stages {
    stage('Build') { steps { sh 'mvn -B package' } }
    stage('Test')  { steps { sh 'mvn test' } post { always { junit 'target/surefire-reports/*.xml' } } }
    stage('Deploy'){ when { branch 'main' } steps { sh './deploy.sh' } }
  }
}
```
6. **Agentes distribuídos**, segurança (usuários, matriz de permissões, credenciais), backup e manutenção (atualizações, limpeza de builds antigos).

## Boas práticas
- Pipeline como código (`Jenkinsfile`) versionado com a aplicação.
- Credenciais no Credentials Store, nunca no script.
- Builds rápidos; notificar falhas imediatamente.
- Não rodar builds no master; use agentes.
- Mantenha poucos plugins e atualizados.
