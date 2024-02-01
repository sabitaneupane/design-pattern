# design-pattern

## What is Design Pattern

Design patterns are general reusable solutions to common problems that occur in software design. They are best practices that provide solutions to recurring design problems.

## Benefits of Design Pattern

- **Recurring Design Problems:** Design patterns address recurring design problems in software development. These are problems that developers encounter frequently.
- **Proven Solutions:** Design patterns are practical, proven solutions that have been used by experienced developers to solve common design problems. They are not just theoretical concepts but have real-world applications.
- **Flexibility and Reusability:** Design patterns provide flexible and reusable solutions to design problems. Instead of reinventing the wheel for each new problem, developers can leverage established patterns.
- **Not a One-Size-Fits-All Solution:** While there are many design patterns, it's crucial to choose the right one for a specific problem. Not every pattern is applicable to every situation, and selecting the appropriate pattern requires understanding the problem at hand.
- **Conceptual Guidance:** Design patterns are more conceptual than concrete sets of source code. They guide the structure of software design and contribute to making it more flexible and reusable.
- **Evolution of Skills:** As developers gain more experience, they move beyond basic language syntax and become adept at writing idiomatic code. Design patterns represent a higher level of expertise, helping developers become design experts.
- **Avoiding Trial and Error:** Design patterns allow developers to benefit from the experience of experts, avoiding the need for trial and error in finding solutions to common design problems.
- **Building a Design Vocabulary:** Design patterns help establish a common design vocabulary among developers. Instead of repeatedly explaining complex design solutions, developers can use pattern names to communicate more efficiently.
- **Skip Hardships:** By using design patterns, developers can skip the hardships and challenges that experts have already faced. This accelerates the development process and leads to better-written software.
- **Creating Better Software:**
  - Ultimately, the goal of design patterns is to contribute to the creation of better, more maintainable, and more robust software by providing proven solutions to common design challenges.

## Types of Design Pattern

- **Creational Patterns:** Creational Patterns address how to handle the creation of new objects. There are several different patterns based on creating and cloning objects. For example, when creating an object similar to an existing one, instead of instantiating a new object, you might choose to clone existing objects. The decision to clone, rather than instantiate, depends on the language in which you are implementing the solution. Languages without the notion of classes would encourage you to clone and add to existing objects. A language like JavaScript does not have traditional classes for instantiation. Instead, objects are cloned and expanded to meet the specific needs of those instances, referred to as prototypes. JavaScript allows changes to these prototypes at runtime. On the other hand, languages like Java and C# heavily rely on instantiating objects using specific classes defined at compile time. The different methods of creating objects can significantly impact how you approach problem-solving. The implementation language is how the design pattern language is realized, and it can heavily influence the patterns that are feasible to use.

  - Singleton Pattern
  - Factory Method Pattern
  - Abstract Factory Pattern
  - Builder Pattern
  - Prototype Pattern

- **Structural Patterns:** Structural patterns describe how objects are connected to each other. Previously, we explored major design principles like Decomposition and Generalization, expressing them in UML class diagrams with relationships such as Association, Aggregation, Composition, Inheritance, and Interfaces. The way objects are structured depends on the desired relationships between them. Structural patterns not only define how objects relate to each other but also how subclasses and classes interact through inheritance. These patterns leverage these relationships to achieve specific design goals. Think of a structural pattern as a food dish with a combination of flavor pairings. Just as flavor pairings determine suitable ingredient combinations, each structural pattern defines various relationships among objects in software.

  - Adapter Pattern
  - Bridge Pattern
  - Composite Pattern
  - Decorator Pattern
  - Facade Pattern
  - Flyweight Pattern

- **Behavioral Patterns:** Behavioral patterns, on the other hand, concentrate on how objects distribute work. They describe how each object performs a single cohesive function and how independent objects collaborate towards a common goal. Imagine a behavioral pattern as a race car pit crew at a track. In the pit crew, each member's role contributes to achieving victory, the common goal. Responsibilities are distributed among members, with some changing tires, others handling wheel nuts, and others refueling the car. Like a game plan, a Behavioral Pattern outlines the overall goal and the purpose of each object. It emphasizes the necessity for all elements to work together harmoniously. It's important to note that these categories may not always be distinct, as some patterns may span multiple categories due to overlapping elements.

- Chain of Responsibility Pattern
- Command Pattern
- Interpreter Pattern
- Iterator Pattern
- Mediator Pattern
- Memento Pattern
- Observer Pattern
- State Pattern
- Strategy Pattern
- Template Method Pattern
- Visitor Pattern

## References:

- [Refactoring.guru](https://refactoring.guru/design-patterns/typescript)
- [Head First Design Patterns](resources/head-first-design-patterns.pdf)
- [Java Code Geeks Design Patterns](resources/java-code-geeks-design-patterns.pdf)
- [Coursera Design Patterns](https://www.coursera.org/learn/design-patterns)
- [Educative Design Patterns](https://www.educative.io/courses/software-design-patterns-best-practices)
- [Udemy Course](https://www.udemy.com/course/typescript-design-patterns/learn/lecture/7510402#overview)
