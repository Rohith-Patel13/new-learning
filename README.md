# new-learning

console.log("Become the programmer you're meant to be!")

// const,var,let youtube video: https://youtu.be/9WIJQDvt4Us?si=FS3p8vrn8EHcKS77
1) var (Function Scope):
Variables declared with var are function-scoped. This means they are visible throughout
the function in which they are declared, but not outside of it.
var variables are hoisted, which means they are moved to the top of their
containing function or global scope during the compilation phase.
This can lead to some unexpected behavior.
Example:
function example() {
    var x = 10;
    if (true) {
        var y = 20;
    }
    console.log(x); // 10
    console.log(y); // 20
}


2) let and const (Block Scope):
Variables declared with let and const have block scope, which means they are
only visible within the block in which they are defined (i.e., within curly braces { }).
let and const variables are not hoisted, and they are only accessible after their
declaration in the code.
Example:
function example() {
    let x = 10;
    if (true) {
        let y = 20;
        const z = 30;
    }
    console.log(x); // 10
    console.log(y); // ReferenceError: y is not defined
    console.log(z); // ReferenceError: z is not defined
}



3) const (Constant):
Variables declared with const are also block-scoped.
const variables, as the name implies, are constants.
They cannot be reassigned after they are given a value.
Example:
const PI = 3.14159265359;
PI = 4; // This will result in an error (can't reassign a constant)

** Math.random() is a built-in JavaScript 
function that generates a random floating-point 
number between 0 (inclusive) and 1 (exclusive). 
It allows you to generate pseudo-random numbers, 
which are not truly random but are sufficiently 
unpredictable for most use cases. 
Here's how you can use Math.random():
const randomNum = Math.random();
console.log(randomNum);

Math.floor():
The Math.floor() method rounds a number down to the nearest integer that is less than or 
equal to the original number.
It always rounds down, making the number smaller.
It is used to get the largest integer less than or equal to a given number.
Example:
Math.floor(3.9); // Result: 3
Math.floor(-2.1); // Result: -3


Math.ceil():
The Math.ceil() method rounds a number up to the nearest integer that is greater than or 
equal to the original number.
It always rounds up, making the number larger.
It is used to get the smallest integer greater than or equal to a given number.
Example:
Math.ceil(3.1); // Result: 4
Math.ceil(-2.9); // Result: -2


Math.round():
The Math.round() method rounds a number to the nearest integer, 
with .5 or greater rounded up, and less than .5 rounded down.
It performs standard rounding where it rounds up if the decimal 
part is equal to or greater than 0.5 and rounds down if it's less than 0.5.
Example:
Math.round(3.4); // Result: 3
Math.round(3.5); // Result: 4
Math.round(3.9); // Result: 4
console.log(Math.round(-2.1)); // Result: -2
console.log(Math.round(-2.4));// Result: -2
console.log(Math.round(-2.5)); // Result: -2
/*
-2.5 is exactly in the middle between -2 and -3, 
but the standard rounding rule is to round to the 
nearest even number, which is -2 in this case. 
This is known as "banker's rounding" or "round half to even."
*/
console.log(Math.round(-2.6)); // Result: -3
console.log(Math.round(-2.8)); // Result: -3
console.log(Math.round(3.5))// Result: 4
/*
3.5 is exactly in the middle between 3 and 4, 
and the standard rounding rule applies, 
so it rounds up to 4.
*/


/*
The includes() method returns true if the provided item exists in the array.
If no item is found, it returns false.
Syntax: arr.includes(item)
*/
let myarray = [5,4,3,2,1];

let possibilty1 = myarray.includes(3);
let possibilty2 = myarray.includes(8);
console.log(possibilty1);//true
console.log(possibilty2);//false
/*------------------------------------END------------------------------------------------*/



/*
The indexOf() method returns the first index at which a given item can be found in the array.
If no item is found, it returns -1.
Syntax: arr.indexOf(item)
*/
let indexNum1 = myarray.indexOf(1);
console.log(indexNum1);// 4
let indexNum2 = myarray.indexOf(0);
console.log(indexNum2);// -1
/*------------------------------------END------------------------------------------------*/



/*
The lastIndexOf() method returns the last index at which a given item can be found in the array.
If no item is found, it returns -1.
Syntax: arr.lastIndexOf(item)
*/
let array = [4,5,6,4,8,9];
let lastIndexNum1 = array.lastIndexOf(4);
console.log(lastIndexNum1);// 3
let lastIndexNum2 = array.lastIndexOf(0);
console.log(lastIndexNum2);// -1
/*------------------------------------END------------------------------------------------*/



/*
The find() method returns the first item's value that satisfies the provided testing function.
If no item is found, it returns undefined.
Syntax: arr.find(Testing Function)
*/
let arrayItems = [12,34,56,78,90];
let findingItem1 = arrayItems.find(function(eachNum){
    //PAUSE LEARNING
    if (eachNum>=59){
        return true;
    }
    else{
        return false;
    }
}
);
console.log(findingItem1);// 56
/*------------------------------------END------------------------------------------------*/

/*
The find() method returns the first item's value that satisfies the provided testing function.
If no item is found, it returns undefined.
Syntax: arr.find(Testing Function)
*/
let findingItem2 = arrayItems.find(function(eachNum){
    //PAUSE LEARNING
    if (eachNum===0){
        return true;
    }
    else{
        return false;
    }
}
);
console.log(findingItem2);// undefined
/*------------------------------------END------------------------------------------------*/



/*
The unshift() method adds one or more items to the beginning of an array
and returns the new array length.
Syntax: arr.unshift(item1,item2, ..., itemN)
*/
let arrayItemsunshift = [12,34,56,78,90];
let newarrayItemsunshift=arrayItemsunshift.unshift(1,2,3,4);
console.log(arrayItemsunshift) // [1,2,3,4,12,34,56,78,90];
console.log(newarrayItemsunshift);// 9: new array length.
/*------------------------------------END------------------------------------------------*/



/*
The shift() method removes the first item from an array and returns that removed item.
Syntax: arr.shift()
*/
let arrayItemsshift = [12,34,56,78,90];
let newarrayItemsshift=arrayItemsshift.shift();
console.log(arrayItemsshift) //[34,56,78,90]
console.log(newarrayItemsshift);//12: returns that removed item
/*------------------------------------END------------------------------------------------*/



/*
The concat() method can be used to merge two or more arrays.
This method does not change the existing arrays but instead returns a new array.
Syntax:
let newArray = arr1.concat(arr2);
*/
let arrayA=[1,2,3];
let arrayB=[4,5,6];
let newArray = arrayA.concat(arrayB);
console.log(newArray);//[ 1,2,3,4,5,6]:returns a new array
/*------------------------------------END------------------------------------------------*/



/*
The slice() method returns a portion
between the specified start index and end index(end index not included)
of an array into a new array.
Syntax: arr.slice(startIndex, endIndex)
*/
let slicearray = [1,2,3,4,5,6,7,8];
let newslicedarray = slicearray.slice(2,6);
console.log(newslicedarray);//[ 3,4,5,6]:between the specified start index and end index(end index not included)
/*------------------------------------END------------------------------------------------*/



/*
The join() method creates and returns a new string by concatenating
all of the items in an array,separated by commas or a specified separator string.

If the array has only one item, then it will be returned without using 
the specified separator.

Syntax: arr.join(separator)

Here separator is a string used to separate each item of the array.
If omitted, the array items are separated with a comma.
*/
let joinArray =[1,2,3,4,5];
let newJoinArray = joinArray.join(" ");
console.log(newJoinArray);//1 2 3 4 5
/*------------------------------------END------------------------------------------------*/



/*
The sort() method sorts the items of an array and returns the sorted array.
The default sort order is ascending.

Syntax: arr.sort()
*/
let ourArray=[1,4,6,7,3,2];
let sortedArray = ourArray.sort();
console.log(sortedArray);//[1,2,3,4,5,6,7]
/*------------------------------------END------------------------------------------------*/

// Example array
const numbers = [1, 2, 3, 4, 5];

// Using splice() to remove elements
/*
splice(): The splice() method is used to change the contents of an array by removing
or replacing existing elements and/or adding new elements in place. It modifies the
original array and returns an array containing the removed elements.

array.splice(start, deleteCount, item1, item2, ...);

start: The index at which to start changing the array.
deleteCount: An integer indicating the number of elements to remove from the array,
starting at the start index. If deleteCount is 0, no elements are removed.
item1, item2, etc.: The elements to be added to the array at the start index.

The splice() method returns an array containing the removed elements.
If no elements are removed (i.e., deleteCount is 0), it returns an empty array.
*/
const removed = numbers.splice(2, 2); // Removes elements starting at index 2
console.log(numbers); // [1, 2,5]
console.log(removed); // [3, 4]
/*------------------------------------END------------------------------------------------*/


// Using map() to create a new array
/*
map(): The map() method creates a new array by applying a provided function to each element
in the original array. It doesn't modify the original array but returns a new one with the
results of the function applied to each element.

const newArray = originalArray.map(callback(currentValue, index, array));

originalArray: The array you want to map over.
callback: A function to be applied to each element of the array.
currentValue: The current element being processed in the array.
index (optional): The index of the current element being processed.
array (optional): The array map() was called upon.
*/
const squared = numbers.map(num => num * num); // Creates a new array with squared values
console.log(squared); // [1, 4]
/*------------------------------------END------------------------------------------------*/


// Using filter() to create a new array with filtered elements
/*
filter(): The filter() method creates a new array by filtering out elements from the
original array based on a provided function that defines the filtering criteria.
It returns a new array containing only the elements that pass the condition.

const newArray = originalArray.filter(callback(currentValue, index, array));

originalArray: The array you want to filter.
callback: A function that defines the filtering criteria.
currentValue: The current element being processed in the array.
index (optional): The index of the current element being processed.
array (optional): The array filter() was called upon.
*/
const evenNumbers = numbers.filter(num => num % 2 === 0); // Filters for even numbers
console.log(evenNumbers); 
/*------------------------------------END------------------------------------------------*/


// Using reduce() to sum all elements
/*
//https://youtu.be/3mGbzELRBkM?si=G96q_ms5eZ9AAw12 explanation link
reduce(): The reduce() method applies a function against an accumulator and each element
in the array (from left to right) to reduce the array to a single value. It's often used
for aggregating data or performing cumulative operations.

array.reduce(callback(previousValue, currentValue, index, array), initialValue);

array: The array you want to reduce.
callback: A function to execute on each element in the array.
previousValue: previousValue from the last function call
currentValue: The current element being processed in the array.
index (optional): The index of the current element being processed.
array (optional): The array reduce() was called upon.
initialValue (optional): A value that will be used as the initial value of the previousValue. If not provided, the first element in the array will be used as the initial accumulator value.


*/
const n=[12,34,5,6,7,8]
const sum = n.reduce((previousValue, current) =>{ 
    console.log(`previousValue: ${previousValue}`)
    console.log(`current: ${current}`)
    return previousValue + current
}, 0); // Sums all elements
console.log(sum); // 72
/*
previousValue: 0
current: 12
previousValue: 12
current: 34
previousValue: 46
current: 5
previousValue: 51
current: 6
previousValue: 57
current: 7
previousValue: 64
current: 8
72
*/

/*------------------------------------END------------------------------------------------*/


// Using forEach() for side effects
/*
forEach(): The forEach() method iterates through each element in an array and applies 
a provided function to each element. It's mainly used for executing a function for
its side effects (e.g., updating variables) rather than producing a new array or value.

array.forEach(callback(currentValue, index, array));

array: The array you want to iterate over.
callback: A function to execute for each element in the array.
currentValue: The current element being processed in the array.
index (optional): The index of the current element being processed.
array (optional): The array forEach() was called upon.
*/
numbers.forEach(num => console.log(num)); // Prints each element

const person={
    name:"rohit",
    age:21,
    sex:"male"
}
Object.values(person).forEach((parameter)=>{
    console.log(parameter);
})



/*
push()
The push() method adds new items to the end of the array.
*/
let myArray = [5, "six", 2, 8.2];
myArray.push(true);
console.log(myArray);  // [5, "six", 2, 8.2, true]


/*
pop()
The pop() method removes the last item of an array and returns that item.
*/
let myArray = [5, "six", 2, 8.2];
let lastItem = myArray.pop();
console.log(myArray);  // [5, "six", 2]
console.log(lastItem);  // 8.2


//Anonymous function:
console.log(function(a,b){
    return a+b
},(4,8)); // [Function (anonymous)] 8


//function expression: assigning a anonymous function to a variable
const add = function(a,b){
    return a+b
}
console.log(add(2,3));

// Arrow functions: Arrow functions are a short syntax for defining a javascript.
const add = (a,b)=>a+b
console.log(add(1,2))



callback function:- A callback function is a function that is passed as an argument to another function.
ex:- 1)iteration like forEach method.



event handling in js:- 
1)event handling is the process of responding to user actions in a web page 
2)addEventListener method of js allows to attach an event name and with 
the function you want to perform on the event. 
> Event.addEventListener("click",callbackFunction)
> Event.addEventListener("mouseover",callbackFunction)
> Event.addEventListener("keydown",callbackFunction)
> Event.addEventListener("keyup",callbackFunction)
> Event.addEventListener("submit",callbackFunction)
> Event.addEventListener("focus",callbackFunction)
> Event.addEventListener("blur",callbackFunction)
> Event.addEventListener("change",callbackFunction)
> Event.addEventListener("load",callbackFunction)
> Event.addEventListener("resize",callbackFunction)



Higher-order function in js:- 
1) take one or more function as arguments(callback function) OR 
2)returns a function as a result



Asynchronous operations in javascript:- 
1) asynchronous operations are operations that do not block 
the execution of the code
2) where as setTimeout is the Asynchronous function which executes
callback function after a specific period of time.
Uses of Asynchronous operations:- 
1)setTimeout 2)Promises 3)Loading Data from an API 
4)Uploading files 5)Animations and transitions
example:- 
console.log("Before setTimeout")
setTimeout(()=>{
    console.log("Inside setTimeout")
})
console.log("After setTimeout")
output:- 
Before setTimeout
After setTimeout
Inside setTimeout




Promises:- 
1)Promises in javascript are a way to handle asynchronous operations
2)A promise represents a value that may not be available yet but
will be available at some point in future. 
ex:-you call API Method
3)Promise can be in one of three states: pending,resolved,or rejected.
steps in promise :- 
const promise = new Promise((resolve,reject)=>{
    // perform Asynchronous operation
    // if successful, call resolve(value)
    // if failed, call reject(error)
})
example to implements in promises:- 
const myPromise = new Promise((resolve,reject)=>{
    setTimeout(function() {
        const randomNumber =Math.floor(Math.random()*10);
        
        //Resolve promise 
        if(randomNumber<5){
            resolve(`success ${randomNumber}`)
        }
        else{
            reject(`failure ${randomNumber}`)
        }
    }, 1000);
})
myPromise.then((result)=>{
    console.log(result)
}).catch((error)=>{
    console.log(error)
})
applications of promises:- 
1)data fetching
2)API calls 



class:- class is a template for creating objects with similar
properties and methods. 
objects:- objects are the instances of a class which are created
using the new keyword
example code :
let carName="Honda";
class Car{
    //static properties
    static numOfWheels=4 
    
    //dynamic properties 
    constructor(model,year){
        this.model=model;
        this.year=year;
    }
    
    //method 
    start(){
        console.log(`${this.model} started`);
    }
}

// create an instance of the car class 
const myCar = new Car("Honda",2023);

//access properties 
console.log(myCar.model);// Honda

//access methods 
myCar.start(); // Honda started




puspose of this keyword in js:- 
1)"this" refers to the current context or scope in which 
code is being executed 



what is hoisting in JavaScript?
1)Hoisting is a js behaviour where functions and variable declarations
are moved to the top of their respective scopes during the 
compilation phase
example 1 of hoisting:
myFunc()
function myFunc(){
    console.log("Hello")
}

example 2 of hoisting:
//Declaration is hoisted
// not assignment is hoisted
console.log(x);

var x =10;
// output : undefined


QUADB Company:
1)
The expression console.log(5 < 6 < 2); might not behave as expected due to how JavaScript handles the comparison operators.

Let's break it down:

5 < 6 evaluates to true because 5 is less than 6.
Now, you have true < 2.
In JavaScript, when you use the less-than operator (<) with non-numeric values (like comparing a boolean to a number), JavaScript will try to convert the non-numeric value to a number. In this case, true is converted to 1 and then compared to 2.

So, effectively, you have 1 < 2, which is true.

Therefore, console.log(5 < 6 < 2); will output true to the console.

2) 
In JavaScript, the || operator is the logical OR operator. It returns the first truthy operand, or the last operand if none are truthy.

In the expression console.log(0 || 6);, the || operator will return the first truthy value, and if none are truthy, it will return the last operand.

In this case, 0 is a falsy value in JavaScript, so the expression evaluates to the second operand, which is 6. Therefore, the output of console.log(0 || 6); will be 6.

3) Event Loop: https://youtu.be/lqLSNG_79lI?si=aLR_eSZMG5xjHhwi

4) Callback function : https://youtube.com/shorts/xYwynxs70yw?si=PLTSA3sOzynnNCu3

5)A parameter is one of the variables in a function. And when a method is called, the arguments are the data you pass into the method's parameters.

css position property:
https://youtu.be/UOPthZvCb9s?si=5g26O5-2nrAfXXQJ
