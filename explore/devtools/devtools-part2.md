1. The bug was both num1 and num2 were string inputs, result was concatenating both with
the + operator, so the output was "23", and didn't add them as numbers

2. Convert htem to numbers first, then check if they are numbers (isNaN), if they are then we can add,
else we return an error or don't add