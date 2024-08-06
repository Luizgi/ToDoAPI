# ToDoApi

## Descrição

ToDoApi é uma API simples de tarefas a fazer (To-Do) desenvolvida em ASP.NET Core com C#. A API permite criar, ler, atualizar e excluir tarefas, integrando o Entity Framework Core com um banco de dados SQL Server e utilizando Swagger para documentação.

## Funcionalidades

- **Criar Tarefa**: Adicionar uma nova tarefa.
- **Ler Tarefas**: Listar todas as tarefas.
- **Ler Tarefa por ID**: Obter uma tarefa específica pelo ID.
- **Atualizar Tarefa**: Atualizar uma tarefa existente.
- **Excluir Tarefa**: Remover uma tarefa.

## Tecnologias Utilizadas

- **ASP.NET Core 6.0**
- **Entity Framework Core**
- **SQL Server**
- **Swagger (Swashbuckle)**

## Requisitos

- .NET 6.0 SDK
- SQL Server

## Configuração e Execução

### Passo 1: Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/ToDoApi.git
cd ToDoApi
```

### Passo 2: Configurar o Banco de Dados

Certifique-se de que o SQL Server esteja em execução e atualize a string de conexão no arquivo `appsettings.json` se necessário.

```json
"ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=ToDoDb;Trusted_Connection=True;MultipleActiveResultSets=true"
}
```

### Passo 3: Aplicar Migrações

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

### Passo 4: Executar a Aplicação

```bash
dotnet run
```

### Passo 5: Acessar a Documentação do Swagger

Abra o navegador e acesse `https://localhost:<port>/swagger` para visualizar a documentação interativa da API.

## Endpoints

- **GET /api/Tasks**: Obter todas as tarefas.
- **GET /api/Tasks/{id}**: Obter uma tarefa pelo ID.
- **POST /api/Tasks**: Criar uma nova tarefa.
- **PUT /api/Tasks/{id}**: Atualizar uma tarefa existente.
- **DELETE /api/Tasks/{id}**: Excluir uma tarefa.

## Estrutura do Projeto

```plaintext
ToDoApi
├── Controllers
│   └── TasksController.cs
├── Data
│   └── TaskContext.cs
├── Models
│   └── TaskItem.cs
├── Properties
├── appsettings.Development.json
├── appsettings.json
├── Program.cs
├── ToDoApi.csproj
└── Startup.cs
```

## Contribuição

Se você deseja contribuir com este projeto, siga os passos abaixo:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature ou correção (`git checkout -b feature/MinhaFeature`).
3. Faça commit das suas alterações (`git commit -m 'Adicionei MinhaFeature'`).
4. Faça push para a branch (`git push origin feature/MinhaFeature`).
5. Abra um Pull Request.
