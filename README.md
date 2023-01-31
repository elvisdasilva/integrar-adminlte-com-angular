## Como integrar Admin LTE com Angular

Neste tutorial, você irá aprender como integrar de forma simples o Dashboard [AdminLTE](https://adminlte.io/) com o framework [Angular](https://angular.io/).

1.  Criar e configurar um novo projeto Angular
2.  Importar os styles e scripts para o projeto
3.  Criar componentes e adicionar conteúdo html
4.  Corrigir links das imagens  
     

### 1 . Criar e configurar um novo projeto Angular

*   Baixe o Admin LTE versão 3.2.0 [aqui](https://github.com/ColorlibHQ/AdminLTE/releases) e descompacte em uma pasta local.
*   Crie uma nova aplicação Angular usando o comando ng new \<app-name>
*   Abra a pasta Admin LTE que você baixou, copie as pastas dist e plugins. Vá para o diretório da sua aplicação Angular e cole-os dentro da pasta src/assets.
*   Abra o arquivo index da pasta do AdminLTE com o VS Code.
*   Abra também o seu projeto Angular com VS Code.

### 2 . Importar os styles e scripts para o projeto

*   Copie os links de importações css da seção head da página index para a seção head da página index da aplicação Angular.
*   Copie os estilos da tag \<body> do index do Admin LTE para a tag \<body> do index da aplicação Angular.
*   Copie os links de importações js antes da tag de fechamento \</body> do index do Admin LTE para a página index da aplicação Angular.
*   Para cada um dos links importados, prefixe a url com assets/ para que aponte para o local correto.

### 3\. Crie e adicione os componentes

*   Abra o arquivo app.component.html e exclua todo o conteúdo, exceto a seção \<router-outlet>\</router-outlet>.
*   Agora você pode dar uma olhada no arquivo index.html do Admin LTE e notará que existem 5 seções diferentes. Estas seções são:

_main-header –_ esta é a tag **\<nav> \</nav>**

_main-sidebar –_ esta é a tag **\<aside>\</aside>**

_content-wrapper –_ esta é uma tag **\<div> com class=”content-wrapper”**

_control-sidebar –_ esta é a tag **\<aside>\</aside> com class=”control-sidebar”**

_main-footer –_ esta é a tag **\<footer>\</footer> com class=”main-footer”**  
 

*   Agora você precisa criar esses 5 componentes com os nomes correspondentes as classes acima, para isso use o comando abaixo:

```plaintext
ng g c <nome do componente>
```

*   Depois de criar todos os cinco componentes, copie o conteúdo de cada seção do index.html do Admin LTE para o componente correspondente.
*   Finalmente, adicione todos os componentes ao arquivo app.component.html logo acima da seção \<router-outlet>\</router-outlet>.
*   Neste ponto, o conteúdo do seu app.component.html seria o mostrado abaixo:

```plaintext
<app-main-header></app-main-header>
<app-main-sidebar></app-main-sidebar>
<app-content-wrapper></app-content-wrapper>
<app-control-sidebar></app-control-sidebar>
<app-main-footer></app-main-footer>
<router-outlet></router-outlet>
```

*   Agora você pode iniciar a Aplicação usando o comando abaixo:

```plaintext
ng serve --open.
```

### 4 . Corrigir links das imagens

  
Quando a aplicação for executada, você notará que algumas imagens não estão aparecendo. Vamos consertar agora.

*   Para cada um dos componentes, localize as tags **\<img>\</img>**. Adicione o prefixo assets/ aos atributos src para que eles apontem para a pasta correta dentro da pasta assets. Através do VS Code é possível fazer essa alteração em múltiplas tags ao mesmo tempo.

Agora, você pode executar a aplicativo novamente e ver que tudo está funcionando perfeitamente bem 🙂.
