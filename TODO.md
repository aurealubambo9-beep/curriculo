# Entregas do portfólio

## Aplicação e navegação
- [x] Criar uma aplicação Next.js com App Router em JavaScript, CSS tradicional personalizado e idioma pt-BR.
- [x] Implementar as rotas `/`, `/sobre`, `/experiencia-academica`, `/experiencia-profissional` e `/projetos`, acessíveis diretamente após atualização.
- [x] Reutilizar Header e Footer, usar `Link` para navegação interna, destacar a página ativa com `aria-current` e oferecer menu móvel acessível.

## Conteúdo configurável
- [x] Centralizar nome, curso, instituição, biografia, objetivos, contatos, GitHub, LinkedIn, formação, experiências, projetos manuais, habilidades e tecnologias em `data/portfolio.js`.
- [x] Manter dados pessoais não fornecidos como instruções provisórias claramente editáveis, sem inventar estatísticas, empresas, diplomas, links ou resultados.

## Páginas e experiência visual
- [x] Criar Home com hero, cartão visual de código, indicadores descritivos, habilidades, projetos em destaque e chamada final.
- [x] Criar Sobre com tecnologias, conceitos, módulos e ferramentas usados no projeto.
- [x] Criar experiência acadêmica em timeline, usando conteúdo provisório claramente identificado.
- [x] Criar experiência profissional honesta quando ainda não houver experiência formal, sem botão de PDF inexistente.
- [x] Criar visual tecnológico escuro usando a paleta definida, gradientes sutis, CSS responsivo, foco visível, animações discretas e respeito a `prefers-reduced-motion`.

## Integração GitHub
- [x] Buscar repositórios públicos pelo endpoint configurável da API oficial do GitHub usando `fetch`.
- [x] Exibir nome, descrição, linguagem, atualização, código, demonstração real quando existir e estado arquivado.
- [x] Diferenciar dados da API e projetos manuais, normalizar URLs para deduplicação e tratar carregamento, erro HTTP, rate limit, falha de rede, resposta inválida, lista vazia e atualização manual.

## Documentação e verificação
- [x] Criar `README.md` com instalação, scripts, configuração do GitHub, API, GitHub/Vercel e estrutura.
- [x] Criar `public/manus-routes.json` com todas as rotas de página.
- [x] Executar `npm install`, `npm run build`, verificações HTTP das cinco rotas, checagem HTTP do manifesto, consulta real à API do GitHub e `npm audit --audit-level=high`.
- [ ] Preencher os dados pessoais reais, criar o repositório próprio no GitHub e publicar na Vercel; essas ações dependem do proprietário do portfólio.
