# TYPESCRIPT HOMEWORK

TypeScript is a free, open-source programming language that runs on any operating system.

_Compiled languages_ are languages whose source code must be "translated” before it can run. The developer writes the source code, then something called a _compiler_ translates it into code the client (a browser, in our case) can understand.

_REMEMBER_ always link to .js in index. !!! NOT .ts !!!

### SETUP

I. Install TypeScript globally via npm.

```
$ npm install typescript -g
```

II. Install Atom TypeScript Package. Helps Atom in recognizing and properly highlighting TypeScript code.

```
$ apm install atom-typescript
```

III. Compile TypeScript file. (tsc: TypeScript compiler.)

* _method signature_ is the combination of the method’s name and parameter list.

```
$ tsc app/hello.ts
```

IIII. Use Node.js to execute file from command line:

```
$ node hello.js
```

***

* To install TypeScript, Node.js and npm must be successfully installed first.

* If npm has been installed correctly, there is little chance for error installing TypeScript.

### CODE NOTES

#### Declaring data types.

```
var greeting: string = "Hi TypeScript";
```

: string is TypeScript's _optional typing_ feature.

* A language is loosely typed if it doesn't require variables to define their data type (ie: String, Integer, etc.) upon creation.

***

#### Classes.

* Class names _always begin_ with a capital letter, followed by {}.

*Properties.*

* Description: _string_ describing task.
* Priority: _string_ info on urgency. ("High", "Low", or "Medium")
* Done: contains _boolean_ on whether Task is complete.

```
class Task {
  done: boolean;
  description: string;
  priority: string;
}
```

***

#### Constructors.

Constructor method to instantiate new _Tasks._


Constructor method takes two parameters:
1. descriptionParameter
2. priorityParameter


Does not require _done_ property info because all Task objects begin as false.


```
constructor(descriptionParameter: string, priorityParameter: string){
 this.done = false;
 this.description = descriptionParameter;
 this.priority = priorityParameter;
}
```

***

#### Access Level Modifiers
The term _public_ before a var or property means that any part of the app can access this property. TypeScript has permission to auto access and assign it to class properties.

_modifier or access-level modifier_
* private
* protected
* public

```
class Task {
  done: boolean;
  description: string;
  priority: string;


   constructor(public description: string, public priority: string){
    this.done = false;
  }
...
```

If constructor() parameters share the *exact same name* as class properties (like description, or priority in the example above), TypeScript will automatically assign them to a public property of the same name and type.


SO:


```
class Task {
  done: boolean;

  constructor(public description: string, public priority: string){
    this.done = false;
  }

...

}
```
