## What is the difference between [[FormBuilder/Architecture/Models|Models]] and [[Interfaces]]?
- interfaces/: Shared, app‑wide type contracts. Pure TypeScript types used across many features (component, dialog, event, form, ui, validation, etc.). No runtime behavior.
- models/: Domain models and concrete data tied to specific features or APIs. Can include classes, type aliases, example fixtures, and yes—local interfaces that are specific to those models or API DTOs.

## Why models can also have interfaces:

- It’s OK to colocate small, model‑specific or API‑specific interfaces next to the model they belong to (e.g., models/responses/*, form-schema.model.ts). They aren’t intended for broad reuse, so they stay with the model for cohesion.

## Rule of thumb:
- Used across multiple areas? Put the interface in interfaces/.
- Specific to one model/API or mostly internal? Keep it in models/.
- Needs behavior (methods)/constructors? Use a class in models/.
- Example here: submission/form/ui contracts live in interfaces/_, while API response DTOs and example schema/data live in models/_.