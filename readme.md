# Giovanna com Bootstrap 3.3.5 em Stylus! - Simples starter com auto-injeção, GulpJs e Stylus

Rode a tarefa `gulp` e comece a trabalhar!

Comece seus projetos direto no html e nunca digite `<script src>` nem `<link href>`!

### Inclui:

- Auto-injeção de dependências ao instalar um pacote pelo bower, ou manualmente na pasta `/lib`

- Bootstrap com Stylus,

- jQuery via Bower

- Include de Partials e mini-template engine com gulp-file-includes `@@include('partials/arquivo.html')`

- LiveReload: uma vez executada `gulp` seu projeto atualiza automaticamente quando editado


# Como Utilizar

> Atenção: Você precisa ter [nodejs](http://nodejs.org/) e [gulpjs](http://gulpjs.com/) instalados.

> Atenção 2: É necessário ter alguma dependencia do bower para funcionar. (devido ao [main-bower-files](https://github.com/ck86/main-bower-files) Sugiro jquery `bower install --save jquery` )

1. `Git clone https://github.com/RcDevLabs/Giovanna.git ***nomeDaPastaDoSeuProjeto***`

2. `npm install `

3. `bower install`. Jogue arquivos .css adiconais na `/lib`

4. No terminal, rode `gulp`

5. Faça algo legal no index.html ***e salve***


> Atenção 3: Não esqueça de editar as informações do seu projeto no `package.json` e `bower.json`


# Estrutura de diretórios esperada

A pasta `./src` é a única que será editada, contendo o código-fonte do projeto.

A pasta `/src/stylus/` contém os arquivos .styl. Apenas o main.styl é processado portanto ao criar outros arquivos é necessário declarar com `@import` no main.styl

Na `./src/libs/` inclua os js, css, imagens e etc que não podem ser inseridos pelo bower. ``` ***Exemplo:*** o semantic-ui , se instalado pelo bower carrega apenas o semantic.min.js e semantic.min.css, deixando de lado importantes arquivos de fontes/icons e tema. Neste caso, insira os arquivos (que faltam, ou todos mesmo) na `/lib` ``´

A pasta `./build` é gerada pelas Gulp Tasks com código crú, porém compilado. É a pasta servida pela task `serve`

A pasta `./dist` é gerada pelo Gulp e contém arquivos de distribuição, devidamente minifcados e otimizados.


