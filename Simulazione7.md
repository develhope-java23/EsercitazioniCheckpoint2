# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Fuel with the following methods:
- getEnergy(): int
2. Declare a class Engine with the following attributes and methods
- energy: int
- fuels: List\<Fuel\>
- capacity: int
- insert(Fuel): bool
  - Adds the Fuel object to fuels.
  - Returns false if the number of fuels inserted is already equal to capacity, otherwise inserts the fuel to the list and returns true
- turnOn(): int
  - Launches an exception if the list fuels is empty
  - Adds the return value of getEnergy() of every item in fuels to energy, then empties fuels and returns the total amount of energy added in the process.
3. Declare the following classes representing fuels:
- Diesel
  - getEnergy() returns 50
- Battery
  - has an integer attribute “capacity”
  - The capacity is initialized by passing its value to the constructor. If the value of the parameter is not positive, launch an exception.
  - getEnergy() returns the value of capacity.
4. Implement a main method where:
- An Engine object with capacity 3 is allocated
- An ArrayList of 4 Fuels objects is allocated. One of them should be a battery.
- The list of Fuels is printed to screen.
- All of the objects in the list are loaded into the Engine through the insert(...) method. Print a message communicating if each object has been inserted or not.
- The turnOn() method is called and the return value is saved into a variable, which is suddenly printed to screen.
  
## SQL
Given the following table:
```
Worker(
  id INTEGER PRIMARY KEY,
  name VARCHAR(255),
  expertise INTEGER,
  departmentTag CHAR(6)
)

Fuel(
  name VARCHAR(64) PRIMARY KEY,
  capacity INTEGER,
  neededExpertise INTEGER,
)
```
Write the following queries:
1. Insert a Fuel entry with random values.
2. Report the count of fuels with an higher capacity than 100.
3. Select the worker with the lower expertise for each department.
4. Calculate the average experitse for each department.
5. Select the count of fuels that each worker is not able to use. A worker can use a fuel if Worker.expertise >= Fuel.neededExpertise.
