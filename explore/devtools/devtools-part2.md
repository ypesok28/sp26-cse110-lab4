1. The bug is that both numbers are being stored as strings, so `num1` becomes a string of a number and so does `num2`. When `calculateSum` tries to add the two strings, the `+` operator concatenates them together rather than adding them as numbers.

2. I would fix this by wrapping the input values in `Number()` before assigning them to `num1` and `num2`, so the addition operates on numeric values instead of strings.

![Fix](../../expand/screenshots/fix.png)
