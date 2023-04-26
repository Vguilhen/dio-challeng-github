# Design Patterns

## About:

Design patterns are reusable Object-Oriented solutions to commonly occurring software design problems.

The main reference book for design patterns is "Design Patterns: Elements of Reusable Object-Oriented Software" by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, also known as the "Gang of Four" (GoF). This book, published in 1994, is considered the seminal work on design patterns and has had a significant impact on software development practices.

In addition to the Gang of Four book, there are other notable books on design patterns, such as "Head First Design Patterns" by Eric Freeman and Elisabeth Robson, "Patterns of Enterprise Application Architecture" by Martin Fowler, and "Domain-Driven Design: Tackling Complexity in the Heart of Software" by Eric Evans.

## Design Patterns Categories:

Design patterns are typically classified into three main categories:

Creational patterns: These patterns are concerned with object creation mechanisms, trying to create objects in a manner that is suitable for a given situation. Creational patterns help to decouple the client code from the objects it needs to instantiate, thereby making it easier to change the object creation process without affecting the rest of the code. Examples of creational patterns include **Singleton**, Factory Method, Abstract Factory, Builder, and Prototype.

Structural patterns: These patterns deal with object composition and help to define how objects can be composed to form larger structures or systems. Structural patterns provide ways to simplify the design of complex systems by identifying simple relationships between objects. Examples of structural patterns include Adapter, Bridge, Composite, Decorator, **Facade**, Flyweight, and Proxy.

Behavioral patterns: These patterns are concerned with communication between objects and how they collaborate to achieve a common goal. Behavioral patterns help to define how objects interact with one another and how they respond to changes in the system. Examples of behavioral patterns include Chain of Responsibility, Command, Interpreter, Iterator, Mediator, Memento, Observer, State, **Strategy**, Template Method, and Visitor.

## Singleton

The Singleton pattern is a creational pattern that ensures that only one instance of a class is created and provides a global point of access to that instance. This pattern is useful in situations where you need to ensure that there is only one instance of a class in your application, such as managing a connection to a database or controlling access to a shared resource.

example:

    public class SingletonLazy {

    private static SingletonLazy instance;
    private SingletonLazy(){
        super();
    }

    public static SingletonLazy getInstance(){
        if (instance == null) {
            instance = new SingletonLazy();
        }
        return instance;
        }
    }

    public class SingletonEager {
    private static SingletonEager instance = new SingletonEager();
    private SingletonEager(){
    super();
        }
    public static SingletonEager getInstance(){
    return instance;
        }
    }

    public class SingletonLazyHolder {
    public static class InstanceHolder {
    public static SingletonLazyHolder instance = new SingletonLazyHolder();
        }
    private SingletonLazyHolder() {
    super();
        }
        public static SingletonLazyHolder getInstance(){
            return InstanceHolder.instance;
    }


## Facede

The Facade design pattern is a structural design pattern that aims to provide a simplified interface for a complex set of interfaces of a system.

In other words, the Facade pattern provides an abstraction layer that hides the underlying complexity of a system and offers a simplified interface to the end user. This helps to reduce the complexity of client code, making it easier to use and understand.

The Facade pattern is often used in large and complex systems, where there are many different components and interfaces. In these cases, creating a facade can be useful to simplify the interaction between the client and the system. The facade acts as an intermediary layer between the client and the underlying components, hiding the complexity of these components and exposing only a simplified interface to the client.

In addition to simplifying the interaction with the system, the Facade pattern can also improve code maintenance by making it easier to make changes to a complex system. By creating a facade for a system, developers can change the implementation of the underlying components without affecting the facade interface. This means that client code does not need to be changed every time there is a change in the internal components of the system.

In summary, the Facade pattern is a useful approach to simplifying the complexity of large and complex systems. It provides a simplified interface to the client and helps improve code maintenance by making it easier to update and modify.

## Strategy

The Strategy pattern is a behavioral design pattern that allows different algorithms or strategies to be selected at runtime based on a specific context. This pattern enables the encapsulation of different algorithms or behaviors, allowing them to be easily interchanged without modifying the code that uses them.

The Strategy pattern involves defining a family of algorithms, encapsulating each one as an object, and making them interchangeable at runtime. In this pattern, a context object is responsible for selecting and invoking the appropriate strategy object based on the current context. The context object is not aware of the details of the algorithms or strategies, but it delegates the responsibility of executing the algorithm to the selected strategy object.

One of the main advantages of the Strategy pattern is that it promotes the principle of separation of concerns, allowing each algorithm or strategy to be developed independently and tested separately. This improves the flexibility and maintainability of the code, as changes to one algorithm or strategy do not affect the others. Additionally, the Strategy pattern promotes code reuse by encapsulating reusable algorithms or behaviors into separate objects that can be shared across different contexts.

The Strategy pattern is commonly used in situations where different algorithms or strategies may be required based on different contexts or user preferences. For example, a search engine may use different search algorithms based on the user's search query or search preferences. By using the Strategy pattern, the search engine can easily interchange different search algorithms without modifying the code that invokes them.

In conclusion, the Strategy pattern is a useful design pattern for implementing interchangeable algorithms or strategies at runtime. It promotes the principle of separation of concerns, code reuse, and flexibility, and is commonly used in situations where different algorithms or strategies may be required based on different contexts or user preferences.
