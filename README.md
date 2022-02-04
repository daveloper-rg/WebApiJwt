## Authentication and Identity Core in ASP.NET Core 6
# Introduction
- JWT is a RFC7519 Standard

# Configuration
- Create migrations for database (SQLite)
```
dotnet ef migrations add FirstMigration -o Persistence/Migrations
```

# Test solution
- Create token
```
POST {{host}}/token
Content-Type: application/json

{
	"userName": "test.demo",
	"password": "P@ss.W0rd"
}
```
- Verify token
```
GET {{host}}/me
Content-Type: application/json
Authorization: Bearer {{jwt}}
```