# Dive-Deep-into-Dependency-Injection

### What is Dependency Injection
``Dependency Injection is a design pattern in software development where objects (or components) get the dependencies they need from an external source rather than creating them themselves.
Think of it as "giving an object what it needs to do its job" rather than letting the object go out and get those things itself.``

### Core Concept Summarized
- Dependency Injection provides the required dependencies (like objects or services) to a class rather than the class creating them itself.
- This achieves loose coupling, improves testability, and makes the code easier to maintain and extend.
- It relies on Inversion of Control (IoC), where the creation and management of dependencies are handled by an external source (like a DI container).

    ` "Giving an object its instance variables" ~ James Shores `

### Registering Controllers using DI
Controllers are added to DI container in Program.cs using `builder.Services.AddControllers()` and then assembly is scanned to find all the controllers in our project.
*DI Container*: Like a sub-application that registers all the interfaces & their registrations
```
       +-------------------+
       |   DI Container    |
       |  [Dependencies]   |
       +-------------------+
                |
                v
    +-------------------------+
    |   App Area Requests     |
    |   [Needs Controller]    |
    +-------------------------+
                |
                v
    +-------------------------+
    |   Controller Provided   |
    |   [Gets Controller]     |
    +-------------------------+
```
  
