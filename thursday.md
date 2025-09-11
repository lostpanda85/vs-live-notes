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

Note: *This was a demo heavy session*

### Voice-First Revolution

* Trends
  * Voice interfaces become standard way to interface with consumer devices
  * Growing demand for hands-free interactions
  * Real-time AI enables natural conversational experiences
* Advantages
  * REduces conative load
  * Improves accessibility
  * Enables hands-free operations

### Real World Apps

* Customer Service
  * Automate call centers and support centers
* Education
  * Language learning and interactive tutoring
* Enterprise
  * Meeting transcriptions, voice commands
* Healthcare
  * Patient intake, medical documentation
* Repair Services
  * Hands-free parts ordering, live help, guidance

### What we're covering (Demos)

* Language Coach
  * Interactive pronunciation practice
  * Real-time feedback on speaking
  * Multiple language support
* Medical for assistant
  * Voice to form data entry
  * Structured JSON extraction
  * Natural Conversion Interface

## Technical Debt is not free

* Chad Green

### Topics

* What is Tech Debt?
* Pros and Cons of Tech Debt
* What causes tech debt
* Identify Tech Debt
* Track Tech Debt

### What is Tech Debt?

* Ward Cunningham in 1992 coined the concept
* Danger occurs when debt is not repaid
  * Every minute on not quite right code is interest on that debt
* Term comes from Martin Fowler
  * Quick and dirty way sets us up for tech debt
  * Which incurs interest payment, extra effort in future development
* Deficient code that introduces risk in the form of time, security, morale, and other forms
  * Typically the rest of poor decision making

### Pros and Cons of Tech Debt

* Tech debt can be devastating
  * Degradation of quality
  * Limits ability to innovate
  * Longer development cycles
  * Less responsive to market changes
  * Customer churn
  * Dev churn
  * Higher upgrade costs
  * System compatibility issues
  * Poor end-user experience
  * Poor IT Morale
* Tech debt can be useful
  * Sometimes taking that debt can get us out the door sooner
  * Short term competitive advantage
  * New features faster
  * Short term capital preservation
  * Faster speed to marker

### What Causes Tech Debt

* Insufficient up-front definition
  * Poor requirements
  * Not enough questions asked
* Business pressures
* Lack of Process or Understanding
  * Could be industry best practices
* Tightly-coupled components
* Lack of test suites
* Lack of Documentation
  * Relevant documentation
* Lack of collaboration
* Parallel Development
* Delayed refactoring
* Lack of alignment to standards
* Lack of knowledge
* Lack of ownership
* Poor technical leadership
* Last minute specification changes

#### Types of Technical Debt

* Flawed Architecture
* Build debt
* Flawed Code
  * This is most tech debt
* Defects (Bugs)
* Flawed Design
* Poor/Stale/Over Documentation
* Infrastructure
* People
* Flawed Process
* Bad Requirements
* Services
* Inadequate Test Automation
* Tests

### Identify Tech Debt

* Code Quality
  * Clear Code
  * Maintainable?
  * Proper Documentation
  * Are we refactoring?
  * Well-Tested
  * Efficiency
    * Get it working first
    * Make it better afterwards
* Technical Deficiencies
  * Has someone else coded this?
  * Are user experiences consistent?
  * Are solutions using the same reusable frameworks?
  * Are best practices being followed?
  * Are deployments taking too long?
  * Are limits being exceeded or users seeing errors?
* Business Misalignment

### Opportunities to Identify Debt

* While coding
* Code review
* Code Analysis tools
  * Tooling is built into Visual Studio
* Pull Requests
* Stand Ups
* Sprint Review
  * May not be the best place due to stakeholders being present
* Look for them! Usually hidden in plain sight.

### Record Tech Debt

* User Story
* Product Backlog Item
* Requirement on a future story
* Issue
* NOT A BUG

#### What to record?

* Problem statement
  * Be careful with wording
  * Use business jargon
* Story Points (Hours)
* Criticality
* Complexity
* Reward (Business value)
* Remediation Cost

### Track Technical Debt

* Consider making a tech debt register with all the info to track
* Add a tech debt score

#### Tech Debt Score

* Consider using the following calculation

`(r x .2) + (CR x .15) - (CO x.15)`

R: Reward\
Cr: Criticality\
Co: Complexity

#### Tech Debt Ratio

* Consider the following calculation for scoring multiple products and systems

`(Remediation Cost / Development Cost) * 100%`

* Greater than 5%? take care of it!
* Less than 5%? Maybe not needed

## Writing Modern CSharp

* Jason Bock

[Demo Repo for this Session](https://github.com/jasonbock/writingmoderncsharp )

```text
"Warnings are errors that lack conviction"
  - Unknown Microsoft Employee
```

```text
"Regex syntax is like someone threw up on your code"
  - Jason Bock
```

### Overview

* Language Evolution
* Modern C# features
* Call to action

### Language Evolution

* Released in 2002
* Object Oriented, Component Based
* Added Roslyn (Compiler API) in 2012
  * Compiles C# in C#
  * THE .Net Compiler Platform
  * Fully moved over in 2015
* After Roslyn integration, C# gains 2-3x more features

### Modern CSharp Features

* `slnx` files are much cleaner than `sln` files
  * `dotnet sln MySolutionFile.sln migrate` performs the migration
* `.editorconfig` files
  * Provides code styling rules
  * Treat warning as errors
* A `Directory.Build.Props` file along side the solution
  * Sets project build properties for all projects in solution, like analysis mode
  * Set default framework
  * Language Version
* A `Directory.Packages.props` file along side the solution
  * Controls all nuget packages for all projects in the solution
  * Overridable at the project level
* Tuples work in constructor property assignments
* [Ligatures](https://www.c-sharpcorner.com/article/writing-code-with-ligatu/) `=>`, its a font. Its still a fat arrow.
* Verbatim string, multi literal string that is printed exactly as defined
* Raw string literals, a string that has three `"` double quotes
  * Lines up the gutter
  * Dollar Signs and Quotes can change where the literal starts
    * Ads ability to add quotes to property names
* Patterns
  * Matches patterns
* `ThrowIf` syntax makes null checking easy and throws a error
* `init` over `set` so that a property can be set only during construction
  * Might need a `[SetsRequiredMembers]` decorator on the class definition
* `record` can be `class` or `struct`
  * Syntax sugar over a type
  * Useful for database extraction
  * Useful for messages
* Source Generators
  * Sets up a given type
  * Can be used to provide mock objects for testing
  * Can also help with Reflection issues
  * AOT friendly

### Call To Action

* C# will continue development at its current pace
* C# 14 due in about 2 months with 11 new features
* C# 15 is slotting 9 new features, but its still in flux
* Follow the roadmap!
* Study!

## Analyzing Code in .Net

* Jason Bock

```text
"There are a finite number of keystrokes left in your hands before you die" 
  - Scott Hanselman
```

Note: *This feels like ESLint*

Note: *This was a demo heavy session*

[Sample Analyzer](https://github.com/jasonbock/transpire)\
[2nd Repo for this session](https://github.com/JasonBock/AnalyzingCodeInDotNet)

### Contents

* Analysis
* Building
* Call to Action

### Analysis

* Analyzers Comes from Roslyn (Compiler API)
* Tons of tools exist to help (See slides for list)
* Analyzer warnings/errors can be suppressed if needed

### Building

Check Slides and Repo
