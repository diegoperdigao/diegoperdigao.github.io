# Academic Portfolio & GitHub Pages

Este repositório contém a estrutura e os arquivos estáticos do site acadêmico replicado a partir de [charlescasimiro.github.io](https://charlescasimiro.github.io/), preparado para ser adaptado e publicado como o site pessoal do pesquisador **Diego Perdigão Sousa** em [diegoperdigao.github.io](https://diegoperdigao.github.io/).

---

## 1. Engenharia Reversa e Arquitetura do Site Original

### 1.1 Stack Tecnológico
* **Estrutura:** HTML5 estático sem dependência de geradores estáticos complexos (não requer Jekyll, Hugo, Ruby ou Node.js para compilar).
* **Estilização:** CSS3 puro (`css/style.css`), baseado originalmente no tema clássico acadêmico `CSS3_four` (de `css3templates.co.uk`), com container centralizado de ~950px e tipografia em `Yanone Kaffeesatz` (`fonts/`).
* **Interatividade / Scripts:**
  * `js/jquery.js` + `js/jquery.sooperfish.js`: Gerenciador do menu dropdown multinível na barra de navegação superior.
  * `js/jquery.easing-sooper.js`: Animações suaves de abertura dos submenus.
  * `js/modernizr-1.5.min.js`: Suporte e detecção de recursos HTML5.
  * `js/image_fade.js`: Efeito de transição de imagens de cabeçalho (quando ativo).
* **Hospedagem nativa:** Compatível diretamente com o GitHub Pages servindo a raiz (`/`) do branch `main` ou `master`.

---

### 1.2 Mapa de Arquivos e Estrutura de Pastas

```text
├── index.html                   # Página inicial: Foto, Biografia, Formação (D.Sc., M.Sc.), Contato e Afiliações
├── publications.html            # Lista de publicações (Livros, Capítulos, Artigos de Periódicos, Conferências, Patentes)
├── research.html                # Linhas e projetos de pesquisa, financiamentos, parceiros e colaboradores
├── students_theses.html         # Orientações e teses/dissertações supervisionadas (ou referências acadêmicas)
├── service.html                 # Atividades profissionais: revisões para periódicos, sociedades científicas, eventos
├── misc.html                    # Notícias, prêmios, palestras e atividades diversas
├── telecommunications_book.html # Página de destaque para livro/publicação específica (opcional)
│
├── [Disciplinas / Ensino]       # Subpáginas do menu Teaching (graduação e pós-graduação)
│   ├── adaptive_filtering.html
│   ├── estimation_detection.html
│   ├── information_theory.html
│   ├── bss.html
│   ├── statistics_eng.html
│   ├── stochastic_processes.html
│   └── statistical_sp.html
│
├── [Recursos / Assets]
│   ├── css/
│   │   └── style.css            # Folha de estilo principal
│   ├── fonts/                   # Fontes web incorporadas (Yanone Kaffeesatz)
│   ├── js/                      # Bibliotecas jQuery e plugins de menu
│   ├── images/                  # Fotos de perfil, logos (UFC, ResearchGate, Scholar, etc.) e ícones
│   └── pdf/                     # PDFs de teses, currículo, slides e notas de aula
```

---

## 2. Guia de Adaptação para Diego Perdigão Sousa

### 2.1 Dados Pessoais e Links Identificados
* **Nome:** Diego Perdigão Sousa
* **Titulação:** Doutor em Engenharia de Teleinformática (D.Sc.)
* **Afiliação:** Universidade Federal do Ceará (UFC), Centro de Tecnologia, PPGETI
* **Links Principais:**
  * **Currículo Lattes:** [http://lattes.cnpq.br/3866699869645553](http://lattes.cnpq.br/3866699869645553)
  * **LinkedIn:** [https://www.linkedin.com/in/diegoperdigaosousa/](https://www.linkedin.com/in/diegoperdigaosousa/)
  * **GitHub:** [https://github.com/diegoperdigao](https://github.com/diegoperdigao)

### 2.2 Principais Alterações por Arquivo

#### A. Cabeçalho Geral (Todas as páginas `.html`)
Substitua no bloco `<div id="logo_text">`:
```html
<h1><a href="index.html">Diego Perdigão Sousa</a></h1>
<h2>Researcher & Engineer | Ph.D. in Teleinformatics</h2>
```

#### B. Barra Lateral e Badges de Perfil (`#sidebar_container`)
Em `index.html` e demais páginas, adicione o link do LinkedIn e atualize os identificadores:
```html
<div class="sidebar">
  <h3>Profiles</h3>
  <!-- Lattes CNPq -->
  <a href="http://lattes.cnpq.br/3866699869645553" target="_blank" title="Currículo Lattes">
    <b>Currículo Lattes</b>
  </a>
  <br/><br/>
  <!-- LinkedIn -->
  <a href="https://www.linkedin.com/in/diegoperdigaosousa/" target="_blank" title="LinkedIn">
    <b>LinkedIn Profile</b>
  </a>
  <br/><br/>
  <!-- GitHub -->
  <a href="https://github.com/diegoperdigao" target="_blank" title="GitHub">
    <b>GitHub Profile</b>
  </a>
</div>
```

#### C. Página Inicial (`index.html`)
1. **Foto de Perfil:**
   - Adicione sua foto na pasta `images/` (por exemplo `images/diego_perdigao.jpg`) e altere na linha da imagem:
     ```html
     <span class="left"><img src="images/diego_perdigao.jpg" alt="Diego Perdigão Sousa" height="300" width="237" /></span>
     ```
2. **Formação Acadêmica (`#Education`):**
   - **Doutorado (2024):** D.Sc. em Engenharia de Teleinformática, Universidade Federal do Ceará (UFC).
     * Título da Tese: *Leakage detection in a real water distribution network through a federated prototype-based model* (Orientador: Prof. Charles Casimiro Cavalcante, Coorientador: Prof. Carlo Fischione - KTH).
     * Link institucional da tese: [Repositório UFC](https://repositorio.ufc.br/bitstream/riufc/80329/1/2024_dpsousa.pdf).
   - **Mestrado (2019):** M.Sc. em Engenharia de Teleinformática, Universidade Federal do Ceará (UFC).
     * Título da Dissertação: *Detecção de falhas de curto-circuito em motores de indução trifásicos usando classificadores baseados em protótipos*.
     * Link institucional da dissertação: [Repositório UFC](http://repositorio.ufc.br/bitstream/riufc/49906/5/2019_dis_dpsousa.pdf).
   - **Graduação:** Bacharelado em Engenharia de Teleinformática, Universidade Federal do Ceará (UFC).
3. **Áreas de Pesquisa:**
   - Aprendizado Federado (*Federated Learning*)
   - Classificadores Baseados em Protótipos (LVQ - Learning Vector Quantization)
   - Redes de Distribuição de Água e Detecção de Vazamentos
   - Detecção de Falhas e Manutenção Preditiva (Motores de Indução)
   - Aprendizado de Máquina Aplicado a IoT e Cidades Inteligentes

#### D. Publicações (`publications.html`)
Você já possui publicações presentes no acervo original prontas para serem destacadas:
* **Capítulo de Livro (Wiley 2025):**
  * Diego P. Sousa, José M. B. da Silva Jr, Charles C. Cavalcante, and Carlo Fischione. *"A Federated Prototype-Based Model for IoT Systems: A Study Case for Leakage Detection in a Real Water Distribution Network"*. In: *Wireless Sensor Networks in Smart Environments*, Chapter 12, pp. 273-298, 2025.
* **Capítulo de Livro (Springer 2019):**
  * Diego P. Sousa, Guilherme A. Barreto, Charles C. Cavalcante, and Cláudio M. S. Medeiros. *"LVQ-type Classifiers for Condition Monitoring of Induction Motors: A Performance Comparison"*. Springer, 2019.
* **Artigo em Periódico (Water Supply 2023):**
  * Diego Sousa, Rong Du, José Mairton Barros da Silva Jr, Charles Casimiro Cavalcante, and Carlo Fischione. *"Leakage detection in water distribution networks using machine-learning strategies"*, *Water Supply*, 2023. DOI: 10.2166/ws.2023.054.
* **Conferências (CBIC, IEEE VTC, Blue Planet, etc.):**
  * Artigos no Congresso Brasileiro de Inteligência Computacional (CBIC 2019, CBIC 2025) e workshops internacionais.

---

## 3. Testando Localmente

Para visualizar e editar as páginas em sua máquina local sem precisar instalar servidores pesados:

### Opção 1: Python
No terminal PowerShell ou Prompt de Comando dentro desta pasta, execute:
```powershell
python -m http.server 8000
```
Depois abra seu navegador em `http://localhost:8000`.

### Opção 2: VS Code Live Server
Se utilizar o Visual Studio Code, basta instalar a extensão **Live Server** e clicar em **"Go Live"** no canto inferior direito.

---

## 4. Publicação no GitHub Pages

Para publicar como seu site oficial:

1. **Crie o repositório no GitHub:**
   - Acesse [github.com/new](https://github.com/new).
   - Nome do repositório: `diegoperdigao.github.io` (exatamente com seu usuário e extensão `.github.io`).
   - Mantenha-o público.

2. **Conecte e envie este código:**
   ```powershell
   git add .
   git commit -m "Initial commit: academic portfolio template replica"
   git remote add origin https://github.com/diegoperdigao/diegoperdigao.github.io.git
   git push -u origin main
   ```

3. **Verifique a ativação do GitHub Pages:**
   - No GitHub, acesse **Settings > Pages**.
   - Em **Source**, confirme que está selecionado **Deploy from a branch**, com branch **main** e pasta **/ (root)**.
   - Dentro de alguns minutos, seu site estará no ar em:
     **`https://diegoperdigao.github.io/`**

