# DesafioBigCore

## Como Executar o Projeto

### Pré-requisitos

- Git
- Docker Desktop: [Faça o download aqui](https://www.docker.com/products/docker-desktop/)

### Passos

1.  **Clonar o Repositório:**

    Abra o seu terminal e execute o seguinte comando para clonar o repositório principal junto com seus submódulos:

    ```bash
    git clone --recurse-submodules https://github.com/CaioTito/DesafioBigCore.git
    ```

    *Substitua `seu-usuario` e `seu-repositorio-principal` pelos seus respectivos nomes de usuário e repositório no GitHub.*

2.  **Iniciar os Contêineres Docker:**

    Navegue até a pasta raiz do projeto clonado e execute o comando abaixo para construir as imagens e iniciar os contêineres:

    ```bash
    docker-compose up --build
    ```

    Este comando irá baixar as dependências necessárias, construir as imagens para o frontend e backend, e iniciar os serviços definidos no arquivo `docker-compose.yml`.

## Funcionalidades

### Frontend

O frontend da aplicação oferece as seguintes funcionalidades:

-   **Filtro:** Permite filtrar os dados apresentados com base em critérios específicos.
-   **Paginação:** Organiza grandes conjuntos de dados em páginas para facilitar a navegação.
-   **Configuração da Página:** Opções para personalizar a visualização e o número de itens por página.

### Backend

O backend foi desenvolvido seguindo as melhores práticas e padrões de arquitetura, incluindo:

-   **CQRS (Command Query Responsibility Segregation):** Separação das operações de leitura e escrita para otimizar a performance e escalabilidade.
-   **Validação:** Implementação de regras de validação robustas para garantir a integridade dos dados.
-   **Padrão Result:** Utilização do padrão Result para tratamento de sucessos e falhas de forma clara e consistente.
-   **Clean Architecture:** Arquitetura limpa para promover a separação de responsabilidades, testabilidade e manutenibilidade.
-   **Polly:** Utilização da biblioteca Polly para implementar políticas de resiliência, como retentativas (retry) em caso de falhas temporárias.
-   **DTOs (Data Transfer Objects):** Uso de DTOs para transferir dados entre as camadas da aplicação de forma eficiente e desacoplada.
-   **Testes Unitários:** Cobertura de testes unitários para garantir a qualidade e o correto funcionamento das lógicas de negócio.