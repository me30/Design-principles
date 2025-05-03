## ✅ Design Principles Used

This project adheres to key software design principles to ensure maintainability, extensibility, and clarity.

### 🔐 SOLID Principles

1. **Single Responsibility Principle (SRP)**  
   Each class has a single well-defined responsibility. E.g., `InvoicePrinter` only prints, while `InvoiceRepository` handles DB operations.

2. **Open/Closed Principle (OCP)**  
   New features (e.g., a new printer or storage type) can be added without modifying existing code.

3. **Liskov Substitution Principle (LSP)**  
   Subtypes can replace base types. Interfaces can be substituted with any implementation.

4. **Interface Segregation Principle (ISP)**  
   Interfaces are role-specific, ensuring clients only use what they need.

5. **Dependency Inversion Principle (DIP)**  
   High-level modules depend on abstractions, not concrete classes. Spring's dependency injection supports this well.

---

### 🧠 Additional Key Design Principles

6. **DRY (Don't Repeat Yourself)**  
   Common logic is abstracted and reused across classes and services.

7. **KISS (Keep It Simple, Stupid)**  
   The code avoids overengineering and keeps solutions straightforward.

8. **YAGNI (You Aren’t Gonna Need It)**  
   Features are only implemented when they are needed, keeping the codebase lean.

9. **Composition Over Inheritance**  
   The system favors object composition to extend behavior rather than deep class hierarchies.

10. **Law of Demeter (LoD)**  
   Methods communicate only with direct collaborators, promoting low coupling and encapsulation.

---
