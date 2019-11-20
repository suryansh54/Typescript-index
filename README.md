# Typescript topics
All Typescript topics index

<ol>
  <li><a href="#what-is-typescript" title="What is TypeScript?">What is TypeScript?</a></li>
  <li><a href="#features-of-typescript" title="Features of TypeScript?">Features of TypeScript?</a></li>
  <li><a href="#why-use-typescript" title="Why Use TypeScript?">Why Use TypeScript?</a></li>
  <li><a href="#basic-types" title="Basic Types">Basic Types</a></li>
  <li><a href="javascript:;" title="Variable Declarations">Variable Declarations</a></li>
  <li><a href="javascript:;" title="Interfaces">Interfaces</a></li>
  <li><a href="javascript:;" title="Classes">Classes</a></li>
  <li><a href="javascript:;" title="Functions">Functions</a></li>
  <li><a href="javascript:;" title="Generics">Generics</a></li>
  <li><a href="javascript:;" title="Enums">Enums</a></li>
  <li><a href="javascript:;" title="Type Inference">Type Inference</a></li>
  <li><a href="javascript:;" title="Type Compatibility">Type Compatibility</a></li>
  <li><a href="javascript:;" title="Advanced Types">Advanced Types</a></li>
  <li><a href="javascript:;" title="Symbols">Symbols</a></li>
  <li><a href="javascript:;" title="Iterators and Generators">Iterators and Generators</a></li>
  <li><a href="javascript:;" title="Modules">Modules</a></li>
  <li><a href="javascript:;" title="Namespaces">Namespaces</a></li>
  <li><a href="javascript:;" title="Namespaces and Modules">Namespaces and Modules</a></li>
  <li><a href="javascript:;" title="Module Resolution">Module Resolution</a></li>
  <li><a href="javascript:;" title="Declaration Merging">Declaration Merging</a></li>
  <li><a href="javascript:;" title="JSX">JSX</a></li>
  <li><a href="javascript:;" title="Decorators">Decorators</a></li>
  <li><a href="javascript:;" title="Mixins">Mixins</a></li>
  <li><a href="javascript:;" title="Triple-Slash Directives">Triple-Slash Directives</a></li>
  <li><a href="javascript:;" title="Type Checking JavaScript Files">Type Checking JavaScript Files</a></li>
  <li><a href="javascript:;" title="Utility Types">Utility Types</a></li>
  <li><a href="javascript:;" title="tsconfig.json">tsconfig.json</a></li>
  <li><a href="javascript:;" title="SOLID principles">SOLID principles</a>
      <ul>
        <li><a href="javascript:;" title="Single responsibility principle">Single responsibility principle</a></li>
        <li><a href="javascript:;" title="Open-closed principle">Open-closed principle</a></li>
        <li><a href="javascript:;" title="Liskov Substitution principle">Liskov Substitution principle</a></li>
        <li><a href="javascript:;" title="Interface segregation principle">Interface segregation principle</a></li>
        <li><a href="javascript:;" title="Dependency inversion principle">Dependency inversion principle</a></li>
      </ul>
  </li>
</ol>

### What is TypeScript?
- TypeScript is an open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing to the language. TypeScript is designed for development of large applications and transcompiles to JavaScript.
- ECMAScript + ECMAScript6 + Additional Feature = TypeScript
- TypeScript is a typed superset of JavaScript compiled to JavaScript.

### Features of TypeScript?
- **TypeScript is just JavaScript.** TypeScript starts with JavaScript and ends with JavaScript. Typescript adopts the basic building blocks of your program from JavaScript. Hence, you only need to know JavaScript to use TypeScript. All TypeScript code is converted into its JavaScript equivalent for the purpose of execution.
- **TypeScript supports other JS libraries.** Compiled TypeScript can be consumed from any JavaScript code. TypeScript-generated JavaScript can reuse all of the existing JavaScript frameworks, tools, and libraries.
- **JavaScript is TypeScript.** This means that any valid .js file can be renamed to .ts and compiled with other TypeScript files.
- **TypeScript is portable.** TypeScript is portable across browsers, devices, and operating systems. It can run on any environment that JavaScript runs on. Unlike its counterparts, TypeScript doesn’t need a dedicated VM or a specific runtime environment to execute.

### Why Use TypeScript?
- **Compilation** − JavaScript is an interpreted language. Hence, it needs to be run to test that it is valid. It means you write all the codes just to find no output, in case there is an error. Hence, you have to spend hours trying to find bugs in the code. The TypeScript transpiler provides the error-checking feature. TypeScript will compile the code and generate compilation errors, if it finds some sort of syntax errors. This helps to highlight errors before the script is run.
- **Strong Static Typing** − JavaScript is not strongly typed. TypeScript comes with an optional static typing and type inference system through the TLS (TypeScript Language Service). The type of a variable, declared with no type, may be inferred by the TLS based on its value.
- **TypeScript supports type definitions** for existing JavaScript libraries. TypeScript Definition file (with .d.ts extension) provides definition for external JavaScript libraries. Hence, TypeScript code can contain these libraries.
- TypeScript supports **Object Oriented Programming** concepts like classes, interfaces, inheritance, etc.

### Basic Types
<ol>
  <li><a href="#boolean" title="Boolean">Boolean</a></li>
  <li><a href="#number" title="Number">Number</a></li>
  <li><a href="#string" title="String">String</a></li>
  <li><a href="#array" title="Array">Array</a></li>
  <li><a href="#tuple" title="Tuple">Tuple</a></li>
  <li><a href="#enum" title="Enum">Enum</a></li>
  <li><a href="#any" title="Any">Any</a></li>
  <li><a href="#void" title="Void">Void</a></li>
  <li><a href="#null-and-undefined title="Null and Undefined">Null and Undefined</a></li>
  <li><a href="#never" title="Never">Never</a></li>
  <li><a href="#object" title="Object">Object</a></li>
  <li><a href="#type-assertions" title="Type assertions">Type assertions</a></li>
</ol>

#### Boolean

```javascript
let isDone: boolean = false;
```

#### Number

```javascript
let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;
```

#### String

```javascript
// Example - 1
let color: string = "blue";
color = 'red';

// Example - 2 (You can also use template strings, which can span multiple lines and have embedded expressions.)
let fullName: string = `Bob Bobbington`;
let age: number = 37;
let sentence: string = `Hello, my name is ${ fullName }.

I'll be ${ age + 1 } years old next month.`;
```

#### Array

```javascript
let list: number[] = [1, 2, 3];

// OR Generic array type
let list: Array<number> = [1, 2, 3];
```

#### Tuple

```javascript
// Declare a tuple type
let x: [string, number];
// Initialize it
x = ["hello", 10]; // OK
// Initialize it incorrectly
x = [10, "hello"]; // Error

console.log(x[0].substring(1)); // OK
console.log(x[1].substring(1)); // Error, 'number' does not have 'substring'
```

#### Enum

```javascript
enum Color {Red, Green, Blue}
let c: Color = Color.Green;

enum Color {Red = 1, Green, Blue}
let c: Color = Color.Green;
```

#### Any

```javascript
let notSure: any = 4;
notSure = "maybe a string instead";
notSure = false; // okay, definitely a boolean
```

#### Void

```javascript
/* void is a little like the opposite of any: the absence of having any type at all. You may commonly see this as the return type of functions that do not return a value:*/

function warnUser(): void {
    console.log("This is my warning message");
}
```

#### Null and Undefined

```javascript
// Not much else we can assign to these variables!
let u: undefined = undefined;
let n: null = null;
```

#### Never
The never type represents the type of values that never occur. For instance, never is the return type for a function expression or an arrow function expression that always throws an exception or one that never returns; Variables also acquire the type never when narrowed by any type guards that can never be true.

```javascript
// Function returning never must have unreachable end point
function error(message: string): never {
    throw new Error(message);
}

// Inferred return type is never
function fail() {
    return error("Something failed");
}

// Function returning never must have unreachable end point
function infiniteLoop(): never {
    while (true) {
    }
}
```

#### Object
object is a type that represents the non-primitive type, i.e. anything that is not number, string, boolean, bigint, symbol, null, or undefined.
```javascript
declare function create(o: object | null): void;

create({ prop: 0 }); // OK
create(null); // OK

create(42); // Error
create("string"); // Error
create(false); // Error
create(undefined); // Error
```

#### Type assertions
Sometimes you’ll end up in a situation where you’ll know more about a value than TypeScript does. Usually this will happen when you know the type of some entity could be more specific than its current type.

Type assertions are a way to tell the compiler “trust me, I know what I’m doing.” A type assertion is like a type cast in other languages, but performs no special checking or restructuring of data. It has no runtime impact, and is used purely by the compiler. TypeScript assumes that you, the programmer, have performed any special checks that you need.

Type assertions have two forms. One is the “angle-bracket” syntax:

```javascript
let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;

let someValue: any = "this is a string";

let strLength: number = (someValue as string).length;
```

#### 5. Variable Declarations

Declaring a variable in JavaScript has always traditionally been done with the var keyword.

```javascript
var a = 10;
```
We can also declare a variable inside of a function:

```javascript
function f() {
    var message = "Hello, world!";

    return message;
}
```
and we can also access those same variables within other functions:

```javascript
function f() {
    var a = 10;
    return function g() {
        var b = a + 1;
        return b;
    }
}

var g = f();
g(); // returns '11'
```

```javascript
function f() {
    var a = 1;

    a = 2;
    var b = g();
    a = 3;

    return b;

    function g() {
        return a;
    }
}

f(); // returns '2'
```

##### Scoping rules
var declarations have some odd scoping rules for those used to other languages. Take the following example:

function f(shouldInitialize: boolean) {
    if (shouldInitialize) {
        var x = 10;
    }

    return x;
}

f(true);  // returns '10'
f(false); // returns 'undefined'

##### Variable capturing quirks

For those unfamiliar, setTimeout will try to execute a function after a certain number of milliseconds (though waiting for anything else to stop running).
```javascript
for (var i = 0; i < 10; i++) {
    setTimeout(function() { console.log(i); }, 100 * i);
}
// Output 10 times 10
```

- Every function expression we pass to setTimeout actually refers to the same i from the same scope.
- Let’s take a minute to consider what that means. setTimeout will run a function after some number of milliseconds, but only after the for loop has stopped executing; By the time the for loop has stopped executing, the value of i is 10. So each time the given function gets called, it will print out 10!

A common work around is to use an IIFE - an Immediately Invoked Function Expression - to capture i at each iteration:

```javascript
for (var i = 0; i < 10; i++) {
    // capture the current state of 'i'
    // by invoking a function with its current value
    (function(i) {
        setTimeout(function() { console.log(i); }, 100 * i);
    })(i);
}
```

#### let declarations

```javascript
let hello = "Hello!";
```
When a variable is declared using let, it uses what some call lexical-scoping or block-scoping. Unlike variables declared with var whose scopes leak out to their containing function, block-scoped variables are not visible outside of their nearest containing block or for-loop.

```javascript
function f(input: boolean) {
    let a = 100;

    if (input) {
        // Still okay to reference 'a'
        let b = a + 1;
        return b;
    }

    // Error: 'b' doesn't exist here
    return b;
}

f(true) // 101
f(false) // b is not defined
```

Here, we have two local variables a and b. a’s scope is limited to the body of f while b’s scope is limited to the containing if statement’s block.

Variables declared in a catch clause also have similar scoping rules.

```javascript
try {
    throw "oh no!";
}
catch (e) {
    console.log("Oh well.");
}

// Error: 'e' doesn't exist here
console.log(e);
```

```javascript
a++; // illegal to use 'a' before it's declared;
let a;
```

```javascript
function foo() {
    // okay to capture 'a'
    return a;
}

// illegal call 'foo' before 'a' is declared
// runtimes should throw an error here
foo();

let a;
```
##### References
- <a href="https://www.typescriptlang.org/docs/home.html " title="Typescript documentation">Typescript documentation</a>
- <a href="https://samueleresca.net/2016/08/solid-principles-using-typescript/" title="SOLID principles">SOLID principles</a>
