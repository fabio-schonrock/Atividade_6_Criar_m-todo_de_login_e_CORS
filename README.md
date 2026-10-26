# Exo.WebApi

API de projetos e usuários com autenticação JWT e SQL Server.

## Requisitos

- .NET 6 SDK ou superior
- SQL Server Express com a instância `SQLEXPRESS`
- Banco de dados `ExoApi` criado no SQL Server

Se o SQL Server estiver em outra instância, ajuste a connection string `ExoApi` em `appsettings.json`.

## Configurar a chave JWT

A chave de assinatura não é armazenada no repositório. Configure-a localmente com User Secrets:

```powershell
dotnet user-secrets set "Jwt:SigningKey" "<chave aleatória com pelo menos 32 bytes>"
```

Ou defina a variável de ambiente `Jwt__SigningKey`. A API não inicia se a chave não estiver configurada ou tiver menos de 32 bytes.

## Executar

```powershell
dotnet run
```

A API usa as portas definidas em `Properties/launchSettings.json`.
