Unit Testing
Unit testing is performed by the developer during the development cycle, and
Functional testing is performed by the tester during the level of system testing.
Pair programming can help on preventing the bugs in higher chance.

1. Jasmine
- Jasmine is a behaviour-driven development framework for testing JavaScript code. It doesn't depend on any other JavaScript frameworks and it doesn't require a DOM. However, it does have a clean, obvious syntax so that you can easily write tests.
2. Mocha
- Mocha is a feature-rich JavaScript test framework running on Node.js and in the browser. Mocha tests run serially, allowing for flexible and accurate reporting, while mapping uncaught exceptions to the correct test cases.

So what is linting?
lint, or a linter, is a tool that analyzes source code to flag programming errors, bugs, stylistic errors, and suspicious constructs.
1. Eslint (npm install eslint -D)
- Example) 
const test = 'I am a test';
console.log(`Test: ${test}`);
const test = 'Another one.';

