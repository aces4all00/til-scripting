# Explicitly declaring variables in PowerShell

When coding in `C#` I prefer to declare my variables as close to the start of the scope as possible, then later initialize them with their first values when the code calls for it. It's one of the methods I use to help make sure I track what I am trying to accomplish

```C#
// Declare greeting as string
string greeting;

// lines of other code. . .

// initialize greeting with "Hello"
greeting = "Hello";
```

To do the same thing in `PowerShell`:

```PowerShell
# Declare greeting as string
$greeting = [string]::new()

# lines of other code. . .

# initialize greeting with "Hello"
$greeting = "Hello"
```