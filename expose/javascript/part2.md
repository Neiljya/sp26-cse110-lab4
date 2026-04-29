1. 3, because i is of type var, it exists outside of its block (the for loop), so its value is the final value that i is set to which is i = 3
2. 150, same reason as above it exists ouside of its block so its value is the final value, 300 is the last element of the prices array so the final value is the result of 300 * (1-discount)
3. 150, same reason as above but finalPrice is Math. round(150 * 100) / 100;
4. [50, 100, 150] - line 3 var discounted = [] is an empty array, for loop runs 3 times and applies 0.5 discount to each item in prices. 

First price is 100, apply the discount formula combined with the final price formula and you get 50, push.

Second price and third price follows same logic

5. error because i is now block scoped so i does not exist after the for loop ends

6. error because discountedPrice is now block scoped to the for loop so it will not exist after for loop ends

7. 150 - finalPrice is scoped to the function, print is called inside the same scope so no crash

8. [50, 100, 150] this works the same as #4, they both have the same scope because in #4 var is declared at the top of function so scope-wise they are the same

9. error because i is block scoped so doesn't exist outside for loop. You are allowed to push into a const array, just not reassign the reference to anything else

10. 3, length is unchanged and the scope is functionally the same as if you were to declare it using 'let', just that length cannot be modified after initialization

11. [50, 100, 150], you are allowed to push into a const array, because the array itself is not const, the reference is the only thing that is const. So the array can be modified, but reference pointing to the array cannot be changed.

12. 
A. student.name
B. student['Grad Year']
C. student.greeting()
D. student['Favorite Teacher'].name
E. student.courseLoad[0]

13. 
A. '32', the plus operator in this case concatonates the 2, 2 is coerced into a string type since '3' is a string
B. 1, - does not work on strings so the only logical coercion is to coerce '3' into a number to perform subtraction
C. 3 - null is coerced into 0
D. '3null', '3' is a string so null is converted to string which is literally 'null'
E. 4, booleans are coerced into 1 or 0, true is 1 so 1 + 3 = 4
F. 0, both are 0 numerically so 0 + 0 = 0
G. '3undefined', same with null, string and + is concat, undefined is coerced into 'undefined'
H. NaN, subtraction cant be used on strings, so it gets converted to a number operation, undefined does not have a direct number representation so it turns into NaN (not a number) so the operation results in NaN
14. 
A. true, when comparing string to number a string is casted to a number so 2 > 1 is true
B. false, both are strings so they are compared lexicographically. '2' has 1 character while '12' has 2 characters, additionally '2' comes after '1' in dictionary order, so '2' is greater
C. true, loose equality converts '2' to number before comparing
D. false, strict equality checks both value, the type differs (String vs. Number)
E. false, true is represented as 1 so 1 == 2 is false
F. true, anything nonzero in javascript is a "truthy" value

15. '==' coerces values and checks the "value", disregarding type because it converts both into a common type. '===' is stricter, checks both types and value, so if you compare String to a Number its false, does not perform type coercion

16. 

for (const property in statistics) {
    if (property.startsWith('r') || statistics[property] % 2 !== 0) {
        console.log(statistics[property])
    }
}

17. 

modifyArray is called with [1,2,3] and doSomething is passed
as the callback

modifyArray creates a new array named newArr

Start iterating:
i = 0, 1 is passed into doSomething -> doSomething(1) = 1 * 2 = 2
2 pushed into newArr

newArr = [2]

i = 1, doSomething(2) -> 4
newArr = [2, 4]

i = 2, doSomething(3) = 6
newArr = [2, 4, 6]

return newArr

([2,4,6]) is the result

19. 
1
4
3
2