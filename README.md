<p>
  <a href="https://conedevelopment.com/#gh-light-mode-only">
    <br/>
    <img src="./.github/cone-logo-dark.svg" alt="Cone Development" width="90">
    <br/>
    <br/>
  </a>
  <a href="https://conedevelopment.com/#gh-dark-mode-only">
    <br/>
    <img src="./.github/cone-logo-light.svg" alt="Cone Development" width="90">
    <br/>
    <br/>
  </a>
</p>

**The “Designing in the Browser Starter Kit” repository contains a simple foundation for designing in the browser. It is nothing more but a simple and opinionated starter foundation based on our experience. So feel free to modify in any way.**

It is a mix of essential tools that we like to use and necessary for working in the browser fast. This project aims to quickly design and then get the source files to integrate into other platforms like WordPress, Laravel, or Gatsby.

If you want to know why it is a good idea to design in the browser, you can read about [my thoughts on Pine](https://pineco.de/designing-in-the-browser/).

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Get Up and Running](#get-up-and-running)
- [Pug](#pug)
- [SCSS](#scss)
- [Browsersync](#browsersync)
- [Misc](#misc)
- [License](#license)

## Get Up and Running

It is easy to start a new project, but please read the following points ([Pug](#pug) [Sass](#sass) [Browsersync](#browsersync)) to understand how it works before you do it.

1. **Clone the repository.**
2. **Install the dependencies.**

    In the `package.json` file, you will find all of the dependencies to install them use the following command:

    ```shell
    npm install
    ```

3. **Run the development mode**

    To run the development mode, use the `dev` script, which does all the job (start a webserver, compile Pug and Sass). In the `package.json`, you can find the individual scripts too.

    ```shell
    npm run dev
    ```

    This script will also watch for changes in the `pug` and `assets/scss` folders.

4. **Run the production mode**
  
    Running the `prod` script, you can create compressed CSS files without .map. Also, it will compile the `pug` files too.

    ```shell
    npm run prod
    ```

## Pug

Pug (formerly Jade) is a JavaScript template engine mostly for Node. It compiles to HTML, has a simplified syntax. Easy to use, handles include (separate files like a header or footer component), can work with JSON data.

You can find the templates in the `pug/templates` folder in the root, and it will compile into the `html` folder.

Under the `pug/assets` folder, you find the `data.json` and the `mixin.pug` files. The first can contain any JSON formatted data for later use, and the second is a simple mixin for the icons. You can find an example for both in the `pug/templates/components/generic/testimonial.pug` file.

## SCSS

The project compiles the SCSS files from the `assets/sass` folder into the `assets/css` folder. We gave the same default CSS styles but feel free to remove them. The value here is the simple compiler that uses the sass-cli.

## Browsersync

Running the `npm run dev` will also start up a Browsersync server which you can share across your local network. It will automatically open the URL in your default browser with the `html/page/home.html` file.

## Misc

**HTML Beautify:** You can run your generated files through a [beautifier](https://www.npmjs.com/package/js-beautify) with the `npm run beautify` command; this is needed because sometimes the Pug pretty formatting makes a mistake (or you need another indenting).

**Sass Lint:** You can lint your SCSS files with [Stylelint](https://stylelint.io/) and [stylelint-config-sass-guidelines](https://github.com/bjankord/stylelint-config-sass-guidelines) preset with the `npm run sass-lint` command.

**Icons:** A starter kit uses a simple SVG-based icon solution. You can extend it through `assets/icon/icons.svg` file. To use the icons first, you have to include them in any Pug template (like you see it in the `home.pug`). We created an `icon` mixin with which you can easily include any icon as you see in the `testimonial.pug` file.

## License

The code is licensed under the [MIT](LICENSE).
