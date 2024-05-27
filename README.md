# Modelo data base

Instalar o CLI e a dependência do prisma
- npm i prisma -D
- npm i @prisma/client

Iniciar o prisma
- npx prisma init --datasource-provider SQLite

(No exemplo acima é usado o SQLite, mas é possivel usar outros bancos de dados)

Adicione o novo arquivo ".env" no ".gitignore"
> .gitignore
> local env files
> .env 
