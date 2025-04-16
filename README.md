# JavaScript-Notes

## 1. Basics

### Variables

It is like we put label over a box where we store our data and Whenever we need that data we simply start looking that box with the label name

__Variables(Boxes) while naming variables there are few convention to follow :__

* Cannot be a reserved keyword
* SHould be meaningful
* Cannot start with a number
* They cannot contain a space or hypen
* Are Case-sensitive

### Constants

JavaScript provides three ways to declare variables: var, let, and const, but they differ in scope, hoisting behaviour, and re-assignment rules. Understanding these differences helps write more predictable and maintainable code. 

* __var__ is very often and you saw in the old codes and the chances of error happening or bug inside your code is very high.
* __let__ this is mostly used now a days because this is less prone to error inlike var keyword
* __const__ this is const keyword where if you declare with any kind of name then these declare name cann't reassign to another variable and You are not going to change it's value.

### Primitive Types / Value Type & Reference Types

__Here we are mainly focused on primitives Types and talk about Reference Types later__ 

There are few Primitives Types

* String
* Number
* Boolean
* undefined
* null

```
let name = 'Mosh'; // String Literal (Another Fancy Name of String)

let age = 30; // Number Literal

let isApproved = true; // Boolean Literal (__We use this logic e.g Orders need to be approved for shipped__)

let firstName; OR let firstName = undefined; (__If we don't define this variable then this automatically define undefined__)

let lastName = null;  (__We Used Explicitly To Clear value of any variable__).
```
__In ES6 we have another primitive type called Symbol which we have later in this course__

### Typing

Javascript is a dynamic language. Generally we have two types of languages

1. Static Languages ( __In Static languages, the type of the variable is set and it cannot be changed in the future e.g string name = 'John'__ ) 
2. Dynamic Languages.( __In Dynamic languages, the type of the variable is not set and it can be changed in the runtime in the future e.g let name = 'John' after running ( name = 1; )__ )

__Properties__

* In JS there are only one type of number no any kind of __floating Point number.__
* The firstname ( which is set to undefined in above exampple ) it's value is undefined and it's type is also undefined.
* in above example lastName value is object.

> Example : let lastName = null (typeof null is object) Which we are going to talk.

### Object

* __Object is a Reference Type__

An Object in JS and Other Programming languages is like an object in real life. Think of a person it's name, age, height and weight these are properties of one person.So When we dealing multiple realted variables, we can put these variables inside of an object.It makes our code cleaner.

 ``` 
 Example: let person = {
    name : 'Ravi',         (In the form of Key-Value Pair) 
    age: 30
 }
 ```
 * __Now there are two ways to access and change key-value pair inside object__

 1. Dot Notation ( person.name = 'John' Change it's value )
 2. Bracket Notation ( person['name'] = 'Mary'; )

__Now Question arise which method is better ?__

As you would see dot notation is sort so that should be your default choice however, Bracket Notation has it's own uses, sometimes, you don't know the name of the target property until the run time.

``` 
Example: The user might be selecting the name of the target property. In that case, in the time of writing code, we don't know what property we're going to access. That is going to be selected at the runtime by the user. So we might have another variable somewhere else like selection, that determines the name of the target property that the user is selecting, and that can change at run time. With this,we can acess that property in a dynamic way.So, we pass 

let person = {
    name: 'Mosh',
    age:30
};

// Dot Notation
person.name = 'John';

// Bracket Notation

let selection = 'name';    <--- 
person[seletion] = 'Mary'
```
**We can access object key value through bracket notation at the run time**

### Arrays

