# Arquitetura

O Produto de Teste é composto por três camadas:

- **Cliente** — renderiza as páginas de documentação.
- **Servidor** — busca arquivos `mkdocs.yml` no GitHub e serve o conteúdo processado.
- **Repositório GitHub** — armazena o `mkdocs.yml` e os arquivos markdown de origem.
