# Angular-Framework

Angular is a Web MVC framework that base on the TypeScript developed by Google.
There are list of useful example below.

## Setup Environment & tools

1. Install editor [Visual Studio code](https://code.visualstudio.com/).
2. Download the **[Node.js®](https://nodejs.org/en/)**.
3. Install node.js (node include **NPM**).
4. `npm install -g @angular/cli` to install the **Angular CLI**.
5. `ng new my-app` to create a new project.
6. Go the the folder `cd my-app` and start the local server `ng serve --open`.
7. Install develop tool [Augury](https://augury.rangle.io/).

## Useful examples

- Official Quick Start project: [https://stackblitz.com/edit/angular-yfujul](https://stackblitz.com/edit/angular-yfujul)
- Heroes App (data-driven application): [https://stackblitz.com/angular/ygvdxjekeba](https://stackblitz.com/angular/ygvdxjekeba)

## Running Server

1. ```ng serve``` to run the server first.
```
..... 
webpack: Compiled successfully.
```
2. ```Ctrl + z``` to stop the job and check the number.
```
^Z
[1]+  Stopped                 npm run remote
```
3. ```bg %1``` to run in background and ```fg %1``` to run at foreground.

## Lifecycle Hooks

![](https://github.com/D50000/Angular-Framework/blob/master/life%20cycle.png)

- **ngOnChanges**  − When the value of a data bound property changes, then this method is called.
- **ngOnInit**  − This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens.
- **ngDoCheck**  − This is for the detection and to act on changes that Angular can't or won't detect on its own.
- **ngAfterContentInit**  − This is called in response after Angular projects external content into the component's view.
- **ngAfterContentChecked**  − This is called in response after Angular checks the content projected into the component.
- **ngAfterViewInit**  − This is called in response after Angular initializes the component's views and child views.
- **ngAfterViewChecked**  − This is called in response after Angular checks the component's views and child views.
- **ngOnDestroy**  − This is the cleanup phase just before Angular destroys the directive/component.
