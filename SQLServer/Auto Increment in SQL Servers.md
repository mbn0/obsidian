example:
```sql
Employee_ID INT IDENTITY(1,1) PRIMARY KEY,
```

- **1st `1` (Seed)**: This is the starting value for the column. The first row inserted will get the value `1`.
- **2nd `1` (Increment)**: This is the increment value. For each new row inserted, the value will increase by `1`.