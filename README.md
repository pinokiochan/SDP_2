# Assignment 2

## 1. Document Creation System

### Overview
This project implements a flexible system for creating different types of documents, such as PDF and Word files, using the Factory Method design pattern. The system is designed to easily support the addition of new document types (e.g., Excel, PowerPoint) without changing the existing code. Each document type has its own creation process, ensuring that the system remains maintainable and extendable.

### Features
- **Supports Multiple Document Types**: Currently, the system can generate PDF and Word documents.
- **Easy Extensibility**: New document types can be added by creating new document classes and factories, without modifying the existing system.
- **Follows SOLID Principles**: The system adheres to the Open/Closed Principle, ensuring the system is open for extension but closed for modification.

### Design Pattern
- **Factory Method**: The creation logic for each document type is encapsulated in its own factory class. This allows for the flexible and scalable creation of different document types.

### Project Structure
- **Document (interface)**: Represents the common interface that all document types implement.
- **PDFDocument, WordDocument**: Concrete implementations of the `Document` interface, each handling the specific creation process for that type.
- **DocumentFactory (abstract class)**: Defines the factory method (`createDocument()`) for creating documents.
- **PDFDocumentFactory, WordDocumentFactory**: Concrete factories that instantiate PDF and Word documents, respectively.

### How to Run
1. Clone the repository to your local machine.
2. Open the project in IntelliJ IDEA.
3. Build the project and run the `Main` class.

---

## 2. Theme Selection System

### Overview
This project implements a theme selection system using the Abstract Factory design pattern in Java. It allows users to choose between different themes (Light Theme and Dark Theme) and displays the corresponding UI components (buttons and checkboxes).

### Features
- **Theme Options**: Choose between Light and Dark themes.
- **Modular Design**: Each theme has its own specific components.
- **Extensibility**: Easily add new themes without modifying existing code.

### Technologies Used
- Java

### Structure
The project is structured into several classes:
- **Interfaces**:
    - `Button`: Interface for button components.
    - `Checkbox`: Interface for checkbox components.
- **Concrete Components**:
    - `LightButton`: Light-themed button implementation.
    - `LightCheckbox`: Light-themed checkbox implementation.
    - `DarkButton`: Dark-themed button implementation.
    - `DarkCheckbox`: Dark-themed checkbox implementation.
- **Factory Interfaces**:
    - `ThemeFactory`: Abstract factory interface for creating components.
- **Concrete Factories**:
    - `LightThemeFactory`: Factory for creating light-themed components.
    - `DarkThemeFactory`: Factory for creating dark-themed components.
- **Main Class**:
    - `Main`: Entry point of the application that interacts with the user and displays the chosen theme components.

### How It Works
1. The user is prompted to select a theme (1 for Light Theme or 2 for Dark Theme).
2. The program instantiates the corresponding factory based on the user's choice.
3. The selected factory creates the theme-specific components (button and checkbox).
4. The program displays the names of the created components in the console.

### How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Compile the Java files:
   ```bash
   javac *.java
