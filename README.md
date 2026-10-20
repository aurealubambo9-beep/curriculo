# Portfólio pessoal em Next.js

Aplicação acadêmica de currículo e portfólio pessoal para um estudante de tecnologia. O projeto demonstra como criar páginas semânticas com Next.js App Router, organizar componentes React reutilizáveis, escrever CSS próprio e consumir uma API pública com `fetch`.

## Tecnologias utilizadas

- Next.js 16 com App Router
- React 19 e JavaScript
- CSS tradicional, sem Tailwind ou biblioteca visual pronta
- Fetch API e API pública oficial do GitHub
- Git/GitHub para versionamento
- Vercel como opção de publicação

## Funcionalidades

O site possui cinco rotas: Home, Sobre, Experiência Acadêmica, Experiência Profissional e Projetos. Header, Footer, dados pessoais, cartões, timeline e estados de interface são reutilizáveis. A navegação funciona com `next/link`, há menu móvel acessível, metadados básicos de SEO, responsividade, foco visível e respeito à preferência de movimento reduzido.

A página de Projetos consulta `https://api.github.com/users/USUARIO/repos?sort=updated`, exibe repositórios públicos e trata carregamento, erros HTTP, limite de requisições, falha de rede, resposta inválida, lista vazia e atualização manual. Projetos cadastrados manualmente ficam separados dos dados da API e não são duplicados quando usam o mesmo endereço de repositório.

## Estrutura

```text
app/
├── layout.js                         # Layout, Header, Footer e metadados
├── page.js                           # Home
├── globals.css                       # Identidade visual e responsividade
├── sobre/page.js
├── experiencia-academica/page.js
├── experiencia-profissional/page.js
└── projetos/page.js                  # Integração com GitHub
components/                           # Componentes React reutilizáveis
data/portfolio.js                     # Configuração central editável
public/manus-routes.json              # Manifesto das rotas para o ambiente Manus
```

## Como executar localmente

Pré-requisitos: Node.js 18.17 ou superior e npm.

```bash
npm install
npm run dev
```

Abra `http://localhost:3000` no navegador. Para verificar a compilação de produção:

```bash
npm run build
npm start
```

## Como personalizar

Edite somente `data/portfolio.js` para trocar o nome, iniciais, curso, instituição, biografia, objetivos, localização, e-mail, GitHub, LinkedIn, formação, experiências, habilidades, tecnologias, ferramentas e projetos manuais.

O `githubUsername` está configurado como `aurealubambo9-beep` e pode ser alterado em `data/portfolio.js` quando necessário. Os campos de formação ainda marcados como provisórios devem ser substituídos por informações reais. Não é necessário criar token: a implementação usa a API pública sem segredo no navegador.

Um projeto manual segue este formato:

```js
{
  name: 'Nome do projeto',
  description: 'Descrição real e curta.',
  technologies: ['React', 'CSS'],
  html_url: 'https://github.com/seu-usuario/seu-repositorio',
  demo: 'https://seu-site-real.vercel.app'
}
```

Só informe uma demonstração quando a URL realmente existir. O botão de currículo em PDF não é exibido porque não há um arquivo real no projeto.

## GitHub e Vercel

Para versionar o projeto, crie um repositório vazio no GitHub e conecte a pasta local com Git. Não adicione URLs fictícias ao README. Depois, importe o repositório na Vercel, confirme o framework Next.js e clique em **Deploy**. A Vercel detectará os scripts do `package.json` automaticamente.

Exemplo de fluxo local:

```bash
git init
git add .
git commit -m "feat: cria portfólio pessoal"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

Substitua os dois valores de exemplo antes de executar. A URL final da produção só deve ser adicionada depois que o deploy for concluído.

## Verificações realizadas

Foram executados `npm install`, `npm run build`, verificações HTTP das cinco rotas e uma requisição real à API pública do GitHub, que respondeu com uma lista válida. Também foi conferido o manifesto `public/manus-routes.json` via HTTP e o `npm audit --audit-level=high`, sem vulnerabilidades reportadas. A publicação no GitHub e na Vercel, assim como o preenchimento dos dados pessoais, dependem das contas e informações do proprietário do portfólio.
