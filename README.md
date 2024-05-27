# Modelo data base

Instalar o CLI e a dependência do prisma
- npm i prisma -D
- npm i @prisma/client

Instalar a extensão "Prisma"
- va em extensões e instale a extensão caso não esteja instalado

Iniciar o prisma
- npx prisma init --datasource-provider SQLite

(No exemplo acima é usado o SQLite, mas é possivel usar outros bancos de dados)

Adicione o novo arquivo ".env" no ".gitignore"
> abaixo do "local env files" adicione ->
> .env
