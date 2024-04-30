# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Fuel with the following methods:
- getEnergy(): int
2. Declare a class Engine with the following attributes and methods
- energy: int
- fuels: List<Fuel>
  - Initialzied as an empty List
- insert(Fuel): void
  - Adds the Fuel object to fuels.
- turnOn(): int
  - Launches an exception if the list fuels is empty
  - Adds the return value of getEnergy() of every item in fuels to energy, then empties fuels and returns the sum of the energy values of every fuel object that was present in the list.
3. Declare the following classes representing fuels:
- Diesel
  - Has an integer attribute "purity"
  - getEnergy() returns purity * 0.3, casted to integer
- Battery
  - Has an integer attribute “capacity”, passed to the constructor as parameter. If the value is not positive, throw an IllegalArgumentException.
  - getEnergy() returns the value of capacity.
4. Implement a main method where:
- An Engine object is allocated
- An HashSet of 4 Fuels objects is allocated. One of them should be a battery
with zero capacity.
- The set of Fuels is printed to screen.
- All objects of the list are loaded into the Engine through the insert(...) method.
- The turnOn() method is called and the return value is saved into a variable, which is suddenly printed to screen. If an exception is thrown then a message must be printed on screen.
