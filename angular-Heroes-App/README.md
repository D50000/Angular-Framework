# AngularHeroesApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.19.

## Focal Point

- **ngOnInit()** is a **lifecycle hook**. Angular calls ngOnInit() shortly after creating a component for initialization logic.
- **[(ngModel)]**  // from '@angular/forms' two-way-binding.
- **[class.selected]**="x === y"  // for elements are selected.
- **@Input() x: X**  // input from the parent component.
- **subscribe()** // getting asynchronous API data
- constructor(**public messageService: MessageService**) { }  // Bind with Service
- **router-outlet** // router matcher component.
- Library **@angular/common/http**, **rxjs/operators**.
- **HttpClient.put()**, **HttpClient.post()**
- `<input #heroName /> <button (click)="add(heroName.value)>` // Select the input textbox.
- the pipe **|** character // for filter expression.
- `<li *ngFor="let hero of heroes$ | async" >` // AsyncPipe. The **$** is a convention that indicates heroes$ is an Observable, not an array.
