# JavaScript-project-
// Superclass
class Animal {
    String name;
    int age;

    // Constructor
    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to describe the animal
    public void describe() {
        System.out.println("This is an animal named " + name + " and it is " + age + " years old.");
    }

    // Overloaded method
    public void sound() {
        System.out.println("This animal makes a sound.");
    }

    public void sound(String specificSound) {
        System.out.println("This animal makes a sound like: " + specificSound);
    }
}

// Subclass 1
class Dog extends Animal {

    // Constructor
    public Dog(String name, int age) {
        super(name, age);
    }

    // Overriding the describe method
    @Override
    public void describe() {
        System.out.println("This is a dog named " + name + " and it is " + age + " years old.");
    }
}

// Subclass 2
class Cat extends Animal {

    // Constructor
    public Cat(String name, int age) {
        super(name, age);
    }

    // Overriding the describe method
    @Override
    public void describe() {
        System.out.println("This is a cat named " + name + " and it is " + age + " years old.");
    }
}

// Main class
public class InheritancePolymorphismDemo {
    public static void main(String[] args) {
        // Creating objects of superclass and subclasses
        Animal generalAnimal = new Animal("GenericAnimal", 5);
        Dog myDog = new Dog("Buddy", 3);
        Cat myCat = new Cat("Whiskers", 2);

        // Demonstrating inheritance and calling superclass methods
        generalAnimal.describe();
        generalAnimal.sound();

        // Demonstrating overriding
        myDog.describe();
        myCat.describe();

        // Demonstrating overloading
        myDog.sound();
        myDog.sound("Woof");
        myCat.sound();
        myCat.sound("Meow");
    }
}
