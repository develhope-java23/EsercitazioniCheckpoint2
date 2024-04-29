# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Fuel with the following methods:
- getEnergy(): int
- canBeConsumed(): boolean
2. Declare a class Car with the following attributes and methods
- energy: int
    - Initialized to 0
- fuels: List\<Fuel\>
    - Initialized as an empty list
- capacity: int
- weight: double
- enginePower: double
- insert(Fuel)
  - Adds the Fuel object to fuels.
  - Launch an exception if the number of fuels inserted is already equal to capacity, otherwise inserts the fuel to the list
- turnOn(): int
  - Adds the return value of getEnergy() of every item in fuels to energy
    - If one of the fuels cannot be consumed, meaning that the canBeConsumed() method returns false, print a warning message to the screen and do not add the energy of the fuel.
  - Empties fuels and returns the total amount of energy added in the process.
- race(int trackLength): int
  - Calculate the maximum reachable length of the car as energy / (weight * enginePower) and return the difference between this value and the parameter (maxReachableLength - trackLength).
1. Declare the following classes representing fuels:
- Diesel
  - getEnergy() returns 50
  - canBeConsumed() always returns true
- Battery
  - has an integer attribute “capacity, initialized by passing its value to the constructor. 
  - getEnergy() returns the value of capacity.
  - canBeConsumed() returns true if capacity > 0, false otherwise.
1. Implement a main method where:
- A list of 2 cars is allocated
- 1 to 3 fuels are added to each car
- For each car, turn on the engine and let them race through a track of length 1000. Print if the car was able to finish the track (the race() method returned a positive value) and finally print the car that has reached the farthest point.
  
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
2. Report the count of fuels with an higher capacity than 10.
3. Select the worker with the higher expertise for each department.
4. Calculate the average experitse for each department.
5. Select the count of fuels that each worker is able to use. A worker can use a fuel if Worker.expertise >= Fuel.neededExpertise.