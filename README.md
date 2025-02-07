# MongoDB $inc Operator Error: String Increment

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries. The `$inc` operator is used to increment a numerical field by a given value.  However, if a string is provided as the increment value, MongoDB will not throw an error but will instead produce unexpected results. 

The `bug.js` file shows the incorrect usage, while `bugSolution.js` provides the corrected version.

## How to reproduce

1.  Make sure you have MongoDB installed and running.
2.  Create a collection named `myCollection` and insert a document with a numerical field (e.g., `{ _id: 1, count: 0 }`).
3. Run the code in `bug.js`. Observe the unexpected result.
4. Run the code in `bugSolution.js` and see the expected result.

## Solution
Ensure that you use a numerical value when using the `$inc` operator.  Never use strings.