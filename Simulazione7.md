# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Fuel with the following methods:
- getEnergy(): int
2. Declare a class Engine with the following attributes and methods
- energy: int
- fuels: List<Fuel>
- capacity: int
- insert(Fuel): bool
  - Adds the Fuel object to fuels.
  - Returns false if the number of fuels inserted is already equal to capacity, otherwise inserts the fuel to the list and returns true
- turnOn(): List<Integer>
  - Launches an exception if the list fuels is empty
  - Adds the return value of getEnergy() of every item in fuels to energy, then empties fuels and returns a List of integers containing the energy values of every fuel object that was present in the list.
3. Declare the following classes representing fuels:
- Diesel
  - getEnergy() returns 20
- Battery
  - has an integer attribute “capacity”
  - getEnergy() returns the value of capacity. If capacity is 0, an exception is thrown.
4. Implement a main method where:
- An Engine object is allocated
- An HashSet of 4 Fuels objects is allocated. One of them should be a battery
with zero capacity.
- The set of Fuels is printed to screen.
- All objects of the list are loaded into the Engine through the insert(...) method.
- The turnOn() method is called and the return value is saved into a variable, which is suddenly printed to screen. If an exception is thrown then a message must be printed on screen.
- The sum of the list of integers returned by turnOn() is printed to screen.
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
2. Report the count of fuels for each neededExpertise value present in the table.
3. Select the worker with the higher expertise for each department.
4. Select the count of fuels that each worker is able to use. A worker can use a fuel if Worker.expertise >= Fuel.neededExpertise.
5. Select all fuels which have “green” in their name.
