# LabES Website

Este repositorio contem o site institucional do LabES (Laboratorio de Engenharia de Software), vinculado ao ICMC-USP.

O projeto apresenta informacoes sobre o laboratorio, sua historia, oportunidades para alunos, materiais de apoio como o Manual do Aluno e uma pagina dedicada ao CAEd. A base visual foi adaptada a partir do template `College`, da BootstrapMade, e customizada para o contexto do laboratorio.

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Bootstrap 5
- Bibliotecas front-end em `assets/vendor`

## Estrutura do projeto

O site usa URLs limpas (sem `.html`): cada pagina fica em uma pasta com seu `index.html`,
servido pelo GitHub Pages como `/pasta/`.

- `index.html`: pagina inicial (`/`)
- `manual-do-aluno/index.html`: pagina "Manual do Aluno" (`/manual-do-aluno/`)
- `caed/index.html`: pagina institucional do CAEd (`/caed/`)
- `orientadores/index.html`: lista de orientadores (`/orientadores/`)
- `orientador/index.html`: perfil individual do orientador (`/orientador/?id=...`)
- `404.html`: pagina de erro do GitHub Pages (usa caminhos absolutos)
- `assets/`: imagens, estilos, scripts e bibliotecas de terceiros
  - `assets/data/orientadores.json`: dados dos orientadores (carregados por `assets/js/orientadores.js`)

## Como clonar o projeto

Se voce usa SSH no GitHub:

```bash
git clone git@github.com:labes-caed-ICMC-USP/labes-website.git
cd labes-website
```

Se preferir HTTPS:

```bash
git clone https://github.com/labes-caed-ICMC-USP/labes-website.git
cd labes-website
```

## Como executar o projeto

O site e totalmente estatico. Sirva a partir da **raiz do repositorio** para que as URLs
limpas (`/manual-do-aluno/`, `/caed/`, etc.) funcionem como no GitHub Pages:

```bash
python -m http.server 8000
```

Depois, abra no navegador:

```text
http://localhost:8000/
```

E navegue por `http://localhost:8000/manual-do-aluno/`, `/caed/`, `/orientadores/`.

> Abrir os arquivos diretamente pelo navegador (`file://`) nao funciona bem: o
> carregamento dos orientadores depende de `fetch` e exige um servidor HTTP.

## Observacoes importantes

- As paginas em pastas usam caminhos relativos `../assets/...`; a `index.html` (raiz) usa
  `assets/...`. Mantenha esse padrao ao criar novas paginas em pastas.
- O `assets/js/orientadores.js` so e carregado pelas paginas `/orientadores/` e
  `/orientador/` (ambas em pasta), por isso assume profundidade 1 (`../`).
