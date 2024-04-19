# Java 23 - Checkpoint #2
## Java advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare a class Battery with the following variables and methods:
- capacity: int
  - Capacity must not be negative, throw an exception instead
 
2. Declare a class ElectricBike with the following variables and methods:
- energy: int
- maxEnergy: int
- weight: float
- speed: int
- maxReachedSpeed: int
- batteries: List\<Battery\>
- position: int
  - All integer variables are initialized to 0, while "batteries" is initialized as an empty list.
  - maxEnergy and weight are passed to the constructor as parameters.
- attach(Battery)
  - Add the battery to the list "batteries".
- recharge()
  - Increases the energy by the sum of the batteries capacities, then empties the batteries list.
  - If the resulting value is greater than maxEnergy, then cap it to maxEnergy.
  - If no batteries are present, throw an exception.
  - Speed is reduce to 25% of its actual value on recharge.
- accelerate()
  - Increases the speed by (energy * 0.2) / (weight * 0.1), then decreases energy by the same value.
  - If the resulting speed value is greater than maxReachedSpeed, then update maxReachedSpeed accordingly.
- move()
  - Increases position by "speed", then decreases speed by speed * 0.4.
  
3. Implement a main method where:
- A LinkedList of 3 electric bikes is initialized, with various weights and maximum energies.
- Attach 1 to 4 batteries to each bike.
- A loop is executed where, for each interation i and each car c:
  - If i % 15 == 0, then the bike is recharged. If an exception is thrown during recharge, catch it and print its message to the screen.
  - The bike moves
  - The bike accelerates
  - If position is a multiple of 50 or the speed of the bike is less than 10, then add a new Battery with capacity position / 5 to the bike.
  - If the bike reaches position >= 1000, then it is declarated a winner. If multiple bikes reach the target during the same iteration, they are all winners. After at least one bike wins, the loop stops.
 - Print the bike that achieved the max speed during the race.
