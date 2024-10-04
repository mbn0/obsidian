---
id: ngstyle
aliases:
  - ngStyle
tags: []
---

# ngStyle

a way to apply inline css styles in angular that can be more dynamic and call functions in the code.

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  isRed: boolean = true;
  fontSize: number = 20; // Font size in pixels

  getStyles() {
    return {
      color: this.isRed ? 'red' : 'blue',
      'font-size': `${this.fontSize}px`,
      'font-weight': 'bold'
    };
  }
}
```

html:
```html
<!-- Using ngStyle for dynamic styling -->
<div [ngStyle]="getStyles()">
  This text changes color and font size!
</div>

<!-- Toggle button for changing styles -->
<button (click)="isRed = !isRed">Toggle Color</button>
<input type="number" [(ngModel)]="fontSize" placeholder="Font Size" />
```
