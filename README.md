# Portfólio Acadêmico e de P&D — Diego Perdigão Sousa, D.Sc.

Site pessoal bilíngue (`EN | PT`) construído em **Jekyll / AcademicPages**, publicado via GitHub Actions em:
**[https://diegoperdigao.github.io/](https://diegoperdigao.github.io/)**

## Principais Recursos

* **Bilíngue (`EN | PT`) com persistência:** Alternância instantânea entre inglês e português em todas as páginas, barra de navegação, barra lateral, projetos e publicações.
* **Tema Claro/Escuro (`Light | Dark`):** Seletor no cabeçalho com estado salvo em `localStorage`.
* **Portfólio Estruturado de P&D (`/portfolio/`):** Projetos agrupados em **P&D Regulado ANEEL**, **P&D Incentivado Lei de TICs / MCTI (Instituto Gridtech)** e **Pesquisa Acadêmica (UFC, KTH & Uppsala)** com filtros interativos por domínio e fichas técnicas.
* **Publicações com BibTeX (`/publications/`):** Catálogo organizado por capítulos, periódicos, anais de congressos e teses, com botão de cópia rápida de BibTeX em 1 clique.
* **Experiência, Governança e Currículo (`/experience/`, `/theses/`, `/talks/`, `/cv/`):** Histórico completo integrando atuação corporativa (CATI/MCTI, ISO 9001/14001/45001, WIPO PI) e trajetória acadêmica, com download direto de `pdf/Resume_Diego_Perdigao_Sousa.pdf`.

## Estrutura do Repositório

```text
├── .github/workflows/jekyll.yml   # Build & Deploy automático no GitHub Pages
├── _config.yml                    # Configurações globais, perfis e categorias
├── _data/navigation.yml           # Abas bilíngues do menu superior
├── _includes/ & _layouts/         # Componentes Liquid e tema AcademicPages customizado
├── _sass/ & assets/               # Estilos SCSS (inclui Light/Dark mode e filtros)
├── _pages/                        # Páginas principais (about, publications, portfolio, talks, theses, experience, cv)
├── _publications/                 # Artigos, capítulos de livros e teses com BibTeX
├── _portfolio/                    # 13 projetos (ANEEL, Lei de TICs/MCTI e UFC/KTH/Uppsala)
├── _talks/                        # Apresentações em congressos e seminários
├── images/                        # Avatar recortado e favicons
└── pdf/                           # Currículo em PDF (Resume_Diego_Perdigao_Sousa.pdf)
```

## Publicação no GitHub Pages

1. No repositório GitHub, acesse **Settings → Pages → Build and deployment → Source** e selecione **GitHub Actions**.
2. Cada push na branch `main` dispara automaticamente o workflow `.github/workflows/jekyll.yml` para compilar o Jekyll e publicar o site.
