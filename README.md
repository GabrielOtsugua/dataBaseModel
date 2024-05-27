# Modelo data base

Instalar o CLI e a dependência do prisma
- npm i prisma -D
- npm i @prisma/client

Instalar a extensão "Prisma"
- va em extensões e instale a extensão caso não esteja instalado

Iniciar o prisma
- npx prisma init --datasource-provider SQLite

(No exemplo acima é usado o SQLite, mas é possivel usar outros bancos de dados)

Adicionar o novo arquivo ".env" no ".gitignore"
> abaixo do "local env files" adicione ->
> .env


No arquivo "prisma/schema.prisma" comece a criar as tabelas da sua preferência
"User" será uma tabela de exemplo, ela terá um "id", "username", "name" e "created_at"
- model User {
- id         String @id @default(uuid())
- username   String @unique
- name       String
- created_at DateTime default(now())

- @@map("users")
- }

Confirmar a criação da tabela
-npx prisma migrate dev

(O comando acima criará uma migration com um determinado nome)
(Você pode ver a migration criada em "prisma/migrations")

Veja seu banco de dados
- npx prisma studio

Em "src", crie um arquivo "lib/prisma.ts" e adicione:
- import { PrismaClient } from "@prisma/client"
- export const prisma = new PrismaClient({
- log: ['query'],
- })
