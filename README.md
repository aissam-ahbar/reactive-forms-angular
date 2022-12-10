# Angular Reactive forms

Create beautiful reactive forms with Angular.

## Import reactive form module in App Module

```ts
# app.module.ts
@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule, ReactiveFormsModule],
  providers: [],
  bootstrap: [AppComponent],
})
export class AppModule {}
```

## Create form on an input for example with a submit button

```ts
# app.component.ts
export class AppComponent {
  inputControl = new FormControl();

  submit() {
    // make a call to your backend
    console.log(this.inputControl);
  }
}
```

## Set up your HTML Template with submit button

```html
<input type="text" [formControl]="inputControl" />
<button type="submit" (click)="submit()">SUBMIT FORM</button>
```
