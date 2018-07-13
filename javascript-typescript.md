
- [Promise](#promise)
    - [Understanding resolve / reject](#understanding-resolve--reject)
- [Closure](#closure)

---
# Promise
## Understanding resolve / reject
[link source](https://basarat.gitbooks.io/typescript/docs/promise.html)
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
# Closure