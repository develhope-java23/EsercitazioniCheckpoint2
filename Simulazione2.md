# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Washable with the following methods:
- onWash(): void
- shouldBeWashed(): boolean
2. Declare a class WashingMachine with the following attributes and methods
- water: int
- capacity: int
- loadedObjects: Set<Washable>
- load(Washable): void
  - Adds the Washable object to loadedObjects.
- wash(): Set<Washable>
  - Calls onWash on every item in loadedObjects, then returns this set and allocates a new empty Set, assigning it to the loadedObjects attribute.
3. Declare the following classes representing washables:
- Shirt
  - Has a “color” string attribute.
  - Has a “cleanliness” integer attribute.
  - shouldBeWashed() returns true if cleanliness < 90.
  - onWash() sets cleanliness += 20.
- Pants
  - Has a “material” string attribute.
  - Has a “cleanliness” integer attribute.
  - Has an additional “ripped” boolean attribute.
  - shouldBeWashed() returns true if cleanliness < 90 and “ripped” is
  false.
  - onWash() sets cleanliness += 20. Plus, it has a 50% chance to set
  ripped = true.
4. Implement a main method where:
- A WashingMachine object is allocated.
- A LinkedList of 3 Washable objects is allocated. One of them should be
ripped Pants.
- The list of Washables is printed to screen.
- All objects of the list are loaded into the WashingMachine through the load(...)
method.
- The wash() method is called and the return value is saved into a variable,
which is suddenly printed to screen.
- A message is printed for every returned Washable that should be washed
again.

## SQL
Given the following table:
```
Cat(
  microchipCode VARCHAR(255) PRIMARY KEY,
  fullName VARCHAR(64),
  nickname VARCHAR(64),
  age INTEGER,
)
```
Write the following queries:
1. Insert a Cat entry with random values.
2. Report the count of cats that have a certain age, for each age value present in the
table.
3. Select all cats older than 10.
4. Select all cats without a nickname.
