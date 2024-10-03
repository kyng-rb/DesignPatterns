## Builder

Problem:
Imagine a complex object that requires laborious, step-by-step initialization of many fields and nested objects. Such initialization code is usually buried inside a monstrous constructor with lots of parameters that in most cases will be unused, making the constructor calls pretty large and ugly. Or even worse: object initialization scattered all over the client code.

Solution:
Builder aims to add flexibility, verbosity and a centralized mechanism for performing the construction of complex objects, detaching it from the real object representation(This is possible by providing a step by step - AKA fluent - interface).

References:
 * [Source Making](https://sourcemaking.com/design_patterns/builder)
 * [Refactoring Guru](https://refactoring.guru/design-patterns/builder)