# Desafio Técnico FullStack - Big Core

![Badge](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

## Índice

- [Descrição](#descrição)
- [Demonstração](#demonstração)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Como Executar o Projeto](#como-executar-o-projeto)
- [Uso](#uso)
- [Funcionalidades](#funcionalidades)
- [Licença](#licença)

## Descrição

Este projeto foi desenvolvido como parte do desafio técnico da Big Core, com o objetivo de implementar uma arquitetura BFF utilizando .NET 8 no backend e Vue 3 com Vuetify no frontend.

## Demonstração

![Demonstração da Aplicação](https://github.com/user-attachments/assets/8cdd5f2b-c2f2-461c-b9ef-7efc4568896e)

## Tecnologias Utilizadas

**Frontend:**

- Vue 3
- Vite
- Vuetify
- Axios
- TypeScript

**Backend:**

- .NET 9
- ASP.NET Core
- HttpClientFactory
- FluentValidation
- Polly
- xUnit

**Outros:**

- Docker
- Docker Compose

## Como Executar o Projeto

### Pré-requisitos

- Node.js >= 18
- .NET 9 SDK
- Git: [Faça o download aqui](https://git-scm.com/downloads)
- Docker Desktop: [Faça o download aqui](https://www.docker.com/products/docker-desktop/)

### Passos

1.  **Clonar o Repositório:**

    Abra o seu terminal e execute o seguinte comando para clonar o repositório principal junto com seus submódulos:

    ```bash
    git clone --recurse-submodules https://github.com/CaioTito/DesafioBigCore.git
    ```

2.  **Iniciar os Contêineres Docker:**

    Navegue até a pasta raiz do projeto clonado e execute o comando abaixo para construir as imagens e iniciar os contêineres:

    ```bash
    docker-compose up --build
    ```

    Este comando irá baixar as dependências necessárias, construir as imagens para o frontend e backend, e iniciar os serviços definidos no arquivo `docker-compose.yml`.

3.  **Acessar a Aplicação:**

    Após os contêineres estarem em execução, abra o seu navegador de preferência e acesse:

    [`http://localhost`](http://localhost)

    Você deverá ver a tela inicial da aplicação.

    ![image](https://github.com/user-attachments/assets/8cdd5f2b-c2f2-461c-b9ef-7efc4568896e)

## Uso

Após iniciar a aplicação, acesse `http://localhost:3000`.

Na tela principal, você encontrará:

- **Botão de Filtro**:
  - Abre um modal onde é possível aplicar os seguintes filtros:
    - **StartDate** e **EndDate** (obrigatórios)
    - **LicensePlate** (lista de placas)
    - **IdTms** (lista de IDs do sistema do cliente)
    - **DivisionId** (seleção múltipla entre divisões fixas: Citrosuco, GLP, Amônia, Máquinas, Ácido, Treinamento)
  - Esses filtros são enviados ao backend como `query parameters`.

- **Botão de Configuração**:
  - Permite escolher:
    - Quais colunas da tabela serão exibidas.
    - A ordem em que elas aparecem.
  - As preferências são armazenadas via `localStorage`, mantendo as configurações mesmo após recarregar ou fechar o navegador.

- **Tabela Paginada**:
  - Exibe os dados retornados do backend.
  - A quantidade de itens por página também pode ser personalizada e é salva localmente.

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

 
## Licença

Este projeto está licenciado sob os termos da licença MIT.  
Veja o arquivo [LICENSE](./LICENSE) para mais detalhes.
