╔══════════════════════════════════════════════════════╗
║             PIPELINE DE TESTES COM JENKINS           ║
║                       E CYPRESS                      ║
╚══════════════════════════════════════════════════════╝

Projeto de estudo de integração contínua para testes automatizados, utilizando Jenkins, Jenkinsfile, Cypress e relatórios Allure.

══════════════════════════════════════════════════════

## Sobre o projeto

O repositório permite explorar pipelines como código, execução de suítes de teste e publicação de relatórios de execução.

══════════════════════════════════════════════════════

## Objetivos

- Definir etapas de pipeline como código.
- Automatizar a execução de três suítes Cypress.
- Praticar execução paralela.
- Estudar a publicação de relatórios no Jenkins.

══════════════════════════════════════════════════════

## Tecnologias e ferramentas

- Jenkins Pipeline
- Node.js e npm
- Cypress
- Allure

══════════════════════════════════════════════════════

## Pré-requisitos

- Jenkins instalado e configurado com um agente compatível.
- Node.js disponível no agente e ferramenta global do Jenkins configurada com o nome `nodejs`.
- Google Chrome disponível no agente para as suítes que o exigem.
- Plugin Allure instalado no Jenkins para a etapa de publicação do relatório.
- Acesso ao repositório e permissão para executar o job.

══════════════════════════════════════════════════════

## Como executar pelo Jenkins

1. Crie um job do tipo **Pipeline** no Jenkins e conecte-o a este repositório.
2. Em agentes Linux/macOS, utilize `Jenkinsfile`, que usa comandos `sh`. Em agentes Windows, confira `Jenkinsfile-win`, que usa `bat`.
3. Confirme se os nomes das ferramentas e os plugins exigidos estão configurados no Jenkins.
4. Execute o job e consulte o console output. O pipeline principal executa as suítes `teste-suite-1`, `teste-suite-2` e `teste-suite-3` em paralelo.
5. Quando a publicação Allure estiver configurada, consulte o relatório na página do build.

══════════════════════════════════════════════════════

## Execução local

Com Node.js e npm instalados, execute na raiz do projeto:

```bash
npm install
npm run teste-suite-1
npm run teste-suite-2
npm run teste-suite-3
```

As suítes e seus caminhos estão definidos em `package.json`. A disponibilidade do Chrome e a configuração do Cypress podem afetar a execução local.

══════════════════════════════════════════════════════

## Estrutura do projeto

```text
ci-cd-teste-jenkins/
├── Jenkinsfile
├── Jenkinsfile-win
├── Jenkinsfile copy
├── cypress/
├── cypress.config.js
├── package.json
└── README.md
```

O arquivo `Jenkinsfile copy` é uma variante adicional; confira seu conteúdo antes de selecioná-lo no job.

══════════════════════════════════════════════════════

## Desafios práticos

- Configurar corretamente o agente de execução.
- Executar suítes em paralelo.
- Interpretar falhas e logs.
- Publicar relatórios de execução.

══════════════════════════════════════════════════════

## Boas práticas

- Versionar o pipeline junto ao projeto.
- Separar os testes em suítes.
- Utilizar os logs do Jenkins para diagnóstico.
- Publicar resultados como apoio à análise de falhas.

══════════════════════════════════════════════════════

## Aprendizados

A atividade permite praticar integração contínua, pipeline como código, execução paralela de testes Cypress e integração de relatórios Allure.

══════════════════════════════════════════════════════

## Considerações finais

Os pipelines exigem configuração compatível com o sistema operacional do agente. Ajuste ferramentas, plugins e caminhos conforme o ambiente Jenkins utilizado. A documentação não implica que o pipeline esteja atualmente executando com sucesso em todos os ambientes.

══════════════════════════════════════════════════════

## Formação e natureza da atividade

Este projeto foi desenvolvido como uma **atividade facultativa** no contexto dos estudos de Quality Assurance (QA), durante a formação da EBAC — Escola Britânica de Artes Criativas e Tecnologia. Seu objetivo é praticar e consolidar conhecimentos de CI/CD e automação de testes.

══════════════════════════════════════════════════════