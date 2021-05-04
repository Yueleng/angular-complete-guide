# Getting Started

## What is Angular

- Angular is a `Javascript Framework` which allows you to create reactive `Single-Page-Applications` (SPAs).

## Understading Angular Versioning

- AngularJS(Angular 1): Angular one `was` a big new thing back then, it also had some issues that could lead to worse performance and bigger applications.

- Angular 2 - current version(Complete re-write from Angular 1) are similar and new version was release very 6 months with minor changes and updates, i.e. small, incremental, backwards-compatible changes. This course will base on current version of Angular, we simply call it Angular (without JS)

- update npm: Run `[sudo] npm install -g npm` (sudo is only required on Mac/ Linux)

- updating the CLI:
  - `[sudo] npm uninstall -g angular-cli @angular/cli`
  - `npm cache verify`
  - `npm install -g @angular/cli`

## Common issues & solutions

- Creation of a new project takes forever (longer than 3 minutes)

  - That happens on Windows from time to time => Try running the command line as administrator

- You get an EADDR error (Address already in use)

  - You might already have another ng serve process running - make sure to quit that or use `ng serve --port ANOTHERPORT` to serve your project on a new port.

- My changes are not reflected in the browser (App is not compiling)
  - Check if the window running `ng serve` displays an error. If that's not the case, make sure you're using the latest CLI version and try restarting your CLI

## Install angular

- `npm install -g @angular/cli`

## Create your first angular project

- `cd goto/your/path/folder`
- `ng new angular-complete-guide`
- `cd ng new angular-complete-guide`
- `ng serve`

## Section Notes

- Angular uses `Typescript` which is a superset of javascript and is compiled down to Javascript in the end by the workflow. Typescript has more features than vanilla JS (e.g. Types, Classes, Interfaces, ...) It ensures you to write more robust code. It's not run in browser, and should be compiled to JS by ts compiler.
- in `app.component.ts`:

  ```ts
  @Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
  })
  ```

  the `app-root` corresponds to the `app-root` html tag when rendered in the browser, consistent with `<app-root></app-root>` in the `/src/index.html` file.

- import modules in `app.module.ts`: `import { FormsModule } from '@angular/forms'`. In this file.

- data binding

  ```html
  <input type="text" [(ngModel)]="name" />
  <p>{{name}}</p>
  ```

- Bootstrap: In this course, we will work with Bootstrap CSS to deal with CSS.
  - `npm install bootstrap jquery`
  - Open the `angular.json` file and add the file paths of Bootstrap CSS and JS files as well as jQuery to the `styles` and `scripts` arrays under the `build` target:
  ```json
  "architect": {
  "build": {
    [...],
    "styles": [
      "src/styles.css",
        "node_modules/bootstrap/dist/css/bootstrap.min.css"
      ],
      "scripts": [
        "node_modules/jquery/dist/jquery.min.js",
        "node_modules/bootstrap/dist/js/bootstrap.min.js"
      ]
    },
  ```

- Enable/Disable `strict mode` in `tsconfig.json` -> `strict:false/true`