# Javascript Design Patterns
Descriptions and examples of common design patterns in Javascript.

---
## Some useful terminology and concepts

### Higher order functions

### First class citizens
Programming languages denote first class citizens as things (i.e. objects) that:
* can be stored as variables / data structures
* can be passed as parameters in to functions
* can be returned from functions

The general gist of it is "they can do what everything else can do, they are not restricted". In Javascript functions are first class citizens which is great because it opens the door to all kinds of techniques.

### Lambda
A Lambda is essentially an anonymous function but there is a difference. A Lambda function is:

**Passed in to a function as an argument**
```javascript
function exampleFunction(lambdaFunction) {
    lambdaFunction(10);
}

exampleFunction(function(x) {
    return x + 1;
});
```

**Returned as a value from a function**
```javascript
function exampleFunction(x) {
    return function(y) {
        return x + y;
    };
}
```

**Assigned to variables**
```javascript
var lambdaFunction = function(x) {
    return x + 1;
}
```

A self-executing function is an example of an anonymous function that is NOT a lambda:
```javascript
(function() {
    console.log('Im going to die after Ive been called');
})();
```

In fact a Lambda doesn't have to be anonymous, it can have a name:
```javascript
element.addEventListener('click', function myClickEventLambda() {
    console.log('myClickEventLambda was called when the element was clicked!');
});
```
*The point is that a Lambda is a function expression, that is stored as data, so it can be passed around to other things.*
