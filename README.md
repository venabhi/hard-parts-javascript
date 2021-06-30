# HARD-PARTS-JAVASCRIPT

WHAT HAPPENS WHEN JAVASCRIPT EXECUTES MY CODE?

const num = 3;
function multiplyby2 (inputnumber) {
   result= inputnumber*2;
   return result;
}
const output = multiplyby2(4);
const newoutput = multiplyby2 (10);

1. once we start running code we create a global execution context;
in a global execution context, thread of exe/ sync thread of execution will takes place that means executes line after line'
in a global exe context, there is a global variable environment that means all the data will be stored.

in line 10 we calling a function with an argument/inputvalue and assign to the variable = output 
in global, local exec context will create in a local memory , input value = 4 and result = 8 
after returning , the result will go to the global execution context
