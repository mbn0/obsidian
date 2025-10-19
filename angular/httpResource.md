
# Description

A new way to use HttpClient.
it provides everything as [[Signals]]

it is used primarily for GET operations, so you still have to use HttpClient Directly.
# example usage
```ts
import { httpResource } from '@angular/common/http';

class MyComponent {
  users = httpResource<User[]>(() => `https://api.example.com/users`);
}
```
we can use variable "users" with:
```ts
users.value()
users.isLoading()
users.errors()
```
# example 
```ts 
@if (users.isLoading()) {
  <p>Loading…</p>
} @else if (users.error()) {
  <p>Error: {{ users.error()?.message }}</p>
} @else if (users.hasValue()) {
  <ul>
    @for (u of users.value()) {
      <li>{{ u.name }}</li>
    }
  }
}
```
