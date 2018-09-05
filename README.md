Array Helpers

1. forEach
   
   var color = ['red', 'blue', 'green'];

   color.forEach(function(color){
     console.log(color);
   });

   forEach takes one function called iterator function as argument. This function iterates over each element in array and rexecute code inside the function. INstead of anonymous function we can also pass our own function inside the forEach.

2. map
   In map all elements are iterated one by one and the returned value is stored in a result array. If something is not returned  in the function, null is returned to the array.

   var numbers = [1, 2, 3];

   var double = numbers.map(function(num){
     return num*2;
   });

   //double[2, 4, 6]

3. filter
   Iterates through each element and check in iterator function required condition. If it returns true that element is included in result array else skipped. Don't forget return else empty array will return.

   var numbers = [2, 3, 8, 6, 7];

   var even = numbers.filter(function(num){
     return num%2 === 0;
   });

   // even[2, 8, 6]

 4. find
    Iterates the array and returns first element that matches the condition in iterator function.

    var students = [
      {name: 'Alex'},
      {name: 'Ashish'},
      {name: 'Jack'}
    ];

    var result = names.find(function(student){
      return student.name == 'Ashish';
    })  

5. every
   Iterates through all elements and return true if all elements in array returns true for some given condition.

6. some:
   Iterates through all elements and return true if at least one element in array returns true for some given condition.

7. reduce:
   Iterate through all elements, takes an argument and returns a condensed value by performing some operation.

   var numbers = [10, 20, 30]; 

   var getSum = numbers.reduce(function(sum, number){
     return sum + number;
   }, 0); //sum initial value is assigned 0

   //getSum = 60

   Const, let, var  

   const:
   Assign to variable whose value will never change

   let:
   Assign to variable whose value might change.

   var:
   never use it.

   Arrow Function:
    Remove the function keyword and put arrow on right of arguments.
    
    For functions having single JS expression remove the brackets, remove the return
    keyword and put it in the first line as shown below.
    
    // Without arrow functons
    const sum = function(a, b) {
      return a + b;
    }

    // With arrow functions
    const sum = (a, b) => a + b;

    In case there is only one argument passed to the function remove parentheses around it.

    Arrow functions bind the value of 'this' to the surrounding context.

    Consider the following function:

    const videoList = (props) => {
      const video = props.video;
      console.log(video);
    }

    This can be written as:

    const videoList = ({video}) => {
      console.log(video);
    }
    
    The above is possible due to ES6 syntax which says first object in the argument has a property video. Grag that property and assign it to variable video.

const:
  const is immutable except when used with objects.
  var is avoided because it is hoisted whereas const and let
  are blocked space i.e. they are only available within its block.
  