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

# pair programming

it will help to reduce the complex code and a couple of dev will work to improve the efficient of code.

#  higher order function & paramaterizing functions
we have a function copyarrayandmultiplyby2

function copyArrayAnsMultiplyBy2 (array) {
   <!--  in the array parameter we are giving newarray arguments1,2,3 -->
   let output = []    here output is an empty array because once the exe all the op values will store in the op []
   for (let i=0; i<array.length; i++) {
           output.push(array[i] *2);           thus is the code we are run and also push the output the empty out [] using output.[push] 
   }  we are giv expression and .len is leng of array like how many argument in array here, array[i] so, it will start with first arg 1
   return output;
   <!--  so, finally we are returning the output array to the global exc which is result -->
} 
const newarray = [1,2,3];
let result = copyarrayansmultiplyby2(newarray)

# generalizing functions
we shd reuse the function times and times only adding parameter

function copyarraymanipulate (array, instructions) {       here, instructions = baby function = complete def of function 
   let output = [];
   for (let i=0; array.length<0; i++) {
     output.push(instructions( array[i]);   here combine parameter in struction to normal array index 

   }
   return output;
}

function divideby2 (input) {    here, input is array[index]s
       return input / 2;
}
<!--  finally it will push all the output to tthe label resul of copyarray -->
let result = copyarraymanipulate([1,2,3], dividby2)

finally we done with principle, execution context, high-order functions, callback , baby functions...etc


<!--  example calling a fun with arg -->

function instructiongen () {
   function multiby2 (num) {
      return num*2;
   }
   return multiby2;
}

let genfun = instructiongen();
let result = genfun(3)

<!--  closure without retun the dec fun inside  because we are declaring counter in global so we will return the dec fun outside  -->
function outer () {
   let counter = 0;
   function incrementc () {
      counter ++;
   }
   return incrementc;
}
let newfun = outer ()  or newfun = incrementc

<!--  what happen if we exc newfun again -->
newfun();    it will look on to the global 

using counter/closure it will store the backpack information it will take the old value and increase the value

function  outer () {
   let counter = o;
   function inc () {
      coonter++;
   }
   return inc;
}
var newfun = outer()

WHAT HAPPENS WHEN JAVASCRIPT EXECUTES MY CODE?

const num = 3;
function multiplyby2 (inputnumber) {
   result= inputnumber*2;
   return result;
}
1. once we start running code we create a global execution context;
in a global execution context, thread of exe/ sync thread of execution will takes place that means executes line after line'
in a global exe context, there is a global variable environment that means all the data will be stored.

# web browser 

features: 
timer = lables for timer is settimeout
HTML DOM - label for dom in web browser is doccument = doccumrnt.getele
network req = label is fetch/xhe
consoloe = console is the label 

these all the browser features js is contacting wit the browser

# setTimeOut

function printhello () {
   console.log('hello');
}
setTimeout(printhello, 1000);   after 1000 msec web browser will call the func printhello and print result on web
console.log('me first');

function printhello () {
   console.log('hello');
}

setTimeout (printhello, 0);

blockFor1scc ()
console.log('me first')
<!--  event loop will check any callback ques fun are waiting and it will call the function this is async js -->\

# promisess
promises are like js object it work with fetch 
fetch will be used to grab the data if u fetch it will divide in to 2 prongs 
1 prong will work with web backend it will contact with n/w collect tghe data send to java script 
then, another prong will the data from web it will store on the promises object  value proprty in js. assig to the var.
promise object has vale and aray properties
function display (data) {
   console.log(data)
}
const tdata = fetch('url);
tdata.then(display);

promise = value and big array 
once data sent to promise and stored in values it will trigger the array to run a function 

const tdata - fetch(url)
tdata.then (display)

<!--  promises async and eventloop  -->
function dispay(data) {
   console.log(data)
}
function printhello () {
   console.log('hello)
}
function block () {

}

setTimeout(printhello, 0);

const newdata = fetch ('url')
newdata.then(display)

newdat.catch() error handeling
blockFor() 

# oop
declaring an obj and binding properties and function

const user1 = {
   name = "abhi";
   score = 7;
   increment = function () {
      score++;
   }
};l
user1.name();
user1.increment();


declare a empty function and assigning a parameters

const user2 = ();

user2.name = "abhi";
user2.score = 5;
user2.increment = function () {
   user2.score++;
};

create user3 using object.create

const user3 = object.create(null);

user2.name = "abhi";
user2.score = 5;
user2.increment = function () {
   user2.score++;
};

<!--  how to resuse the object using generalise function -->
create the object and use many times we can by using generalise function
generate a object with a function then we can use many times.

function createuser (name, score ) {
   const newuser = () ;
   newuser.name = name;
   newuser.score = score;
   newuser.increment = function () {
      newuser.score++
   }; 
  return newuser;
}
const user1 = createuser('abhi', 5);
const user2 = createuser('ram', 5);
user1.increment()
user2.increatement();

# prototype chain
prototype chin = object.create
this type will help to store all the fun in a function inside 

function createuser (name, score) {
   const newuser = object.create(userinfostore);
   newuser.name = 'abhi';
   newuser.score = 5;
};
const userinfo = () {
   increatment = function () {
      this.score++;
   };
   login = function () {
      console.log("logged on");
   }
}


