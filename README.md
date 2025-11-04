# Lab04 - Integração Contínua com Docker e GitHub Actions

---

Este repositório contém a implementação de um workflow de Integração Contínua (CI) utilizando o **Docker** e **GitHub Actions**. O objetivo deste projeto foi configurar um pipeline para automatizar o processo de construção e deploy de uma aplicação Node.js usando Docker, além de integrar com o DockerHub e o Google Cloud Platform (GCP).

## Objetivo

O principal objetivo deste exercício foi criar um workflow que:
1. Realiza o **checkout** do código sempre que um commit é enviado para o repositório.
2. Configura o Docker e executa o **build** de uma imagem Docker para a aplicação.
3. Faz o **push** da imagem Docker para o **DockerHub**.
4. Realiza o **deploy** da aplicação no **Google Cloud Run**, utilizando a imagem Docker recém-criada.

## Estrutura do Projeto

- **.github/workflows/test.yml**: Contém o arquivo de configuração do GitHub Actions que define o workflow, incluindo etapas de build, push para o DockerHub e deploy para o Google Cloud.
- **docker-compose.yml**: Arquivo de configuração do Docker Compose para orquestrar a aplicação.
- **Dockerfile**: Define a imagem Docker para a aplicação Node.js.
- **package.json**: Define as dependências do projeto, incluindo bibliotecas como `express` e outras.
- **app.js**: Script principal da aplicação que executa a lógica do servidor Node.js.
- **.gitignore**: Arquivo que define quais arquivos e diretórios o Git deve ignorar (como o `node_modules`).
- **README.md**: Este arquivo de documentação.

## Passos Realizados

1. **Configuração do Docker**: A aplicação foi empacotada dentro de um container Docker usando um **Dockerfile**.
2. **Configuração do GitHub Actions**: O workflow foi configurado para rodar automaticamente com cada commit, realizando os processos de build, teste, push para o DockerHub e deploy no Google Cloud.
3. **Credenciais de DockerHub**: As credenciais de acesso ao DockerHub foram armazenadas como secrets no repositório para garantir a segurança durante o login e push da imagem Docker.
4. **Deploy no Google Cloud**: O deploy da imagem Docker foi realizado no Google Cloud Run, garantindo que a aplicação estivesse disponível na nuvem.

## Conclusão

Este exercício permitiu a configuração de um pipeline de Integração Contínua (CI) completo, com **Docker**, **GitHub Actions**, **DockerHub** e **Google Cloud**. A automação do processo de build, push e deploy facilita a gestão de ambientes de desenvolvimento e produção, além de garantir que a aplicação seja entregue de forma contínua e eficiente.

---

### Discente: Alicia Caldeira  
### Curso: Web Academy - UFAM
