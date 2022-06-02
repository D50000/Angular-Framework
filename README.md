# [Angular-Framework](https://angular.io/docs)

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

## Angular CLI

- Run the server in local or remote VM.

```
$ ng serve --host 0.0.0.0 --port 4200
```

- `Ctrl + c` stop and cancel the job/server. `Ctrl + z` to pause/hold the job/server and check the number.

```
# Kill the server
^c

# Pause the server and it show the id.
^z
[1]+  Stopped               npm run remote
```

- `bg %N` to run in background and `fg %N` to run at foreground.

```
# Number is [1]
$ bg %1
$ fg %1
```

- Build the project.

```
# Run build and get the compiled result in ./dist/*
$ ng build --configuration=production
```

## Lifecycle Hooks

![](https://github.com/D50000/Angular-Framework/blob/master/life%20cycle.png)

| #   | Hooks                     | Purpose                                                                                                                               | Timing                                                                                     |
| --- | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 2   | **ngOnChanges**           | When the value of a data bound property changes, then this method is called.                                                          | It will call once before ngOnInit                                                          |
| 3   | **ngOnInit**              | This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens. | It execute after the first time call ngOnChanges and it just happened ***once*** time.           |
| 4   | **ngDoCheck**             | This is for the detection and to act on changes that Angular can't or won't detect on its own.                                        | Run for Angular update detection. The very first run will after the ngOnChanges, ngOnInit. |
| 5   | **ngAfterContentInit**    | This is called in response after Angular projects external content into the component's view.                                         | Just runs ***once*** after the first ngDoCheck.                                                  |
| 6   | **ngAfterContentChecked** | This is called in response after Angular checks the content projected into the component.                                             | It calls after ngAfterContentInit and after every ngDoCheck.                               |
| 7   | **ngAfterViewInit**       | This is called in response after Angular initializes the component's views and child views.                                           | Just runs ***once*** after the first ngAfterContentChecked.                                      |
| 8   | **ngAfterViewChecked**    | This is called in response after Angular checks the component's views and child views.                                                | It calls after ngAfterViewInit and after every ngAfterContentChecked.                      |
| 9   | **ngOnDestroy**           | This is the cleanup phase just before Angular destroys the directive/component.                                                       | Before Angular destroy component and directive.                                            |

## Data Binding

- [Binding to a property](https://angular.io/guide/property-binding#binding-to-a-property)

```Html
<!-- Assignment as a dynamic expression. -->
<img alt="item" [src]="itemImageUrl">

<!-- String literal to that static value. -->
<app-item-detail childItem="parentItem"></app-item-detail>
```

- [Bind values between components](https://angular.io/guide/property-binding#bind-values-between-components)

```Html
<!-- component.html -->
<!-- 1. Data pass through parent to children -->
<app-item-detail [childItem]="parentItem"></app-item-detail>

<!-- 2. Data emit through children to parent -->
<div (open)="onOpen($event)" (close)="onClose($event)"></div>
```

```TypeScript
// component.ts
// 1. Input data
@Input() childItem = [1,2,3];

// 2. Emit binding function in children
@Output() open: EventEmitter<any> = new EventEmitter();
@Output() close: EventEmitter<any> = new EventEmitter();
toggle() {
    if (this.!isOpen) {
      this.open.emit({a:1, b:2});
    } else {
      this.close.emit({a:1, b:2});
    }
  }
```

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
2. Modifier: Public property → private property
3. Getter: Public getter → private getter
4. Constructor
5. Lifecycle: ngOnChanges → ngOnInit → ngAfterViewInit
6. Function: public function, private function

#### Useful Plugin

- [Angular Material](https://material.angular.io/)
- [Nx & Angular](https://nx.dev/getting-started/intro)
- [RX.JS](https://rxjs.dev/guide/overview)
- [SCSS](https://sass-lang.com/guide)
