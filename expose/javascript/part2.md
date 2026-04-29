1. Line 12 will print "3"
2. Line 13 will print "150"
3. Line 14 will print "150"
4. The function will return [50,100,150]. It return this array because it loops through the input prices array (of length 3), and multiplies each price by the discount value which is 0.5 and rounds to the nearest 2 decimal places then pushes it to the discounted array. So the prices array [100, 200, 300] with discount of 0.5 gets halved to [50, 100, 150].
5. Line 12 will error because now the function is using the let keyword for variable assignment. This means that the variable can only be accessed in the scope of the block. So i can only be accessed in the scope of the for loop, thus trying to reference it outside the scope of the loop will throw a reference error.
6. Line 13 will error as well because again the function is using the let keyword. The discountedPrice variable is declared inside the for loop, and can only be accessed in the for loop block, thus when line 13 tries accessing it from outside the block of the loop, it will throw an error.
7. Line 14 will print "150". This is because the finalPrice variable is declared inside the scope of the function root, so when it goes through the for loop it keeps getting reassigned to the latest final price. Once it loops through the whole prices array it gets set to the final discounted price, which is 300 to 150. Since finalPrice is declared in the scope of the function, it can then be accessed by the console.log, and thus prints out "150."
8. The function will return [50,100,150]. This is because the var to let swap doesn't change what still inside the loop, so the function logic itself stays the same. Thus the discounted variable array still exists in the scope of the function, and halves all the prices to the nearest 2 decimal places then returns it at the end of the function.
9. Line 11 would throw an error because i is undefined at that point in the function because i was declared with let in the scope of the for loop. Thus once it reaches the console.log(i) the i is no longer accessible and will throw an error. i only exists inside the for loop.
10. Line 12 will print 3 because length was declared as const at the function scope level and stores the length of the prices array. Thus when it logs it in the function scope, it prints 3.
11. The function will return [50,100,150] because although discounted is a constant variable, the array's contents are still mutable meaning that you are able to push values into the array, you just cannot reassign the variable to something new. The function works the same as the others and cuts the prices in half and pushes them to the discount array.
12. Object access notation:
    - A. `student.name`
    - B. `student['Grad Year']`
    - C. `student.greeting()`
    - D. `student['Favorite Teacher'].name`
    - E. `student.courseLoad[0]`

13. Arithmetic:
    - A. `'3' + 2` → "32" - Because the addition converts the 2 to a string then concatenates them.
    - B. `'3' - 2` → 1 - subtraction forces both sides to be numbers so 3 becomes a number, so 3-2
    - C. `3 + null` → 3 - adds 3 and null together, null coerces to 0, so 3 + 0
    - D. `'3' + null` → 3null - addition string concatenation, null coerces to 'null', so '3' + 'null'
    - E. `true + 3` → 4 - numeric addition, true coerces to 1, so 1 + 3
    - F. `false + null` → 0 - numeric addition, false coerces to 0, so 0 + 0
    - G. `'3' + undefined` → 3undefined - string concatenation since addition, '3' is a string, undefined becomes 'undefined'
    - H. `'3' - undefined` → NaN - subtraction forces both sides to be numbers, undefined becomes NaN, and any arithmetic with NaN becomes NaN

14. Comparison:
    - A. `'2' > 1` → true - one operand is a string, the other is a number, so converts string to number for comparison, 2 > 1 = true
    - B. `'2' < '12'` → false - Both are strings, so compares lexicographically and compares position 0, so '2' = 50 and '1' = 49, and 50 < 49 = false
    - C. `2 == '2'` → true - double equals sign coerces types, so 2 is converted to a number, so comparison is 2 == 2 which is true
    - D. `2 === '2'` → false - triple equals, strict equality, the two operands are different types so returns false
    - E. `true == 2` → false - true is converted to a number first, which is converted to 1, and 1 == 2 is false.
    - F. `true === Boolean(2)` → true - boolean(2) returns true since any non-zero number is truthy, so true === true, same value and same type so returns true

15. Difference between `==` and `===`: The difference between '==' and '===' is that the double equals coerces types before comparing them, meaning that if the 2 sides of the operator are different types, the javascript will convert one of them to match the other then compare the values. On the other hand the triple equals doesn't coerce the types, meaning that if the types differ then it immediately returns false, otherwise compares the values. So the triple equals compares also to make sure that both sides are the same type.

16. In part2-question16.js

17. The function will return `[2,4,6]`. I got to this because I first looked at the callback function that is being passed through, which is `doSomething`, which all it does is it takes a number as an input and returns the number `* 2`. Then the `modifyArray` function loops through the array `[1,2,3]` and for each iteration it will call that number through the `doSomething` function and add it to the `newArr` array. This means that it first adds 2 (`1 * 2`), then 4 (`2 * 2`), then 6 (`3 * 2`).

18. In part2-question18.js

19. The code will output 1 4 3 2
