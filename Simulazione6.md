# Java 23 - Checkpoint #2
## Java advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare a class ElectricCar with the following variables and methods:
- energy: int
- speed: int
- position: int
  - All variables are initialized to 0
- recharge(int)
  - Increases the energy by the value of the parameter
- accelerate()
  - Increases the speed by energy * 0.3, then decreases energy by the same value
- move()
  - Increases position by speed * 0.5, then decreases speed by the same value
 
2. Declare a class Battery with the following variables and methods:
- capacity: int
- apply(ElectricCar):
  - Recharges the car via the method recharge, passing the value of capacity as parameter
 
3. Implement a main method where:
- An HashSet of 3 electric cars is initialized
- 3 ArrayLists of batteries are initialized, one for each car
- A loop is executed where, for each interation i and each car c:
  - If i % 5 == 0, then the car c is recharged by the first battery available in its list, which is then removed. If no batteries are available for that car, nothing is done.
  - The car accelerates
  - The car moves
  - If the car reaches position >= 100, then it is declarated a winner. If multiple cars reach the target during the same iteration, they are all winners. After at least one car wins, the loop stops.
 
## SQL
Given the following schema:
```
Car(
  plate CHAR(8) PRIMARY KEY,
  maxSpeed INTEGER NOT NULL,
  capacity INTEGER NOT NULL
)

Road(
  identifier INTEGER PRIMARY KEY,
  minimumSpeed INTEGER NOT NULL,
  length INTEGER NOT NULL,
  hasChargeStations BOOLEAN NOT NULL
```

Write the following queries:
- Insert a Car and a Road in the database with random values
- Select all cars with higher speed than capacity
- Select the count of cars that can access each road. A car can access a road if the car's maximum speed is higher than the road's minimum speed. Plus, it is required that the car's capacity is higher than the road's length, otherwise the car is allowed to access the road only if there is any charge station.
