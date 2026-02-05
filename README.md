# AGC — Agência Criativa

Site institucional da **AGC (Agência Criativa)**, apresentando soluções digitais ágeis para negócios: sites, landing pages, lojas on-line e e-commerce.

---

## Sobre o projeto

Landing page responsiva que apresenta a agência, seus serviços, depoimentos de clientes e um formulário de contato. O foco é em agilidade, eficiência e inovação nas soluções digitais.

---

## Estrutura do site

| Seção | Descrição |
|-------|-----------|
| **Header** | Logo, nome da agência e menu de navegação (Sobre, Serviços, Depoimentos, Contato) |
| **Sobre** | Proposta de valor e diferenciais da AGC |
| **Serviços** | Cards com: Sites, Landing Pages, Lojas On-line e E-commerce |
| **Depoimentos** | Citações de clientes (Moda Ágil, Tech Creators) |
| **Contato** | Formulário com Nome, E-mail e Mensagem |

---

## Tecnologias

- **HTML5** — estrutura semântica
- **SASS** — estilos com variáveis, mixins e partials
- **CSS** — gerado a partir do SASS (`css/styles.css`)
- **Google Fonts** — Inter, Saira e Varela

---

## Requisitos do sistema

Para visualizar e desenvolver o projeto:

| Requisito | Descrição |
|-----------|-----------|
| **Navegador** | Qualquer navegador moderno (Chrome, Firefox, Edge, Safari) com suporte a HTML5 e CSS3 |
| **Servidor local** (opcional) | Python 3.x ou Node.js para servir os arquivos e evitar problemas com CORS/caminhos |
| **Sass** (opcional) | Necessário apenas se for alterar os arquivos `.scss`; instalar com `npm install -g sass` ou usar [Dart Sass](https://sass-lang.com/install) |
| **Git** | Para clonar o repositório e versionar alterações |

Não é obrigatório ter Node.js, Python ou Sass apenas para abrir o `index.html` no navegador.

---

## Estrutura de arquivos

```
AGC-creative/
├── index.html          # Página principal
├── css/
│   ├── styles.css      # CSS compilado
│   └── styles.css.map  # Source map do SASS
├── img/
│   ├── logo1.png       # Logo do header
│   └── logo2.jpg
├── sass/
│   ├── styles.scss     # Entrada principal (importa os partials)
│   ├── _variaveis.scss # Cores, fontes, espaçamentos
│   ├── _base.scss      # Reset e estilos globais
│   ├── _componentes.scss # Botões e componentes
│   ├── _mixins.scss    # Mixins (flex, nav)
│   └── _layout.scss    # Layout responsivo (breakpoints)
└── README.md
```

---

## Design responsivo

O layout se adapta em três faixas de largura:

| Breakpoint | Comportamento |
|------------|----------------|
| **≤ 600px** | Coluna, título do header oculto, grid 2 colunas nos serviços |
| **601px – 900px** | Header em linha (sem título), formulário em linha |
| **≥ 901px** | Layout completo com header, navegação e formulário em linha |

---

## Como usar

### Visualizar o site

Abra o arquivo `index.html` no navegador ou use um servidor local:

```bash
# Exemplo com Python
python -m http.server 8000

# Exemplo com Node (npx serve)
npx serve .
```

Acesse `http://localhost:8000` (ou a porta indicada).

### Compilar o SASS

Se alterar arquivos em `sass/`, recompile para atualizar `css/styles.css`:

```bash
# Com SASS instalado globalmente
sass sass/styles.scss css/styles.css

# Ou com watch para recompilar ao salvar
sass --watch sass/styles.scss:css/styles.css
```

**Requisito:** [Sass](https://sass-lang.com/install) instalado (`npm install -g sass` ou via bundler).

---

## Personalização

- **Cores e tipografia:** edite `sass/_variaveis.scss`
- **Estilos globais:** `sass/_base.scss`
- **Componentes (botões, etc.):** `sass/_componentes.scss`
- **Layout e breakpoints:** `sass/_layout.scss`
- **Utilitários (flex, nav):** `sass/_mixins.scss`

---

## Observações

- O formulário de contato é apenas front-end; não envia dados para servidor. Para envio real, é necessário integrar com backend ou serviço (ex.: Formspree, API própria).
- A imagem do logo está referenciada como `/img/logo1.png`; em alguns ambientes pode ser necessário usar caminho relativo `img/logo1.png`.

---

## Licença

Uso conforme definido pelo projeto AGC-creative.
