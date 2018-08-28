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
