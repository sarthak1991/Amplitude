## ES6 imports in NodeJS

This is going to be a short, simple and targeted blog. **Solution First, explanation later. **

#### TL:DR

1. Make sure your Node version is above v13 (if it is not, update your version of node)
2. In the package.json file, paste the following before dependencies 

```
  "type": "module"
``` 
Such that your package.json loos something like below

![es6_module_example.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1616588704378/WWndvcfOb.png)

Et Voila. 

**Still here? Looking for explanation. Read on.** 

## Compatibility
Since Node v13 and above, NodeJS has an experimental support for ES Modules by default as declared [here](https://nodejs.org/docs/latest-v13.x/api/esm.html#esm_enabling), ie, Node will treat the following as ES modules when passed to node as the initial input, or when referenced by import statements within ES module code :- 



  -->   Files ending in ```.mjs```.

  -->   Files ending in ```.js``` when the nearest parent ```package.json``` file contains a top-level field ```"type"``` with a value of ```"module"```.

-->    Strings passed in as an argument to ```--eval``` or ```--print```, or piped to node via ```STDIN```, with the flag ```--input-type=module```.

## Difference b/w CommonJS vs ES6 module syntax

|REQUIRE |	ES6 IMPORT AND EXPORT  |
--- | --- | ---
|Require is Non-lexical, it stays where they have put the file.|Import is lexical, it gets sorted to the top of the file.|
|It can be called at any time and place in the program.|It can’t be called conditionally, it always run in the beginning of the file.|
|You can directly run the code with require statement.|To run a program containing import statement you have to use experimental module feature flag.|
|If you want to use require module then you have to save file with ‘.js’ extension.|If you want to use import module then you have to save file with ‘.mjs’ extension.|

## Support
As of April 2021, an overwhelming majority of browsers support ES6 modules so you don't have to worry about the support

If you found this helpful, consider subscribing to my social channels? 
Cheers! 

