1. values added: 20
2. final result: 20
3. var causes the variable to be hoisted to the top of its broader scope, so in this case its hoisted to the top inside the function scope. This causes result to be able to be accessed outside the if block as seen in the screenshot. The issue with this is that if we have a longer function, result can be potentially overriden and due to its placement, it could turn out to be very misleading
4. values added: 20
5. error - result is not defined, because result is only defined in the first block of the if statement, once it leaves that scope it ceases to exist
6. error - it wuold error by line 7 because you are attempting to modify the value of a constant variable, actual value would be 0
7. error - result is not defined, same reason as the 'let' because its block scoped

