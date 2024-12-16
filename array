'use strict';

const array = () => {
  const arr = [];
  const obj = (i) => arr[i];
  obj.push = (el) => {
    arr.push(el);
    return arr;
  };
  obj.pop = () => arr.pop();
  return obj;
};

const myArray = array();

myArray.push('first');
myArray.push('second');
myArray.push('third');

console.log(myArray(0));
console.log(myArray(1));
console.log(myArray(2));

console.log(myArray.pop());
console.log(myArray.pop());
console.log(myArray.pop());

module.exports = { array };
