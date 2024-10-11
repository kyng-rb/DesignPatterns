## Factory method

Problem:
We have a service that implements specific business logic. However, depending on the case, the service needs an instance of a particular family of classes. As complexity grows, the family of classes expands with more members. As a result, the logic for deciding which class to instantiate gets updated frequently, making the main service error-prone and dependent on every member of the family. This situation becomes even worse when the constructors are complex.

There are several issues here:

* We are violating the open-closed principle by updating the main service every time a new class is added.
* The service becomes dependent on each member of the class family.

Solution:
The Factory Method provides a mechanism to simplify this while making the system more extensible and decoupled from specific product class implementations. Instead of directly constructing objects with the `new()` operator, we replace those calls with a specialized factory method in the service(here is important to notice the difference between requesting a new object and creating it). At first glance, this change may seem superficial—it just moves the constructor call from one part of the program to another. However, the key benefit is that we can now override the method in a subclass, allowing us to change the class of the objects being created without altering the main service.

While this is the traditional approach defined by the Gang of Four (GoF), there’s a simpler alternative called Simple Factory. This approach uses a static method to return an instance of a specific implementation based on input parameters, allowing us to avoid creating multiple subclasses.

Key point:
It’s not mandatory to create a concrete creator for each specific class. The factory can return different objects based on the input (similar to an Abstract Factory pattern)

**Author notes:**

*Scenarios where the product has a simple construction are easy to adrress using generics and constrains, however, when they gets complex, like introducing services, configurations and any other dependencies, generic not solves the problem.*

*Factory method attempt is to abstract and decouple the concret product creation, not for improving the decision making of which product create, for this we have strategies like factory selector, DI, Dictionaries and even a builder.*

References:
 * [SourceMaking](https://sourcemaking.com/design_patterns/factory_method)
 * [Refactoring guru](https://refactoring.guru/design-patterns/factory-method/csharp/example)
 * [Geek for geeks](https://geeksforgeeks.org/factory-method-for-designing-pattern/#advantages-of-factory-method-design-pattern)
 * Dessign patterns book second edition by O'Really