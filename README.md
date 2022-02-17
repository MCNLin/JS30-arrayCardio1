Welcome! 

Come join me on my journey of Wes Bos's 30 Day Vanilla JS Code Challenge! Where I build 30 things in 30 days with 30 tuturials~
<br></br>
## Day 4 Challenge of Javascript30

### Array Cardio 1
---- 
In this challenge, I was given some test datasets and utilised popular Array Methods using the data provided~

----
### What I learned/refresher:

#### .filter()
  - this method creates a new array with all elements that pass the test implemented by the provided function.
  - example from challenge (filter through the array to find inventors who were born in the 1500s) :
  ```js
  const fifteen = inventors.filter(inventor => inventor.year >= 1500 && inventor.year <=1599)
  ```

#### .reduce()
- this method iterates through an array and returns a single value. It takes a callback function with two parameters (accumulator, currentValue) as arguments. On each iteration, accumulator is the value returned by the last iteration, and the currentValue is the current element.
- exampe from challenge (looking for total # of years lived for all inventors):
```js
const totalYears = inventors.reduce((total, inventor) => {
      return total + (inventor.passed - inventor.year)

    },0);
```
- In this example, **total** is the accumulator and **inventor** is currentValue. The ```0``` is a starting point for the **total** or else it would of use ```undefined``` to add the first iteration.

- Another example of using .reduce() in the challege was to reduce each element to the number of occurrences in the array.
```js
const transportation = data.reduce(function(obj,item){
      if (!obj[item]){
        obj[item] = 0
      }
      obj[item]++;
      return obj

    },{})
```
In this example, used an ```empty object``` as the inital value for the object and for each iteration called ```obj[key]```.

#### .map()
- this method executes a callback function on each element in an array. It returns a **new** array made up of the return values from the callback function

#### .sort()
#### Array.from


Starter code from [Javascript 30 Challenge](https://github.com/wesbos/JavaScript30)