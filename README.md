

## ✅ Design Principles Used

This project adheres to key software design principles to ensure maintainability, extensibility, and clarity.

### 🔐 SOLID Principles

1. **Single Responsibility Principle (SRP)**  
   SRP means a class should do only one thing.
   
   1) Each class has a single well-defined responsibility. E.g., `InvoicePrinter` only prints, while `InvoiceRepository` handles DB operations.  
   2) Each class or module should have only one reason to change, meaning it should be responsible for a single, well-defined task.  
   3) This promotes modularity, testability, and maintainability by preventing classes from becoming overloaded with unrelated responsibilities.

   🚦 **Why is SRP Important?**
   - ✅ **Improves maintainability**: Smaller, focused classes are easier to update.
   - ✅ **Increases readability**: Easier for others (and you) to understand.
   - ✅ **Enables better testing**: Unit tests become more precise.
   - ✅ **Promotes reusability**: SRP classes can be reused in other contexts.

   🧠 **Real-Life Analogy**  
   Think of a restaurant worker:
   - **Bad design**: One person cooks, takes orders, serves food, and cleans dishes.
   - **Good design (SRP)**: Each worker has one responsibility: cook, orders, server, cleaner, cashier.

   Why is this better? If one task (say, cleaning) changes, it doesn't affect cooking.

   🧰 **When to Apply SRP in Real Projects**
   - When you notice many unrelated methods in a class.
   - When your class is growing too large (God Class).
   - When a change in one area accidentally breaks something else.
   - When testing becomes difficult or unclear.

2. **Open/Closed Principle (OCP)**  
   A class should be **open for extension** but **closed for modification**. This means that the behavior of a class can be extended without modifying its existing code.

   1) New functionality should be added through **extension** (e.g., subclassing or composition) rather than changing the existing code.
   2) This principle allows you to add new features while ensuring the existing codebase remains intact and doesn't introduce bugs.
   3) The open/closed principle promotes scalability and helps maintain stability in a system, especially in large projects.

   🚦 **Why is OCP Important?**
   - ✅ **Increases stability**: Code is less likely to break with changes.
   - ✅ **Improves maintainability**: Easier to add features without touching existing code.
   - ✅ **Promotes flexibility**: Enables you to adapt to changing business requirements.

   🧠 **Real-Life Analogy**  
   Think of a plugin-based music player:
   - **Bad design**: Every time you want a new feature (e.g., adding a new audio format support), you modify the core player.
   - **Good design (OCP)**: You add a plugin to the player that provides the new feature without touching the core player code.

   Why is this better? It allows you to add new features without disrupting the original player.

   🧰 **When to Apply OCP in Real Projects**
   - When you need to add new features regularly.
   - When the core functionality is stable, and you want to avoid changing it frequently.
   - When you need to ensure backward compatibility with previous versions of your software.

3. **Liskov Substitution Principle (LSP)**  
   Subtypes must be **substitutable** for their base types without affecting the correctness of the program. This means objects of a derived class should be able to replace objects of the base class without altering the desired behavior.

   1) Derived classes should not change the expected behavior of the parent class.
   2) This ensures that any derived class can be used interchangeably with its base class without introducing errors.
   3) Liskov’s principle ensures consistency and reliability when polymorphism is used.

   🚦 **Why is LSP Important?**
   - ✅ **Promotes code reusability**: You can confidently use derived classes in place of their base class.
   - ✅ **Ensures consistency**: Keeps the system's behavior predictable.
   - ✅ **Improves maintainability**: Reduces the chances of unexpected bugs when extending functionality.

   🧠 **Real-Life Analogy**  
   Think of an electric appliance:
   - **Bad design**: You buy a vacuum cleaner that can only clean carpets but says it works on all surfaces. It breaks when used on tiles.
   - **Good design (LSP)**: You buy an appliance that cleans all surfaces (tiles, carpet, hardwood). You can replace any cleaning device with the new one, and it should work the same way.

   Why is this better? You can replace a cleaner without worrying about it breaking.

   🧰 **When to Apply LSP in Real Projects**
   - When polymorphism is used in your design.
   - When you create derived classes or subclasses.
   - When you need predictable and consistent behavior from subclasses.

4. **Interface Segregation Principle (ISP)**  
   Clients should not be forced to implement interfaces they do not use. In other words, it's better to have several small, specific interfaces than one large, general-purpose interface.

   1) Instead of having one huge interface, split it into smaller, more manageable ones.
   2) This minimizes the number of unnecessary methods for each class and promotes better adherence to the **Single Responsibility Principle**.
   3) ISP helps make the system more flexible and maintainable by ensuring that classes only implement the interfaces relevant to them.

   🚦 **Why is ISP Important?**
   - ✅ **Promotes flexibility**: Classes only need to implement methods they actually use.
   - ✅ **Reduces complexity**: Smaller, more focused interfaces are easier to understand.
   - ✅ **Improves maintainability**: Changes to one interface don't affect unrelated classes.

   🧠 **Real-Life Analogy**  
   Think of a power tool:
   - **Bad design**: A tool that has one interface for all types of work (e.g., drilling, sanding, cutting) requires a user to learn every feature.
   - **Good design (ISP)**: Separate tools for drilling, sanding, and cutting, each with their own interface.

   Why is this better? The user only needs to know how to use the tool that suits their needs.

   🧰 **When to Apply ISP in Real Projects**
   - When your system has large interfaces with methods that aren't needed by all clients.
   - When your classes are implementing unnecessary methods.
   - When you want to reduce code coupling.

5. **Dependency Inversion Principle (DIP)**  
   High-level modules should depend on abstractions (e.g., interfaces), not on concrete classes. Likewise, low-level modules should depend on abstractions, not concrete classes.

   1) Depend on **interfaces or abstract classes** rather than on concrete implementations.
   2) This reduces the coupling between different components of your system and makes it more flexible and testable.
   3) This allows higher-level components to change without affecting lower-level components, as long as the abstraction remains consistent.

   🚦 **Why is DIP Important?**
   - ✅ **Promotes flexibility**: Changes in the implementation details of lower-level modules do not affect high-level modules.
   - ✅ **Improves testability**: It's easier to mock interfaces or abstract classes in unit tests.
   - ✅ **Increases maintainability**: Changes in one module are less likely to break others.

   🧠 **Real-Life Analogy**  
   Think of a remote control:
   - **Bad design**: A remote control is tightly coupled to a specific TV brand, so when you change TVs, the remote no longer works.
   - **Good design (DIP)**: A universal remote that can work with any TV, as long as both support a common interface (e.g., infrared signals).

   Why is this better? It doesn't matter which TV you buy; the remote will work as long as both support the same interface.

   🧰 **When to Apply DIP in Real Projects**
   - When building flexible, testable applications.
   - When your system has tightly coupled classes that need to be decoupled.
   - When you need to change the implementation of a service without affecting others.

