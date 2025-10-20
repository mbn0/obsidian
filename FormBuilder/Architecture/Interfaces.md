# `component.interfaces.ts`

has interface `DatetimeComponentDetails` that extends `FormComponent`, it adds to it details such as:
- Rules about the kind of date.
- Min/max date rules.
- Optional time-aware values
- and relative day offsets.

and an interface `CalndarDay` that explains itself:
```ts
export interface CalendarDay {
  date: Date;
  dayNumber: number;
  isCurrentMonth: boolean;
  isToday: boolean;
  isSelected: boolean;
  isDisabled: boolean;
}
```