# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Food with the following methods:
- getSatiety(): int
- getGreasiness(): int
2. Declare a class Cutlery with the following attributes and methods:
- dirtiness: int
- onUse(Eatable): void
  - Increases dirtiness based on the return value of getGreasiness of the parameter.
3. Declare a class Person with the following attributes and methods:
- hunger: int
- eat(Eatable, Cutlery):
  - If the dirtiness of the cutlery is > 0, throw an exception.
  - Eats the Eatable, decreasing the value of hunger based on the return value of getSatiety(). hunger cannot be < 0.
  - calls onUse on the Cutlery object, passing the Eatable as parameter.
4. Implement the following Eatables:
- Pasta: has a “quantity” integer attribute. satiety = quantity * 2, greasiness = quantity * 3
- Apple: low satiety, low greasiness
- Cake: low satiety, high greasiness
5. Implement a main method where the following operations are executed:
- A Person object is allocated
- Three Cutlery objects with names “fork”, “knife” and “spoon”
- An HashMap “menu” is allocated, with strings as keys and Eatables as values. The menu is the following:
  - “first_course”: a Pasta object.
  - “fruit”: an Apple object.
  - “snack”: a Cake object.
- The person uses the fork to eat the first course, the knife to eat the fruit, and a spoon to eat the snack. After being consumed, the value is deleted from the map.
## SQL
Given the following table:
```
Car(
  id VARCHAR(255) PRIMARY KEY,
  nickname VARCHAR(64),
  speed INTEGER,
  productionYear INTEGER
)
```

Write the following queries:
1. Insert a Car entry with random values.
2. Report the count of cars that have been manufactured in a certain year, for each year
value present in the table.
3. Select all cars faster than 200.
4. Select all cars with a nickname, selectings only the nickname and their speed.
