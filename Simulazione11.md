# Java 23 - Checkpoint #2
## Java advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare a class Battery with the following variables and methods:
- capacity: int
  - Capacity must be positive, throw an exception instead
 
2. Declare a class ElectricBike with the following variables and methods:
- energy: int
- speed: int
- maxSpeed: int
- batteries: Set\<Battery\>
- position: int
- All integer variables are initialized to 0, while "batteries" is initialized as an empty list.
- insert(Battery)
  - Add the battery to the list "batteries".
- recharge()
  - Increases the energy by the sum of the batteries capacities, then empties the batteries list. If no batteries are present, throw an exception.
- accelerate()
  - Increases the speed by energy * 0.1, then decreases energy by the same value
- move()
  - Increases position by speed * 0.6, then decreases speed by the same value
  
3. Implement a main method where:
- An ArrayList of 3 electric bikes is initialized
- Attach 2 or 3 batteries to each bike.
- A loop is executed where, for each interation i and each car c:
  - If i % 10 == 0, then the bike is recharged. If an exception is thrown during recharge, catch it and print its message to the screen.
  - The bike moves
  - The bike accelerates
  - If position is a multiple of 100, then add a new Battery with capacity position / 3 to the bike with probability 20%.
  - If the bike reaches position >= 1000, then it is declarated a winner. If multiple bikes reach the target during the same iteration, they are all winners. After at least one bike wins, the loop stops.
 
