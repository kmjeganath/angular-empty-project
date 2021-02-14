#  Angular Journey

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.13

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests //TODO: to be decided

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


#  Angular Journey

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.0.4.

<!-- vim-markdown-toc GFM -->

* [Initial Setup](#initial-setup)
* [Developer Guide](#developer-guide)
* [Style Guide](#style-guide)
* [Project structure](#project-structure)
* [Code scaffolding](#code-scaffolding)
* [Code commit messages conventional](#code-commit-messages-conventional)

<!-- vim-markdown-toc -->

## Initial Setup

You will need to be using Node 10 or later to work on the app. We recommend using [Node Version Manager](https://github.com/nvm-sh/nvm) to manage Node versions. Use a Node 10+ engine, then install and run the tests to ensure you have a working setup:

```sh
nvm use 10
npm it
```

Most simple or build-oriented tasks can be run with `npm`. However, if you are developing frontend code, you will find it helpful to install the [Angular CLI](https://angular.io/cli/):

```sh
npm i -g @angular/cli
```

## Developer Guide

1. Install dependencies:

```bash
npm install
```

2. Use the following commands to work with the code:

| Command              | Notes                                                                                                                                |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `npm run start`      | Alias for `ng serve`. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
| `npm run build`      | Build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.        |
| `npm run test`       | Run unit tests via [Karma](https://karma-runner.github.io).                                                                          |
| `npm run e2e`        | Alias for `ng e2e`. Execute the end-to-end tests via [Protractor](http://www.protractortest.org/).                                   |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|


If you get a CORS error on a regular browser, launch an insecure browser with:

Windows:
```bash
"C:\Program Files\Google\Chrome\Application\chrome.exe" --disable-web-security --user-data-dir="C:\tmpChromeSession"
```

## Style guide

HTML Semantics
- all to be followed, including heading, paragraphs, buttons, images etc

Fonts
- font-size [rem] (define fonts size in html root)
<h1>Heading 1 (2.25rem = 36px)</h1>
<h2>Heading 2 (1.875rem = 30px)</h2>
<h3>Heading 3 (1.5rem = 24px)</h3>
<h4>Heading 4 (1.25rem = 20px)</h4>
<h5>Heading 5 (1.125rem = 18px)</h5>
*source = w3schools

Layouts
- Bootstrap grid structure 

Paddings
- [rem]

Margins
- [rem]

All colors and font sizes should be maintained in theme.scss

Header
- height [%, vh]
- width [%, vw]

Additional points:
- For responsive design not use px unless we don't want the element to scale.
- Can use rem for max/min height/width for restricting container sizes.

## Project structure

```
e2e/                         end-to-end tests
src/                         project source code
|- app/                      app container
|  |- _configs/              app settings and other predefined values
|  |- _core/                 core module (singleton services and single-use components)
|   |- guards/               all guards
|   |- interceptors/         all interceptors
|   |- mocks/                mocks used for testing
|   |- services/             app services are defined
|   |- core.module.ts        core module and route import
|  |- _shared/               shared module  (common components, directives and pipes)
|  |- app.component.ts       app root component (shell)
|  |- app.module.ts          app root module definition
|  |- app-routing.module.ts  app routes
|- assets/                   app assets (images, fonts, pdfs)
|- environments/             values for various build environments
|- index.html                html entry point
|- styles                    styles folder and global style entry point
|- main.ts                   app entry point
|- polyfills.ts              polyfills needed by Angular  
+- test.ts                   unit tests entry point
```


## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.


## Code commit messages conventional

We can try following the below git commit message conventions https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines


- feat: A new feature
    ```sh
    feat: [JIRA-ID] - login feature is implemented
    ```
- fix: A bug fix
    ```sh
    fix: [JIRA-ID] - login page css is fixed
    ```
- docs: Documentation only changes
- perf: A code change that improves performance
- refactor: A code change that neither fixes a bug nor adds a feature
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- test: Adding missing tests or correcting existing tests

