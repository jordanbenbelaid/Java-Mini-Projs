# Object-Oriented Programming Exercise

## Encapsulation

**Task:** Create a class called `Vehicle`.

The class should contain:

- At least 3 attributes in general of a vehicle, and an `id` for each vehicle (as an `int`)
- A constructor with all attributes as parameters and a constructor with no parameters (you can add an extra if you want)
- Getters and setters for your attributes
- 2 generic methods for a vehicle
- A `toString` method (you can reformat this to make it look nicer)

In your main runner class, instantiate **4 objects**.

---

## Inheritance & Polymorphism

**Task:** Create 3 subclasses (children classes) of `Vehicle`, each with 1 or 2 of its own attributes (different from `Vehicle`).

Requirements:

- Create a constructor with every attribute (including parent attributes) in each class
- Create getters and setters in each child class
- Override the generic methods for `Vehicle` in each child class
- Create a `toString` in each child class (these should include the attributes from `Vehicle` as well)

---

## Garage Class

Create a new class called `Garage`:

- Include a list of vehicles (empty for now)
- Add a method that lets you **add a vehicle** to the list
- Create a `findVehicleById` method to find a vehicle by its ID
- **STRETCH:** Create a `findVehicleByType` method to find vehicles based on their type

---

## Exceptions

- Create a custom exception called `VehicleNotFoundException`
- Apply it to your `Garage` class on the `findVehicleById` method

---

## Abstraction

- Make your `Vehicle` class an **abstract class**
- Add 1 abstract method to your `Vehicle` class called `calcBill`, and implement it in the child classes.  
  - This method will calculate the bill depending on the type of vehicle
- In the `Garage` class, create a `calculateTotalBill` method that goes through your list and adds a cost to each vehicle depending on the vehicle type
- **STRETCH:**
  - Add a method to calculate the bill by ID
  - Add a method to remove a vehicle by ID
  - Add a method to calculate the bill depending on the type of vehicle
  - Add any other methods you think will improve your garage

---

## Interfaces

- Create some interfaces that you can implement into your `Vehicle` class and the child classes