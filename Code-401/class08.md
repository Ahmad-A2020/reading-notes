Resources:
- [SOLID principles intro](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
- [OO SOLID principles in real life](https://dzone.com/articles/the-solid-principles-in-real-life)


### SOLID principles intro
- SOLID is an acronym for the first five object-oriented design (OOD) principles by Robert C. Martin as follows:
- S : Single-responsiblity Principle

A class should have one and only one reason to change, meaning that a class should have only one job
- O : Open-closed Principle- Objects or entities should be open for extension but closed for modification

- L : Liskov Substitution Principle: Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T

- I : Interface Segregation Principle: A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.

- D : Dependency Inversion Principle: Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.

### OO SOLID principles in real life:
- s is for single responsibility principle: class or module should do one thing onlycd
- o is for open/closed principle:ode entities should be open for extension, but closed for modification.a great example of this in real life is sitting in your pocket in the form of a smartphone. all such phones have app stores and these app stores let you extend the base functionality of the phone.
- l is for liskov substitution principle:   any child type of a parent type should be able to stand in for that parent without things blowing up. for example if you have a class, animal, with a makenoise() method, then any subclass of animal should reasonably implement makenoise(). cats should meow, dogs should bark, etc.
- i is for interface segregation principle: A good real life example on this is hink of going down to your local corner restaurant and checking out the menu. you'll see all of the normal menu mainstays, and then something that's just called "soup of the day." why do they do this? because the soup changes a lot and there's no sense reprinting the menus every day.
- d is for dependency inversion
- dependency inversion principle (dip) encourages you to write code that depends upon abstractions rather than upon concrete details.to visualize this in your day to day,go down to your local store and pay for something with a credit card. the clerk doesn't examine your card and get out the "visa machine" after seeing that your card is a visa. he just takes your card, whatever it is, and swipes it. both you and the clerk depend on the credit card abstraction without worrying about specifics.
