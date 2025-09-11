# Thursday

## TypeScript: Moving Beyond the Basics

* Allen Conway

### General

* [TypeScript is moving to Go](https://github.com/microsoft/typescript-go)
* @ts-node is a package that can run typescript code
  * `tsc --init` will setup the tsconfig file.
  * `ts-node <filename>` executes a script
* [Quokka](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode) provides realtime feedback
* [Demo App for this Session](https://github.com/AllenConway/TypeScriptDemoApp)

### Agenda

* Generics
* Extending Interfaces
* Declaration Merging
* Iterators, Generators
* Symbols
* Advanced Types
* Types and Interfaces
* Mapped and Conditional Types
* Satisfies Operator
* Mixins

### Generics

* Flexible types
* Type safe

### Extending Interfaces and Classes

* Provides flexibility
* Inherits members but not implementations in Classes
* Reduces duplicated code

### Declaration Merging

* Merge multiple declarations into a single one
  * Interfaces
  * Namespaces
  * Modules
* Ideal to create a union across types
* Control-Click will show all references of merged union types.

```typescript
/** Example of Merging */
interface a {
    a: number;
}

interface a {
    b: number;
}

let foobar: a = {
    a: 100,
    b: 100
}
```

You can also merge an interface into a class by merging without implementing the interface.

Global scope can also be merged into.

### Iterator & Generator

* Return index of the loop
* Generators generate an iterator and return it without explicitly defining it
* `yield` is a valid operator in a custom iterator
  * must use `*` before the function name to identify it doesn't really return a value

### Symbols

* Primitive data type
* Feature in ES6
* Not enumerable in `for in`, or `for of`
  * Use `Object.getOwnPropertySymbols` to iterate over collection
* Are unique, one cannot === another
  * This is to avoid collisions

### Advanced Types

* Intersections Types
  * Combines multiple types into one
* Union Types
* String or Numeric Literal Types
* Type Guards
  * Checks to see if the type coming into the method is of the type expected
* Nullable Types

### Types and Interfaces

* Provide data contract
* Type cannot be reopened
* Interfaces are extendable
* Types are unique

### Mapped and Conditional Types

* Partial
  * Allows types to be partially filled and used
* Readonly
  * Can be applied to the definition `Readonly<T>`
* Record
* `Pick`
* Exclude<T,U>
* `Include` adds additional types as needed
  * Helper type, `pick` handles everything needed
* Extract<T,U>
* `Omit` can remove members from a type

### Satisfies Operator

* Ensures an expression satisfies a given type without narrowing it
* Useful for enforcing required structure
* Less strict than interfaces

### Mixins

* Allows composition of partial classes
* Promote code reuse
* Create helpers to apply mixins
* Composites using the object constructor

## Real-Time AI: Take your Apps to the Next Level

* Dan Wahlin

## Technical Debt is not free

* Chad Green

## Writing Modern CSharp

* Jason Bock

## Analyzing Code in .Net

* Jason Bock
