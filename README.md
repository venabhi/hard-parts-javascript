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

# CALL STACK
call stack in js will track where my js are in and what line of exec
it will tells the state of the js
call stack ios special data structure and it will start with global exec()
normally when we call it will push to call stack to track
if we call a func then local exec will be placed on top of global exc once it don 
it will come back to global exec once it done with local exec / var environment
what function we are calling now and where to return after done 
global exe context have multiple function exec.

# functional programing
a function is a first class citizen it has two type  fun def and exc
mainly, pure func is called it has no side effectc and shd not break polocies
function prg is a structure of the program with no breaking polocies
we sbd use the same func repeteadly times by times by calliong a function with an argument and input 
if we are using the func repetedly, we are not giv any parameters/inputus simply give placeholders like num and return num*num
function squarenum () {
   return num*num,
}

<!-- repedetdly using functions -->
function squareNum (num) {
   return num*num;
}
const output = squareNum(10);
const output = squareNum(9);

