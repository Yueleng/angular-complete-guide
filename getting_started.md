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