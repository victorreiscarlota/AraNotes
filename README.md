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
```bash
git clone https://github.com/victorreiscarlota/AraNotes.git
```

### Passo 1.2 - Instalar dependências
```bash
npm i -g pnpm
pnpm install
```

### Passo 1.3 - Executar o projeto
```bash
pnpm dev
```
- Em um novo terminal:
```bash
pnpx convex dev
```

## Passo 2 - Configurar o .env

### 2.1 - Configuração do Convex - [Link de referência](https://docs.convex.dev/home)

### 2.2 - Configuração do Clerk - [Link de referência](https://clerk.com/docs)

### 2.3 - Configuração do Edge Store - [Link de referência](https://edgestore.dev/docs/quick-start)

## Documentação dos Componentes

### Estrutura de Componentes

Abaixo está um resumo dos componentes principais do projeto, organizados por diretórios e função:

#### Diretório: **app/_components**
- **Banner.tsx**: Componente responsável por exibir o banner principal do sistema, geralmente contendo informações iniciais ou um resumo da aplicação.
- **document-list.tsx**: Exibe a lista de documentos do usuário, fornecendo uma interface para visualizar e gerenciar documentos.
- **Item.tsx**: Representa um item reutilizável, utilizado na renderização de listas.
- **Menu.tsx**: Menu de navegação principal, que facilita o acesso às diferentes seções do app.
- **Navbar.tsx**: Barra de navegação superior, contendo opções como login e links importantes.
- **Navigation.tsx**: Componente utilizado para a navegação geral da aplicação, permitindo transição entre as seções.
- **Publish.tsx**: Utilizado para gerenciar publicações e disponibilizar conteúdo criado pelo usuário.
- **Title.tsx**: Exibe o título de uma página ou seção, ajudando na organização visual da aplicação.
- **trash-box.tsx**: Gerencia a lixeira do usuário, onde itens excluídos temporariamente são mantidos.
- **user-item.tsx**: Representa um usuário ou um item relacionado ao perfil do usuário.

#### Diretório: **components**
- **Editor**: Contém componentes relacionados ao editor de texto principal:
  - **Editor.tsx**: Principal componente do editor de texto, onde o usuário pode escrever e editar suas anotações.
  - **Toolbar.tsx**: Barra de ferramentas para o editor, incluindo opções como negrito, itálico e listas.
- **modals**: Componentes modais utilizados para interações específicas:
  - **confirm-modal.tsx**: Modal de confirmação para ações críticas, como excluir documentos.
  - **cover-image-modal.tsx**: Modal para selecionar e definir a imagem de capa de um documento.
  - **settings-modal.tsx**: Modal para configurações gerais do usuário ou documento.
- **providers**: Fornecedores de contexto da aplicação:
  - **convex-provider.tsx**: Provedor para integração do Convex, permitindo acesso a funcionalidades de backend.
  - **modal-provider.tsx**: Provedor que gerencia o estado e a exibição dos modais na aplicação.
  - **theme-provider.tsx**: Gerencia o tema da aplicação, permitindo alternar entre modos claro e escuro.
- **ui**: Componentes de interface do usuário:
  - **Cover.tsx**: Exibe a imagem de capa dos documentos.
  - **icon-picker.tsx**: Permite ao usuário escolher ícones para representar seus documentos.
  - **mode-toggle.tsx**: Alterna entre os modos claro e escuro.
  - **search-command.tsx**: Barra de pesquisa para buscar documentos e comandos.
  - **single-image-dropzone.tsx**: Zona para arrastar e soltar uma imagem única, utilizada na definição de capas ou uploads.
  - **spinner.tsx**: Indicador de carregamento para ações em andamento.

### Estrutura de Pastas e Integração
Os componentes estão organizados de forma modular, facilitando a reutilização e manutenção. 
- A pasta `app/_components` contém componentes principais da aplicação que são utilizados em diversas partes do sistema.
- A pasta `components` é mais subdividida e conta com componentes específicos, como o editor e modais.
- A pasta `providers` é responsável pelo contexto e funcionalidades compartilhadas da aplicação.

### Exemplos de Uso
Cada componente foi desenvolvido com o intuito de ser reutilizável dentro do sistema AraNotes. Por exemplo:
- **Toolbar.tsx** é utilizada exclusivamente no contexto do **Editor.tsx** para oferecer funcionalidades de edição de texto de forma mais intuitiva.
- **modal-provider.tsx** permite abrir qualquer um dos modais (é utilizado em conjunto com os modais para manter a consistência no comportamento).

### Notas sobre Integração com Outros Módulos
A integração entre o frontend e o backend ocorre principalmente através dos provedores (`convex-provider.tsx`). Além disso, o **theme-provider.tsx** é um exemplo de como funcionalidades globais (como o tema) são disponibilizadas para toda a aplicação.
