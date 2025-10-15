---
id: property_binding_in_angular
aliases:
  - property binding in angular
tags: []
---

# Note : Check [[Signals]] for new way
# property binding in angular

declaring a variable in typscript then using it in the html.

example:

file: app.component.ts
```ts
import { Component } from '@angular/core';
import { RouterOutlet } from '@angular/router';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [RouterOutlet],
  templateUrl: './app.component.html',
  styleUrl: './app.component.css'
})
export class AppComponent {
  title: string = 'task1frontend';
  imgsrc: string = 'https://upload.wikimedia.org/wikipedia/commons/1/1c/Emblem_of_Kuwait.svg'
}
```

file: app.component.html
```html
<router-outlet> </router-outlet>
{{title}}
	
<h1 [innerHTML]= "title"></h1>
  <img [src] = "imgsrc">

```

