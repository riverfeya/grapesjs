# [GrapesJS](http://grapesjs.com)

[![Build Status](https://travis-ci.org/artf/grapesjs.svg?branch=master)](https://travis-ci.org/artf/grapesjs)
[![Chat](https://img.shields.io/badge/chat-discord-7289da.svg)](https://discord.gg/QAbgGXq)
[![CDNJS](https://img.shields.io/cdnjs/v/grapesjs.svg)](https://cdnjs.com/libraries/grapesjs)
[![npm](https://img.shields.io/npm/v/grapesjs.svg)](https://www.npmjs.com/package/grapesjs)
[![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=QksxaStYaGI3eE5VMDlPTEh0Z3hYOXEwRWNMc1ZYT0lNbEJxMWdOZWFDZz0tLWlqcFVWb05PMmlQMmU3emFIZkFNWVE9PQ==--e89345be5e303d515276e3accd6f1316dfa857ab)](https://www.browserstack.com/automate/public-build/QksxaStYaGI3eE5VMDlPTEh0Z3hYOXEwRWNMc1ZYT0lNbEJxMWdOZWFDZz0tLWlqcFVWb05PMmlQMmU3emFIZkFNWVE9PQ==--e89345be5e303d515276e3accd6f1316dfa857ab)


<p align="center"><img src="http://grapesjs.com/img/grapesjs-front-page-m.jpg" alt="GrapesJS" width="500" align="center"/></p>


GrapesJS это бесплатный и c открытым исходным кодом Web Builder Framework который помогает создавать шаблоны HTML, быстрее и проще, доставляться на сайтах, в новостных рассылках или мобильных приложениях. В основном, GrapesJS был разработан для использования внутри [CMS] чтобы ускорить создание динамических шаблонов. Чтобы лучше понять эту концепцию, проверьте изображение ниже

<br/>
<p align="center"><img src="http://grapesjs.com/img/gjs-concept.png" alt="GrapesJS - Style Manager" height="400" align="center"/></p>
<br/>

Вообще любой 'template system', что вы найдете в различных приложениях, таких как CMS, состоит из **structure** (HTML), **style** (CSS) и **variables**, которые затем заменяются другими шаблонами и содержимым на стороне сервера и отображаются на клиенте.

Это демо показывает примеры того, чего можно достичь:
Webpage Demo - http://grapesjs.com/demo.html
Newsletter Demo - http://grapesjs.com/demo-newsletter-editor.html





## Table of contents

- [GrapesJS](#grapesjs)
  - [Table of contents](#table-of-contents)
  - [Features](#features)
  - [Download](#download)
  - [Usage](#usage)
  - [Development](#development)
  - [Documentation](#documentation)
  - [API](#api)
  - [Testing](#testing)
  - [Plugins](#plugins)
    - [Extensions](#extensions)
    - [Presets](#presets)
  - [Support](#support)
  - [License](#license)




## Features

| Blocks | Style Manager | Layer Manager |
|--|--|--|
|<img  src="http://grapesjs.com/img/sc-grapesjs-blocks-prp.jpg"  alt="GrapesJS - Block Manager"  height="400"  align="center"/>|<img  src="http://grapesjs.com/img/sc-grapesjs-style-2.jpg"  alt="GrapesJS - Style Manager"  height="400"  align="center"/>|<img  src="http://grapesjs.com/img/sc-grapesjs-layers-2.jpg"  alt="GrapesJS - Layer Manager"  height="400"  align="center"/>|

| Code Viewer | Asset Manager |
|--|--|
|<img  src="http://grapesjs.com/img/sc-grapesjs-code.jpg"  alt="GrapesJS - Code Viewer"  height="300"  align="center"/>|<img  src="http://grapesjs.com/img/sc-grapesjs-assets-1.jpg"  alt="GrapesJS - Asset Manager"  height="250"  align="center"/>|

* Local and remote storage

* Default built-in commands (в основном для создания и управления различными компонентами)





## Download

* CDNs
  * UNPKG (resolves to the latest version)
    * `https://unpkg.com/grapesjs`
    * `https://unpkg.com/grapesjs/dist/css/grapes.min.css`
  * CDNJS (replace `X.X.X` with the current version)
    * `https://cdnjs.cloudflare.com/ajax/libs/grapesjs/X.X.X/grapes.min.js`
    * `https://cdnjs.cloudflare.com/ajax/libs/grapesjs/X.X.X/css/grapes.min.css`
* NPM
  * `npm i grapesjs`
* GIT
  * `git clone https://github.com/artf/grapesjs.git`

Для целей разработки вы должны следовать инструкциям ниже.





## Usage

```html
<link rel="stylesheet" href="path/to/grapes.min.css">
<script src="path/to/grapes.min.js"></script>

<div id="gjs"></div>

<script type="text/javascript">
  var editor = grapesjs.init({
      container : '#gjs',
      components: '<div class="txt-red">Hello world!</div>',
      style: '.txt-red{color: red}',
  });
</script>
```

Вы также можете получить содержимое непосредственно из элемента с помощью свойства `fromElement` 

```html
<div id="gjs">
  <div class="txt-red">Hello world!</div>
  <style>.txt-red{color: red}</style>
</div>

<script type="text/javascript">
  var editor = grapesjs.init({
      container : '#gjs',
      fromElement: true,
  });
</script>
```

Для более практического примера я предлагаю посмотреть код внутри этой демонстрации: http://grapesjs.com/demo.html


## Development

GrapesJS использует [Webpack](https://github.com/webpack/webpack) в качестве модуля сборки [Babel](https://github.com/babel/babel) как сборщик.

Клонируйте репозиторий и установите все необходимые зависимости

```sh
$ git clone https://github.com/artf/grapesjs.git
$ cd grapesjs
$ npm i
```

Запустите сервер разработки

```sh
$ npm start
```

После запуска сервера разработки вы сможете попасть на демонстрационную страницу (eg. `http://localhost:8080`)





## Documentation

Проверьте руководство по началу работы здесь: [Documentation]





## API

Ссылки на API можно найти здесь: [API-Reference]





## Testing

```sh
$ npm test
```





## Plugins

### Extensions
* [grapesjs-plugin-export](https://github.com/artf/grapesjs-plugin-export) - Экспорт GrapesJS шаблонов в архив zip
* [grapesjs-plugin-filestack](https://github.com/artf/grapesjs-plugin-filestack) - Добавляет Filestack uploader в Asset Manager
* [grapesjs-plugin-ckeditor](https://github.com/artf/grapesjs-plugin-ckeditor) - Заменяет встроенный RTE на CKEditor
* [grapesjs-aviary](https://github.com/artf/grapesjs-aviary) - Добавляет Aviary Image Editor (отклонен, используйте плагин ниже)
* [grapesjs-tui-image-editor](https://github.com/artf/grapesjs-tui-image-editor) - GrapesJS TOAST UI Image Editor
* [grapesjs-blocks-basic](https://github.com/artf/grapesjs-blocks-basic) - Базовый набор блоков
* [grapesjs-plugin-forms](https://github.com/artf/grapesjs-plugin-forms) - Набор компонентов формы и блоков
* [grapesjs-navbar](https://github.com/artf/grapesjs-navbar) - Простой компонент панели навигации
* [grapesjs-component-countdown](https://github.com/artf/grapesjs-component-countdown) - Простой компонент обратного отсчета
* [grapesjs-style-gradient](https://github.com/artf/grapesjs-style-gradient) - Добавляет `gradient` type input в Style Manager
* [grapesjs-style-filter](https://github.com/artf/grapesjs-style-filter) - Добавляет `filter` type input в Style Manager
* [grapesjs-style-bg](https://github.com/artf/grapesjs-style-bg) - Full-stack тип свойства стиля фона, с возможностью добавления изображений, цветов и градиентов
* [grapesjs-blocks-flexbox](https://github.com/artf/grapesjs-blocks-flexbox) - Добавляет блок flexbox
* [grapesjs-lory-slider](https://github.com/artf/grapesjs-lory-slider) - Слайдер компонент с помощью [lory](https://github.com/meandmax/lory)
* [grapesjs-tabs](https://github.com/artf/grapesjs-tabs) - Компонент простых вкладок
* [grapesjs-tooltip](https://github.com/artf/grapesjs-tooltip) - Простой, только CSS, компонент всплывающей подсказки для GrapesJS
* [grapesjs-custom-code](https://github.com/artf/grapesjs-custom-code) - Вставить пользовательский код
* [grapesjs-touch](https://github.com/artf/grapesjs-touch) - Включить сенсорную поддержку
* [grapesjs-indexeddb](https://github.com/artf/grapesjs-indexeddb) - Обертка для храненилища IndexedDB
* [grapesjs-firestore](https://github.com/artf/grapesjs-firestore) - Обертка для храненилища [Cloud Firestore](https://firebase.google.com/docs/firestore)
* [grapesjs-parser-postcss](https://github.com/artf/grapesjs-parser-postcss) - Пользовательский анализатор CSS для GrapesJS использующий [PostCSS](https://github.com/postcss/postcss)
* [grapesjs-typed](https://github.com/artf/grapesjs-typed) - Компонент печатной машинки на основе Typed.js 

### Presets
* [grapesjs-preset-webpage](https://github.com/artf/grapesjs-preset-webpage) - Webpage Builder
* [grapesjs-preset-newsletter](https://github.com/artf/grapesjs-preset-newsletter) - Newsletter Builder
* [grapesjs-mjml](https://github.com/artf/grapesjs-mjml) - Newsletter Builder with MJML components


Узнайте больше о плагинах здесь: [Creating plugins](https://github.com/artf/grapesjs/wiki/Creating-plugins)





## Support

Если вам нравится проект, поддержите его пожертвованием на ваш выбор или станьте спонсором / спонсором через [Open Collective](https://opencollective.com/grapesjs)

[![PayPalMe](http://grapesjs.com/img/ppme.png)](https://paypal.me/grapesjs)
[![Bitcoin](https://user-images.githubusercontent.com/11614725/52977952-87235f80-33cf-11e9-9607-7a9a354e1155.png)](https://commerce.coinbase.com/checkout/fc90b940-558d-408b-a166-28a823c98173)

<a href="https://opencollective.com/grapesjs/sponsors/0/website"><img src="https://opencollective.com/grapesjs/sponsors/0/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/1/website"><img src="https://opencollective.com/grapesjs/sponsors/1/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/2/website"><img src="https://opencollective.com/grapesjs/sponsors/2/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/3/website"><img src="https://opencollective.com/grapesjs/sponsors/3/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/4/website"><img src="https://opencollective.com/grapesjs/sponsors/4/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/5/website"><img src="https://opencollective.com/grapesjs/sponsors/5/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/6/website"><img src="https://opencollective.com/grapesjs/sponsors/6/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/7/website"><img src="https://opencollective.com/grapesjs/sponsors/7/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/8/website"><img src="https://opencollective.com/grapesjs/sponsors/8/avatar"></a>
<a href="https://opencollective.com/grapesjs/sponsors/9/website"><img src="https://opencollective.com/grapesjs/sponsors/9/avatar"></a>

<a href="https://opencollective.com/grapesjs/backers/0/website"><img src="https://opencollective.com/grapesjs/backers/0/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/1/website"><img src="https://opencollective.com/grapesjs/backers/1/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/2/website"><img src="https://opencollective.com/grapesjs/backers/2/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/3/website"><img src="https://opencollective.com/grapesjs/backers/3/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/4/website"><img src="https://opencollective.com/grapesjs/backers/4/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/5/website"><img src="https://opencollective.com/grapesjs/backers/5/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/6/website"><img src="https://opencollective.com/grapesjs/backers/6/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/7/website"><img src="https://opencollective.com/grapesjs/backers/7/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/8/website"><img src="https://opencollective.com/grapesjs/backers/8/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/9/website"><img src="https://opencollective.com/grapesjs/backers/9/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/10/website"><img src="https://opencollective.com/grapesjs/backers/10/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/11/website"><img src="https://opencollective.com/grapesjs/backers/11/avatar"></a>
<a href="https://opencollective.com/grapesjs/backers/12/website"><img src="https://opencollective.com/grapesjs/backers/12/avatar"></a>

<br>

[![BrowserStack](https://user-images.githubusercontent.com/11614725/39406324-4ef89c40-4bb5-11e8-809a-113d9432e5a5.png)](https://www.browserstack.com)<br/>
Thanks to [BrowserStack](https://www.browserstack.com) for providing us browser testing services


## License

BSD 3-clause


[Documentation]: <https://grapesjs.com/docs/>
[API-Reference]: <https://grapesjs.com/docs/api/>
[CMS]: <https://it.wikipedia.org/wiki/Content_management_system>
