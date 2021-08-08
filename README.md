<h1 align="center" style="font-size: 3em;">JavaScript Notes</h1>

# Table of Contents
<ol>
<li>[ES6](#ES6)
<ol>
<li>Indented item</li>
<li>Indented item</li>
</ol>
</li>
<li>Fourth item</li>
</ol>
1. [ES6](#ES6)
- [var Vs let](#var-vs-let)

## ES6 <a name="ES6"></a>
### var Vs let <a name="var-vs-let"></a>
1. Biggest problems with declaring variables with the var keyword is that you can overwrite variable declarations without an error.
    * ``` var camper = 'James';
          var camper = 'David';
          console.log(camper); ```
        * Here the console will display the string David.
    * If you were to replace var with let in the variable declarations of the code above, **the result would be an error**.
    * ``` let camper = 'James';
          let camper = 'David'; ```

2. Compare Scopes of the var and let Keywords
    * When you declare a variable with the `var` keyword, it is declared globally, or **locally if declared inside a function**.
        *``` var numArray = [];
              for (var i = 0; i < 3; i++) {
                numArray.push(i);
              }
              console.log(numArray);
              console.log(i); ```
       * Here the console will display the values [0, 1, 2] and 3. With the var keyword, i is declared globally. So when i++ is executed, it updates the global variable.

3. Union Types Array
    * `let emptyMixedArr: (string | number)[]`
        * NOTE: will need to wrap the union in brackets.
        * This array accepts both types strings and numbers: `emptyMixedArr.push('only strings allowed', 1)`

4. Any Type Array (Dynamic Type)
    * `let anyArray: any[] = []`
        * Can push any types inside this array: `anyArray.push(1, false, 'string')`

### Objects
* NOTE: With objects once we create an object (and declare their properties), we cannot add new properties.
* NOTE: We cannot change the property type, BUT we can change thier values.

1. Creating objects
```typescript 
    let player = {
    name: 'Messi',
    age: 30,
    isPlaying: true
    }
```
* To change the property value we do: `player.name = 'Ronaldo'`.
* If you do change the entire Object you must include ALL properties.

2.  Explicit Object type
    * `let thisIsAnObject: Object`
        * Now to add properties inside the object: `thisIsAnObject = { name: 'Redz', age: '23'}`

3. Creating an object with EXPLICIT property types
```typescript
let newObj: {
    name: string,
    age: number
}
```


 


    
    




