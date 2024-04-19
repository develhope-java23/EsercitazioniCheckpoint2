# Java 23 - Checkpoint #2
## Java advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare a class ElectricBike with the following variables and methods:
- energy: int
- speed: int
- position: int
  - All variables are initialized to 0
- recharge(int value)
  - Increases the energy by "value". If value is <= 0, throw an exception
- accelerate()
  - Increases the speed by energy * 0.2, then decreases energy by the same value
- move()
  - Increases position by speed * 0.8, then decreases speed by the same value
 
2. Declare a class Battery with the following variables and methods:
- capacity: int
  - Capacity must be positive, throw an exception instead
- apply(ElectricBike):
  - Recharges the car via the method recharge, passing the value of capacity as parameter
 
3. Implement a main method where:
- A LinkedList of 3 electric bikes is initialized
- 3 ArrayLists of batteries are initialized, one for each car
