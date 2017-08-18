# Javascript Design Patterns
Descriptions and examples of common design patterns in Javascript.




## Some useful terminology and concepts

### First class citizens


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
The point is that a Lambda is a function expression, that is stored as data, so it can be passed around to other things.
