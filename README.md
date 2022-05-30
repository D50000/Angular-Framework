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
  
|  #  | Hooks  | Purpose  | Timing |
|  ---- | ---- | ---- | ---- |
| 2 | **ngOnChanges** | When the value of a data bound property changes, then this method is called. | It will call once before ngOnInit |
| 3 | **ngOnInit** | This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens. | It excute  after the first time call ngOnChanges and it just happened once time. |
| 4 | **ngDoCheck** | This is for the detection and to act on changes that Angular can't or won't detect on its own. | Run for Angular update detection. The very first run will after the ngOnChanges, ngOnInit. |
| 5 | **ngAfterContentInit** | This is called in response after Angular projects external content into the component's view. | Just runs once after the first ngDoCheck. |
| 6 | **ngAfterContentChecked** | This is called in response after Angular checks the content projected into the component. | It calls after ngAfterContentInit and after every ngDoCheck. |
| 7 | **ngAfterViewInit** | This is called in response after Angular initializes the component's views and child views. | Just runs once after the first ngAfterContentChecked. |
| 8 | **ngAfterViewChecked** | This is called in response after Angular checks the component's views and child views. | It calls after ngAfterViewInit and after every ngAfterContentChecked. |
| 9 | **ngOnDestroy** | This is the cleanup phase just before Angular destroys the directive/component. | Before Angular destory component and directive. |

## Coding Convention

### Import order for all .ts files, relative path
  1. Angular related
  2. Companies' projects related (our companies’ stuff with @)
  3. Project related (current project with @)
  4. Relative path of our files in this project
  5. Other libraries  
  
![](https://github.com/D50000/Angular-Framework/blob/master/Angular%20convention%20import%20order.png)

### Class members, methods order
1. Decorator: @ViewChild → @Input → @Output
2. Modyfier: Public property → private property
3. Getter: Public getter → private getter
4. Constructor
5. Lifecycle: ngOnChanges → ngOnInit → ngAfterViewInit
6. Function: public function, private function

#### Useful Plugin
- [Angular Material](https://material.angular.io/)
- [Nx & Angular](https://nx.dev/getting-started/intro)
