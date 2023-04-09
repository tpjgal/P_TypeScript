# TypeScripts 


## Install Node.js 

https://nodejs.org 


## Check Version 

node --version



## Create a Directory 

mkdir hello-ts

## Create a file 
index.ts



## Terminal 

npx --package typescript tsc -- help 

npx --package typescript tsc --outDir dist index.ts 


## Installing TypeScripts

npm init -y

npm install typescript --save-dev 



version 

node -v
npm -v 

npm install typescript -g

-g means a gloabl installtion 

tsc -v 


## Building 

"tsc" : "tsc"

npm run tsc -- --init

see the target in tsconfig.json 

target : Es2016 
SourceMap : true
OutDIr : ./dist 
moduleResolution  : true



npm run tsc 

npm start 

================

npm install

npm start 

========


## Debugging

npm start 

Open Developer Tools  from broswer  ( More Tools -> Developer Tools) 
Open file   
eg. 2gettingstart/index 



=================


```
test.ts:
 function hello(name: string): void {
 console.log(`hello, ${name}!`);
 }
 
 hello('world');
 
 ```
 
 tsc test.ts
 
 node test.js
==========================


## TypeScript Getting Started

TypeScript Compiler

TypeScript being converted into JavaScript means it runs anywhere that JavaScript runs!

### Installing the Compiler
TypeScript has an official compiler which can be installed through npm.
```
npm install typescript --save-dev
```
The compiler is installed in the node_modules directory and can be run with: npx tsc.
```
npx tsc
```

### Configuring the compiler
By default the TypeScript compiler will print a help message when run in an empty project.

The compiler can be configured using a tsconfig.json file.

You can have TypeScript create tsconfig.json with the recommended settings with:
```
npx tsc --init
```
Which should give you an output similar to:

Created a new tsconfig.json with:
TS
  target: es2016
  module: commonjs
  strict: true
  esModuleInterop: true
  skipLibCheck: true
  forceConsistentCasingInFileNames: true


=================

## TypeScript Simple Types


TypeScript supports some simple types (primitives) you may know.

There are three main primitives in JavaScript and TypeScript.

boolean - true or false values
number - whole numbers and floating point values
string - text values like "TypeScript Rocks"

### Type Assignment
When creating a variable, there are two main ways TypeScript assigns a type:

Explicit
Implicit


Explicit Type
Explicit - writing out the type:

```
let firstName: string = "Dylan"; // type string

console.log(typeof firstName);

```
Implicit Type
Implicit - TypeScript will "guess" the type, based on the assigned value:

```
let firstName = "Dylan";

console.log(typeof firstName);
```

Note: Having TypeScript "guess" the type of a value is called infer.



Error In Type Assignment
TypeScript will throw an error if data types do not match.

```
let firstName: string = "Dylan"; // type string

firstName = 33; // attempts to re-assign the value to a different type

console.log(firstName);


let firstName: string = "Dylan"; // type string

firstName = 33; // attempts to re-assign the value to a different type

console.log(firstName);

```

Unable to Infer
```
// Implicit any as JSON.parse doesn't know what type of data it returns so it can be "any" thing... 
const json = JSON.parse("55");

// Most expect json to be an object, but it can be a string or a number like this example
console.log(typeof json);

```