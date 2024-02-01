# factory-pattern

## Definition

The Factory Method design pattern is a creational pattern that provides an interface for creating objects in a superclass, but it allows subclasses to alter the type of objects that will be created. The key concept is the introduction of a factory method, which is declared in the superclass and implemented by its subclasses. This pattern promotes coding to an interface, not an implementation, and allows for flexible object creation without modifying client code.

## Example

Consider an online store specializing in knives. The original implementation of the `KnifeStore` class had a method named `orderKnife` responsible for creating different types of knives based on conditions. As the store expanded its knife offerings, the method became intricate with an increasing number of conditionals.

To enhance clarity and maintainability, a `KnifeFactory` class has been introduced. The `KnifeFactory` class contains a method named `createKnife` that handles the concrete instantiation of specific types of knives. The `orderKnife` method in the `KnifeStore` class now delegates the responsibility of creating knives to the `KnifeFactory`.

```javascript
// Concrete factory
class KnifeFactory {
  createKnife(type) {
    switch (type) {
      case 'chefs':
        return new ChefsKnife()
      case 'steak':
        return new SteakKnife()
      // Add more cases for other knife types
      default:
        throw new Error('Unknown knife type')
    }
  }
}

// Superclass for KnifeStore
class KnifeStore {
  constructor(knifeFactory) {
    this.knifeFactory = knifeFactory
  }

  orderKnife(type) {
    const knife = this.knifeFactory.createKnife(type)
    knife.sharpen()
    knife.polish()
    knife.package()
    return knife
  }
}

// ChefsKnife and SteakKnife are subclasses representing different types of knives.
class ChefsKnife {
  sharpen() {
    console.log("Sharpening Chef's Knife")
  }
  polish() {
    console.log("Polishing Chef's Knife")
  }
  package() {
    console.log("Packaging Chef's Knife")
  }
}

class SteakKnife {
  sharpen() {
    console.log('Sharpening Steak Knife')
  }
  polish() {
    console.log('Polishing Steak Knife')
  }
  package() {
    console.log('Packaging Steak Knife')
  }
}

// Usage
const knifeFactory = new KnifeFactory()
const knifeStore = new KnifeStore(knifeFactory)

const chefsKnife = knifeStore.orderKnife('chefs')
const steakKnife = knifeStore.orderKnife('steak')
```

In this example, the `KnifeStore` remains the abstract creator class with an abstract factory method, `createKnife`. The `KnifeFactory` serves as the concrete creator class, implementing the factory method for concrete instantiation. The `ChefsKnife` and `SteakKnife` classes represent concrete product classes.

This implementation adheres to the Factory Method pattern, enabling the system to extend its range of knife types without modifying the core `KnifeStore` class. Subclasses, such as `QualityKnifeStore` or `BudgetKnifeStore`, can provide their own factory method implementations to create different types of knives. This design approach aligns with object-oriented principles, promoting extensibility and separation of concerns.
