# JavaScript Closure Issue in setTimeout Loop

This example demonstrates a common issue in JavaScript related to closures and the `setTimeout` function.  The expected behavior is to print the numbers 0 through 9, each after a 1-second delay. However, due to the way closures work, all callbacks will print the final value of 'i' (which is 10). 

**To Reproduce:**
1. Run `bug.js`.
2. Observe that the console logs '10' ten times instead of 0-9.

**Solution:** The solution involves using `let` within the loop to create a new scope for each iteration, ensuring each callback captures the correct value of `i`.

**Solution File:** `bugSolution.js` demonstrates the corrected code.