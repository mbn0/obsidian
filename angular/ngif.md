---
id: ngif
aliases:
  - ngIf
tags: []
---

# ngIf

affects the visibility of the elements

example:

html:
```html
<button (click)="toggleVisibility()">Toggle Visibility</button>

<div *ngIf="isVisible">
  This content is visible!
</div>
```

ts:
```ts
export class AppComponent {
  isVisible: boolean = true;

  toggleVisibility() {
    this.isVisible = !this.isVisible; // Toggles the visibility
  }
}
```

you can also add en else clause to handle cases when the condition is false.

example with else:
```ts
<div *ngIf="isVisible; else noContent">
  This content is visible!
</div>
<ng-template #noContent>
  This content is hidden!
</ng-template>
```
