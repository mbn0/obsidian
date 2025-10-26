
Content projection in Angular is when you want a child component to show content decided by the parent component, 

## example 

Child Component
```html
<div class="card">
  <h3>Title of card</h3>
  <ng-content></ng-content>  <!-- Parent content will go here -->
</div>

```
Parent Component:
```html
<app-card>
  <p>This paragraph comes from the parent component.</p>
</app-card>
```