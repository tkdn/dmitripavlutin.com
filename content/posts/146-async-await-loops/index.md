---
title: "async/await and JavaScript Loops"
description: "How does async/await syntax work in JavaScript for and while loops"
published: "2021-08-17T12:00Z"
modified: "2021-08-17T12:00Z"
thumbnail: "./images/cover-2.png"
slug: async-await-cycles-javascript
tags: ['javascript', 'async', 'for']
recommended: ['what-is-javascript-promise', 'promise-all']
type: post
---

Let's consider an asynchronous function `runLoop()` where inside a `for()` loop an `await` statement is used:

```javascript
async function runFor() {
  for (let i = 0; i < 3; i++) {
    await delay(1000);
  }
  console.log('Done!');
}

runLoop();
```

Where the `delay(time)` function simply returns a promise that gets resolved after `time` milliseconds:

```javascript
function delay(time) {
  return new Promise(resolve => {
    setTimeout(() => resolve(), time);
  });
}
```

Here's the big question: does `Done!` message log to console after passing *1 second* or *3 seconds*? 

In this post the answer to this question, and generally how `await` behaves in JavaScript loops.  

## 1. *await* in loops

## 2. await for...of syntax

## 3. Conclusion