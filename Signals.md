Signals are a new reactivity model in Angular introduced in Angular 16, they are
# Signal binding

Only re-renders what changed. 

```ts
Import {Signal} from '@angular/core'

@Component({
template: 
<p>Count: {{ count() }} </p>
})
export class Name{
count = signal(0);
}
```