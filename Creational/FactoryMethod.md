## Factory method

Problem: We have a service that implement an specific bussines logic, however, depending on external input, this service needs to instantiate one of many specific classes, as it gets more popular, the number of specific classes increment, by the way the logic for instantiating the one that the service needs gets updated every single time, making it error prone, dependant of every single class and even worse if the object constructors are complicated.

Solution: Factory method provide a mechanism for simplifying it, making it at the same time more extensible, decoupled the main service from the specific class implementations and encapsulated. The way we achieve all these capabilities is by:
    * Defining an common interface for all the specific class implementations.
    * Defining a method in the service that defines an abstrach method that returns an instance of the Product interface.
    * Defining a subclass that inherit from the main service one (Creator, Specific Factory) and implement the abstract method (Responsible of the product Interface instantiation)
    * Adapt the client code for using the main service as base, that way we can use any of the concrete creators at runtime.

Despite this is the way defined by the GOF there is a more simple approach called SimpleFactory, this is basically an static method that return an instance of the specific implementation based on the parameters, this way we can avoid creating many classes.

Good to highlight: Create a Concrete creator is not mandatory for each specific class, we can return an object or anothe depending on the input (yes, like a Abstract factory)

References:
[SourceMaking](https://sourcemaking.com/design_patterns/factory_method)
[Refactoring guru](https://refactoring.guru/design-patterns/factory-method/csharp/example)
[Geek for geeks](https://geeksforgeeks.org/factory-method-for-designing-pattern/#advantages-of-factory-method-design-pattern)
Dessign patterns book second edition by O'Really