# Design pattern general notes

## What is a Design pattern?

A design pattern is a blueprint for solving common problems in software design. In context, in software development, we often encounter recurring challenges, such as resource management, readability, or maintenance. Many of these issues are well-known, along with proven guidelines for addressing them — these guidelines are referred to as design patterns.

## Why to learn?

Design patterns provide tested solutions, helping prevent potential issues and avoid reinventing the wheel. They also improve code readability, ease maintenance, and establish a common language among developers.

## Utility - Classification

There are three kind of design patterns, classification was made by the problem they solves:

### Creational
  * Creational design patterns abstract the instantiation process. They help make a system independent of how its objects are created, composed, and represented.
    * Abstract Factory
    * Builder
    * Factory Method
    * Object Pool
    * Singleton
    * Prototype -> https://sourcemaking.com/design_patterns/prototype/java/1

### Structural
 * Structural Design Patterns are concerned with how classes and objects are composed to form larger structures, it describe ways to compose objects. The added flexibility of object composition comes from the ability to change the composition at run-time.
    * Adapter
    * Bridge
    * Composite
    * Decorator
    * Facade
    * Flyweight
    * Private Class Data
    * Proxy

### Behavioral
 * A behavioral design pattern is a way to organize how different parts of a software system interact with each other. These patterns focus on how objects or classes communicate and work together, making it easier to manage and change the code.
    * Chain of responsibility
    * Command
    * Interpreter
    * Iterator
    * Mediator
    * Memento
    * Null Object
    * Observer
    * State
    * Strategy
    * Template method
    * Visitor