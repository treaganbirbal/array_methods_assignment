# Exercises

__NOTE:__ DO NOT USE THE BUILT IN METHODS WHEN ASKED TO MAKE THEM!

1. Using Array.prototype add a new method `myForEach` that mimics the behavior of the built in `forEach`.
//
Array.prototype.myForEach = function(callback) {
  for (let i = 0; i < this.length; i++){
    callback(this[i]);
  }
};
[1, 2, 3].myForEach((el) => {
console.log (el)
})
  }
};
//
2. Use your `myForEach` to add `myMap` to the Array prototype. `myMap` should behave the same as regular `map`.
//
Array.prototype.myMap = function(callback){
  let output = [];
  for(let i = 0; i < this.length; i++){
    output.push(callback([this[i],i));
  }
  return output;
}
//

3. Write a 'myFilter` that behave's the same as `filter`.
//
Array.prototype.myFilter = function(callback){
  let output [];
  for(let i = 0; i < this.length; i++){
    if(callback(this.[i], i)
    output.push((this[i], i));
  }
  return output
}
//

4. Write a `myEvery`.
//
Array.prototype.myEvery = function(callback){
  for(let i = 0; i < this.length; i++){
    if(!(callback(this.[i])){
      return false;
    }
  }
  return true;
}
//

5. Write a `myReduce`. It should use the first element in the array if none is given.
//
Array.prototype.myReduce = function(callback, optAcc){
  let acc = optAcc || 0;
  for(let i = 0; i < this.length; i++){
    acc = callback(acc.this[i], i);
  }
  return acc;
}


//

6. Write a `myTranspose`. This function should transpose a matrix. Exp:
```js
let mtx = [
            [1, 2],
            [3, 4],
            [5, 6]
          ]

mtx.myTranspose();

// => [
        [1, 3, 5],
        [2, 4, 6]
       ]

```
//
Array.prototype.myTranspose = function(callback){
 let grid = [];
 for(let i = 0; i < mtx[0].length; i++){
   grid[i] = []

   for(let j = 0; j< mtx.length;j++){
     grid[i][j] = mtx[j][i]

   }
 }
 return grid
};

let mtx = [
           [1, 2],
           [3, 4],
           [5, 6]
         ]

//console.log(transpose(mtx))
let results = mtx.myTranspose((el) => {
 console.log(el)
})
console.log(results)
//

7. Use `myMap` to build a new array where every element is incremented by 10.
//
Array.prototype.myForEach = function (callback) {
 for(let i = 0; i < this.length; i++){
   callback(this[i]);
 }

};

Array.prototype.myMap = function(callback) {
let newArray = [];
this.myForEach((el) => {
 newArray.push(callback(el))
})
return newArray
};


let arr = [1,2,3,4,5,6];

let results = arr.myMap((el) => {
 console.log(el * 10)
});

//
8. Use `myMap` to build a new array where every non-string element is converted to an empty string.

//

Array.prototype.myMap = function(callback){
  let newArray = []
  
}

//

9. Use `myFilter` to get only the even elements in an array.
10. Use `myEvery` to check if all elements in the array are the same.
11. Use `myReduce` to return the sum of every element in an array.
12. Use `myMap` to build a new array that doubles each element. Then chain `myReduce` to find the product of all the elements.
13. Use `myReduce` to find the largest number in an array.
14. Write a function `elementDivisibleBy` with parameters `divisor` and `arr`.
Use `myFilter` to return a new array of every element of arr that can be evenly divided by divisor.
14. Write a `myJoin` function.
15. Write a `mySlice` function.
16. Write a function `countZeroes`, which takes an array of numbers as its argument and returns the amount of zeroes that occur in it.
Use reduce.
17. Write a `numberTimesIdx` that uses `map` and multiples each number in the array by it's index.

Bonus: Write a `myFlatten`. This should take a multi-dimensional array and return it as one array.
```js
let arr = [1, 2, [3, 4, 5, [6, 7, 8]]]
  arr.myFlatten();
  // => [1, 2, 3, 4, 5, 6, 7, 8]
```
