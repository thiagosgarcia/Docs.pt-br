<span data-ttu-id="c79f0-101">O código de banco de dados de identidade gerado requer [migrações do Entity Framework Core](/ef/core/managing-schemas/migrations/).</span><span class="sxs-lookup"><span data-stu-id="c79f0-101">The generated Identity database code requires [Entity Framework Core Migrations](/ef/core/managing-schemas/migrations/).</span></span> <span data-ttu-id="c79f0-102">Criar uma migração e atualizar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c79f0-102">Create a migration and update the database.</span></span> <span data-ttu-id="c79f0-103">Por exemplo, execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="c79f0-103">For example, run the following commands:</span></span>

# <a name="visual-studiotabvisual-studio"></a>[<span data-ttu-id="c79f0-104">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c79f0-104">Visual Studio</span></span>](#tab/visual-studio)

<span data-ttu-id="c79f0-105">No Visual Studio **Package Manager Console**:</span><span class="sxs-lookup"><span data-stu-id="c79f0-105">In the Visual Studio **Package Manager Console**:</span></span>

```PMC
Add-Migration CreateIdentitySchema
Update-Database
```

# <a name="net-core-clitabnetcore-cli"></a>[<span data-ttu-id="c79f0-106">CLI do .NET Core</span><span class="sxs-lookup"><span data-stu-id="c79f0-106">.NET Core CLI</span></span>](#tab/netcore-cli)

```cli
dotnet ef migrations add CreateIdentitySchema
dotnet ef database update
```

------

<span data-ttu-id="c79f0-107">O parâmetro de nome "CreateIdentitySchema" para o `Add-Migration` comando é arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c79f0-107">The "CreateIdentitySchema" name parameter for the `Add-Migration` command is arbitrary.</span></span> <span data-ttu-id="c79f0-108">`"CreateIdentitySchema"` Descreve a migração.</span><span class="sxs-lookup"><span data-stu-id="c79f0-108">`"CreateIdentitySchema"` describes the migration.</span></span>