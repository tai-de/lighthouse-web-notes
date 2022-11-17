# Command Line Arguments

## Summary

- [StackAbuse](https://stackabuse.com/command-line-arguments-in-node-js/)

> The simplest way of retrieving arguments in Node.js is via the process.argv array. This is a global object that you can use without importing any additional libraries to use it. You simply need to pass arguments to a Node.js application, just like we showed earlier, and these arguments can be accessed within the application via the process.argv array.

`$ [runtime] [script_name] [argument-1 argument-2 argument-3 ... argument-n]`

Example from `/focal/processargv.js`:

``` javascript
'use strict';

for (let j = 0; j < process.argv.length; j++) {
    console.log(j + ' -> ' + (process.argv[j]));
}
```

All this script does is loop through the process.argv array and prints the indexes, along with the elements stored in those indexes. It's very useful for debugging if you ever question what arguments you're receiving, and in what order.

Now, to run this type the following command. Just make sure you are in the directory where the "processargv.js" file is saved.

``` console
$ node processargv.js tom jack 43
```

Results:

``` console
$ node processargv.js tom jack 43
0 -> /Users/scott/.nvm/versions/node/v4.8.0/bin/node
1 -> /Users/scott/javascript/processargv.js
2 -> tom
3 -> jack
4 -> 43
```