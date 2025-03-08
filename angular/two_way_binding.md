---
id: two_way_binding
aliases:
  - two way binding
tags: []
---

# two way binding

two way binding is taking input from the user that updates the value in the [[code behind]]

dont forget to add FormsModule.

example:

file: app.component.ts
```typescript
import { Component } from '@angular/core';
import { RouterOutlet } from '@angular/router';
import { FormsModule } from '@angular/forms';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [RouterOutlet, FormsModule],
  templateUrl: './app.component.html',
  styleUrl: './app.component.css'
})
 export class AppComponent {
  title: string = 'Two-way binding example';
  inputValue: string = 'Initial value';  // Property bound to the input field
}

```

file: app.component.html
```html
<h1>{{ title }}</h1>

<!-- Two-way binding using [(ngModel)] -->
<input [(ngModel)]="inputValue" />

<p>You typed: {{ inputValue }}</p>

```

