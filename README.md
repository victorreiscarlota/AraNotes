# AraNotes (Clone do Notion)

![Foto AraNotes](https://cdn.discordapp.com/attachments/895030530154823720/1299852348377534504/image.png?ex=671eb555&is=671d63d5&hm=0acf6e640b0b87797f1a4abc6f8336826353df52f5231089592e511af9c3609f&)
[Acesse o site por aqui](https://aranotes.vercel.app)

## Descrição do Projeto

AraNotes é um projeto desenvolvido como parte da atividade de code review da matéria de Projeto de Software. O objetivo é criar um clone simplificado do Notion, utilizando Next.js para a interface do usuário, Convex no backend para gerenciamento de dados e Clerk para autenticação de usuários.

![Vídeo AraNotes](/assets/AraNotes%20-%20Opera%202024-10-26%2018-57-29.gif)

## Arquitetura do Projeto

- **Frontend**: O frontend é construído em Next.js, um framework React que facilita a criação de aplicações web com renderização do lado do servidor e geração de páginas estáticas. Isso garante uma melhor performance e otimização para SEO.
  
- **Backend**: O backend utiliza Convex, que oferece uma solução escalável para gerenciamento de dados em tempo real, simplificando a interação entre o frontend e o banco de dados.

- **Autenticação**: A autenticação de usuários é gerida pelo Clerk, que fornece uma interface fácil de usar para login, registro e gerenciamento de sessões, garantindo a segurança dos dados do usuário.

<br/>
<br/>
<br/>

## Clone do Repositório

### Passo 1.1 - Clonar o repositório
```
git clone https://github.com/victorreiscarlota/AraNotes.git
```

### Passo 1.2 - Instalar dependências

```
npm i -g pnpm
pnpm install
```


### Passo 1.3 - Executar o projeto

```
pnpm dev
```

- Em um novo terminal

```
pnpx convex dev
```
## Passo 2 - Configurar o .env

### 2.1 - Configuração do Convex - [Link de referência](https://docs.convex.dev/home)

### 2.2 - Configuração do Clerk - [Link de referência](https://clerk.com/docs)

### 2.3 - Configuração do Edge Store - [Link de referência](https://edgestore.dev/docs/quick-start)



