Noticing bugs in our subsystems is call code fragility. 
Rigidity is the tendency for software to be difficult to change even in simple ways.
Technical debt is the cost of prioritizing fast delivery over code quality for long periods of time the key for this is to keep it under control because if not it can kill the project.

Solid has 5 principles.
Single responsibility principle, open closed principle, liskov substitution principle, interface segregation principle, dependency inversion principle.

Single responsibility principle 
Every function class or module should only have 1 reason to change.
Identify multiple reasons of change.
If methods are a great example of this, the same goes for switch statements. 

Danger of multiple responsibilities
This is more difficult to read and the reason for it.  
-Decrease quality due to testing difficulty.
-Side effect
-High coupling
-Coupling Is the level of interdependency between various software’s components

Evolving code with the open closed principle(ocp)
Classes function and modules should be closed for modification, but open for extension
Why should we apply the OCP
-New features can be added easily with minimal cost.
-Minimizes the risk of regression bugs.
-Enforces decoupling by isolating changes in specific components, works along with the SRP


Open closed principle
OCP implementation strategies
Inheritance is a good way to apply open closed principle.
-Start small, make changes inline.
-More changes consider inheritance. 

Applying OCP for frameworks and API
 API a contract agreement between different software components on how they should work together.

A public framework or API is under your control but clients might use it in ways that I am not aware of
Best Practices for Changing API
-Do not change existing public contracts: data classes, signatures
-Expose abstractions to your customers and let them add new features on top of your framework
 If a breaking change is inevitable, give Your clients time to adapt.

Applying Liskov Substitution Principle
Liskov Subtitution Principle
Any object of a type must be substitutable by objects of a derived typed without altering the correctness of that program.

Fixing incorrect relationships between objects are a cause of subtle bugs in applications and they need to be 
corrected as soon as they are discovered.

2 ways to refactor code and make it respect the Liskov 
Substitution principle
1.eliminate incorrect relations between objects
2.use “Tell, don’t ask!” principle to eliminate
Type checking and casting 
To apply the LSP in a proactive way
Make sure that a derived type can substitute its base type completely keep base classes small and focused.

Interface Segregation Principle
 Clients should not be forced to depend on methods they do not use, we have to split interfaces that are very large into smaller interfaces so that clients that use them will not be  force to depend on things they don’t need.

The ISP reinforces other solid principles, for example. 
Keeping interfaces small, the classes that implement them have a higher chance to fully substitute that interface. 
Classes that implement small interfaces are more focused, So we reinforce the single responsibility principle.

Benefits of Applying the ISP
Lean interfaces minimize dependencies on unused members and reduce code coupling, code coupling is the number one enemy of clean code.
Code becomes more cohesive and focused, It reinforces the use of the SRP and LSP.
Symptoms of Interface Pollution
-interfaces with lots of methods 
-interfaces with low cohesion
Fixing Interface Pollution
Your own code breaking interfaces is easy and safe due to the possibility to implement as many interfaces As we want.
External legacy code you can’t control the interfaces In the external code, so you use design patterns
Like “adapter” 

Decoupling components with the dependency inversion Principle
Dependency inversion principle
-high level modules should not depend on low level modules both should depend on abstractions.
-abstractions should not depend on details. Details should Depend upon abstraction.

Dependency injection (DI)
A technique that allows the creation of dependent objects outside a class and provides those objects
to a class.

Inversion of control
Is a design in which the control of object creation, configuration and lifecycle is passed to a container framework Is not the programmer but someone else who control the objects.
IoC container benefits
-makes it easy to switch between different implementations at runtime
-increased program modularity
-manages the lifecycle of objects and their configuration

Spring bean
Objects use by you application and that are managed by the spring IoC container. They are created with the configuration that you supply to the container.

Design patterns in java
A solution of a problem in context, Patterns are discovered not created.

Object-oriented programing
-Abstraction hiding complexity
-encapsulation information hiding
-inheritance inherit from another class and avoid duplicate
Code
-polymorphism subclass stands in for the superclass

Strategy pattern
-defines a family of algorithms, encapsulates each one and makes them interchangeable
-lets algorithm vary independently from clients that use it.




