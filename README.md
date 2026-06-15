# LabES Website

Este repositorio contem o site institucional do LabES (Laboratorio de Engenharia de Software), vinculado ao ICMC-USP.

O projeto apresenta informacoes sobre o laboratorio, sua historia, oportunidades para alunos, materiais de apoio como o Manual do Aluno e uma pagina dedicada ao CAEd. A base visual foi adaptada a partir do template `College`, da BootstrapMade, e customizada para o contexto do laboratorio.

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Bootstrap 5
- Bibliotecas front-end em `assets/vendor`
- PHP simples para servir a pagina inicial e suportar endpoints de formulario

## Estrutura do projeto

- `index.html`: pagina principal do site
- `index.php`: entrada alternativa que serve o conteudo de `index.html`
- `students-life.html`: pagina "Manual do Aluno"
- `news.html`: pagina institucional do CAEd
- `assets/`: imagens, estilos, scripts e bibliotecas de terceiros
- `forms/contact.php`: endpoint PHP para envio de formulario

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


### Opcao recomendada: servidor PHP embutido

Use esta opcao se voce quiser acessar a raiz do projeto por `index.php`.

```bash
php -S localhost:8000
```

Depois, abra no navegador:

```text
http://localhost:8000
```

### Alternativa: servidor estatico com Python

Se o objetivo for apenas visualizar o front-end, voce pode usar um servidor estatico:

```bash
python -m http.server 8000
```

Depois, abra:

```text
http://localhost:8000/index.html
```

## Observacoes importantes

- O site pode ser aberto diretamente pelo navegador, mas usar um servidor local evita problemas com caminhos relativos e facilita os testes.
- O formulario em `forms/contact.php` depende da biblioteca `assets/vendor/php-email-form/php-email-form.php`, que nao esta presente neste repositorio. Sem essa biblioteca e sem configurar um endereco de e-mail real, o envio de mensagens nao funcionara.
- Parte do conteudo original do template ainda existe em paginas auxiliares. Antes de publicar novas alteracoes, vale revisar titulos, textos e metadados que ainda mencionam o template original.
