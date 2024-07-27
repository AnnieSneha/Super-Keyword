# Super-Keyword

To implement the problem statement, you need to define two classes: `Vehicle` and `Car`. The `Vehicle` class will have fields for `make` and `year`, and the `Car` class will extend `Vehicle` by adding an additional field for `model`. The `Car` class will also override a method called `displayDetails()` to demonstrate calling the parent class method using `super`.

```java
// Define the parent class Vehicle
class Vehicle {
    // Fields for the make and year of the vehicle
    private String make;
    private int year;

    // Constructor for the Vehicle class
    public Vehicle(String make, int year) {
        this.make = make;
        this.year = year;
    }

    // Method to display vehicle details
    public void displayDetails() {
        System.out.println("Vehicle Make: " + make);
        System.out.println("Vehicle Year: " + year);
    }
}

// Define the child class Car that inherits from Vehicle
class Car extends Vehicle {
    // Additional field for the model of the car
    private String model;

    // Constructor for the Car class
    public Car(String make, int year, String model) {
        super(make, year); // Call the parent class constructor
        this.model = model;
    }

    // Override the displayDetails() method
    @Override
    public void displayDetails() {
        super.displayDetails(); // Call the parent class displayDetails()
        System.out.println("Car Model: " + model);
    }
}

// Main class to test the implementation
public class Main {
    public static void main(String[] args) {
        // Create an instance of Car
        Car car = new Car("Toyota", 2020, "Corolla");
        
        // Display the details of the car
        car.displayDetails();
    }
}
```
1. **Vehicle Class**:
   - It has two private fields, `make` and `year`.
   - It has a constructor that initializes these fields.
   - The `displayDetails()` method prints the make and year of the vehicle.

2. **Car Class**:
   - It extends the `Vehicle` class and includes an additional private field, `model`.
   - The constructor of the `Car` class takes `make`, `year`, and `model` as parameters and uses the `super` keyword to call the parent class (`Vehicle`) constructor to initialize `make` and `year`.
   - The `displayDetails()` method is overridden to first call the `displayDetails()` method of the `Vehicle` class using `super.displayDetails()` and then print the `model`.

3. **Main Class**:
   - An instance of `Car` is created with specific values for make, year, and model.
   - The `displayDetails()` method is called to show the details of the car, demonstrating the use of inheritance and method overriding.
