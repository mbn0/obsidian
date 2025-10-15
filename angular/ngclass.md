---
id: ngclass
aliases:
  - ngClass
tags: []
---

# ngClass

is a way to add CSS classes just like the normal html "class", but it is more costumizable.

conditions can be added and many more.

example:
```html
<!-- Dynamically adding classes using an array in `[ngClass]` -->
<div [ngClass]="['class1', class2]">
  Dynamic classes from array
</div>
```

typescript:
```ts
export class AppComponent {
  class2: string = 'class-active';
}
```
