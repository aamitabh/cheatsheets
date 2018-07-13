- [Promise](#promise)
- [Markdown Sample](#markdown-sample)
    - [Task List](#task-list)
    - [Table Heading](#table-heading)

# Promise
```js
    const promise = new Promise((resolve, reject) => {
        resolve(123);
    });
    promise.then((res) => {
        console.log('I get called:', res === 123); // I get called: true
    });
    promise.catch((err) => {
        // This is never called
    });
    const promise = new Promise((resolve, reject) => {
        reject(new Error("Something awful happened"));
    });
    promise.then((res) => {
        // This is never called
    });
    promise.catch((err) => {
        console.log('I get called:', err.message); // I get called: 'Something awful happened'
    });
```
