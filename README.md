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


No arquivo "prisma/schema.prisma" comece a criar as tabelas da sua preferência. Vou usar "User" como uma tabela de exemplo, ela terá um "id", "username", "name" e "created_at".
- model User {
-  id String @id @default(uuid())
-  username String @unique
-  name String
-  created_at DateTime default(now())

- @@map("users")
- }
