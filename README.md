<div align="center">
  <a href="https://github.com/Hamalkari/chrome-extension-boilerplate" title="Webpack Chrome Extension Boilerplate">
    <img alt="Webpack Chrome Extension Boilerplate" src="https://i0.wp.com/innovation-village.com/wp-content/uploads/2019/03/Chrome-Extensions.png?fit=684%2C367&ssl=1" width="240px" />
  </a>
  <br />
  <h1>Webpack Chrome Extension Boilerplate</h1>
</div>

## Table of contents:

* [Features](#features)
* [About file structure](#about-file-structure)
  * [Src](#src)
  * [Dist](#dist)
* [Installation](#installation)
* [Development](#development)
* [Build](#build)
* [Contact](#contact)
* [License](#license)

## Features
- Simple Boilerplate without any framework.
- You can write code with es6+ syntax (using [Babel](https://github.com/babel/babel))
- You can use the Promise-based WebExtension/BrowserExt API (using [Webextension-polyfill](https://github.com/mozilla/webextension-polyfill))
- Hot reloading while you develop extension (using [webpack-chrome-extension-reloader](https://github.com/rubenspgcavalcante/webpack-chrome-extension-reloader))

## About file structure

- file **manifest.json** - just manifest.json
- folder **src/html/*.html** - Here you can add your html files (ex. popup.html, options.html). After building all files will be in **dist/html**
- folders **src/{fonts,imgs,css}/** - all your static files 
- folders **src/js/** - all your main js files (background.js, content.js, popup.js). If you want add library, add file in folder libs or install with **npm** and **add this library using es6 module** for example
```js
import 'libs/jquery.min.js'; 
```

Below you can see **src** folder and after build you get folder **dist**

### Src
```
📦src
 ┣ 📂css
 ┃ ┣ 📂libs
 ┃ ┗ 📜popup.css
 ┣ 📂fonts
 ┃ ┗ 📜example.woff
 ┣ 📂html
 ┃ ┗ 📜popup.html
 ┣ 📂imgs
 ┃ ┗ 📂icons
 ┃ ┃ ┗ 📜example.png
 ┣ 📂js
 ┃ ┣ 📂libs
 ┃ ┣ 📜background.js
 ┃ ┣ 📜content.js
 ┃ ┗ 📜popup.js
 ┗ 📜manifest.json
```
### Dist
```
📦dist
 ┣ 📂css
 ┃ ┗ 📜popup.css
 ┣ 📂fonts
 ┃ ┗ 📜example.woff
 ┣ 📂html
 ┃ ┗ 📜popup.html
 ┣ 📂imgs
 ┃ ┗ 📂icons
 ┃ ┃ ┗ 📜example.png
 ┣ 📂js
 ┃ ┣ 📜background.bundle.js
 ┃ ┣ 📜browser-polyfill.min.js
 ┃ ┣ 📜content.bundle.js
 ┃ ┗ 📜popup.bundle.js
 ┗ 📜manifest.json
```

## Installation

1. Clone the repo

```sh
git clone https://github.com/Hamalkari/chrome-extension-boilerplate.git
```
2. Install all NPM packages

```sh
npm install
```

## Development

1. Run script

```sh
npm run dev
```

2. (If you run first) Go to [chrome://extension](chrome://extension) and [load extension](https://developer.chrome.com/extensions/getstarted#unpacked) from folder `./dist`.

## Build

1. Run script and js files will be compress. Output folder `./dist`

```sh
npm run build
```

## Contact
**Ivanov Vyacheslav** - kosha.1997@bk.ru,https://vk.com/id143203503

Project Url - https://github.com/Hamalkari/chrome-extension-boilerplate

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details