# 30-Days-Of-javascripit-
1. create-hello-world-function 
 /**
 * @return {Function}
 */
var createHelloWorld = function() {
    
    return function(...args) {
     return "Hello World"   
    }
};

/**
 * const f = createHelloWorld();
 * f(); // "Hello World"

 */
 2. Counter
 /**
 * @param {number} n
 * @return {Function} counter
 */
var createCounter = function(n) {
    
    return function() {
        return n++
    };

}; 
3.to-be-or-not-to-be
var expect = function(val) {
    return {
        toBe: (val2) => {
            if (val !== val2) throw new Error("Not Equal");
            else return true;
        },
        notToBe: (val2) => {
            if (val === val2) throw new Error("Equal");
            else return true;
        }
    }
};
4.Counter-ii
function createCounter(init) {
    let current = init;
    
    return {
        increment: function() {
            current += 1;
            return current;
        },
        decrement: function() {
            current -= 1;
            return current;
        },
        reset: function() {
            current = init;
            return current;
        }
    };
}
5.apply-transform-over-each-element-in-array
/**
 * @param {number[]} arr
 * @param {Function} fn
 * @return {number[]}
 */
var map = function(arr, fn) {
      for(let i=0;i<arr.length;i++){
        arr[i]=fn(arr[i],i);
    }
    return arr
};
