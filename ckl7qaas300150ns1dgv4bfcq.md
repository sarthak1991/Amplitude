## ES6 imports in NodeJS

This is going to be a short, simple and targeted blog. **Solution First, explanation later. **

#### TL:DR

1. Make sure your Node version is above v13 (if it is not, update your version of node)
2. In the package.json file, paste the following before dependencies 

```
  "type": "module"
``` 
Such that your package.json loos something like below
```
{
  "name": "ES6_modules_example",
  "version": "0.1.0",
  "private": true,
  "type": "module",
  "scripts": {
    "start": "node server",
  }
}

```

Et Voila. 

**Still here? Looking for explanation. Read on.** 

## Compatibility
Since Node v13 and above, NodeJS has an experimental support for ES Modules by default as declared [here](https://nodejs.org/docs/latest-v13.x/api/esm.html#esm_enabling), ie, Node will treat the following as ES modules when passed to node as the initial input, or when referenced by import statements within ES module code :- 



  -->   Files ending in ```.mjs```.

  -->   Files ending in ```.js``` when the nearest parent ```package.json``` file contains a top-level field ```"type"``` with a value of ```"module"```.

-->    Strings passed in as an argument to ```--eval``` or ```--print```, or piped to node via ```STDIN```, with the flag ```--input-type=module```.

If you found this helpful, consider subscribing to my social channels? 
Cheers! 

