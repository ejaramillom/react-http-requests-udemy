# async - await feature in javascript

The word “async” before a function means one simple thing: a function always returns a promise. Other values are wrapped in a resolved promise automatically.

So, async ensures that the function returns a promise, and wraps non-promises in it. Simple enough, right? But not only that. There’s another keyword, await, that works only inside async functions, and it’s pretty cool.

# callbacks

Callback functions are used a lot in JavaScript. In the end, a callback function is simply a function that's passed as an argument to another function.

function greet() {
  console.log('Hi!');
}

function executeItForMe(cb) {
  cb();
}

executeItForMe(greet);

# promises

they only work inside asynchronous functions

Await

The syntax:

// works only inside async functions
let value = await promise;

The keyword await makes JavaScript wait until that promise settles and returns its result.

Here’s an example with a promise that resolves in 1 second:

async function f() {

  let promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("done!"), 1000)
  });

  let result = await promise; // wait until the promise resolves (*)

  alert(result); // "done!"
}

f();

# abstract 

Summary

The async keyword before a function has two effects:

    Makes it always return a promise.
    Allows await to be used in it.

The await keyword before a promise makes JavaScript wait until that promise settles, and then:

    If it’s an error, an exception is generated — same as if throw error were called at that very place.
    Otherwise, it returns the result.

Together they provide a great framework to write asynchronous code that is easy to both read and write.