---
id: template_reference_variable
aliases:
  - template reference variable
tags: []
---

# template reference variable

template reference variable is a way to reference an element or a component within the template without defining it in the code behind(aka without creating a class).

example with template reference variable:
```html
<input #myInput type="text" placeholder="Enter your name" />

<!-- Use the reference variable inside the template -->
<button (click)="logValue(myInput.value)">Log Input Value</button>

<p>You entered: {{ myInput.value }}</p>
```

the function logValue is created as follows:
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  standalone: true,
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  logValue(value: string): void {
    console.log('Input value:', value);
  }
}
```


