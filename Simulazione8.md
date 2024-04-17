# Java 23 - Checkpoint #2
## Java Advanced
It is possible to implement constructors, setter, getters or any other additional method where it is considered necessary.
1. Declare an interface Washable with the following methods:
- wash(): boolean
  - This method should return true if the object was dirty enough to be washed, otherwise it should return false
2. Declare a class Dishwasher with the following attributes and methods
- capacity: int
- loadedObjects: List\<Washable\>
- load(Washable): void
  - Adds the Washable object to loadedObjects.
  - Launches an exception if the length of loadedObjects is equal to capacity.
- launchWash(): boolean
  - Calls wash() on every item in loadedObjects, then empties loadedObjects. Returns true if and only if all elements were cleaned.
3. Declare the following classes representing washables:
- Fork
  - Has a “dirtyness” integer attribute.
  - wash() returns false if dirtyness is 0, otherwise sets dirtyness to 0 and returns true.
- PlasticSpoon
  - Has a "color" string attribute
  - wash() always returns false 
4. Implement a main method where:
- A Dishwasher object with capacity = 3 is allocated.
- An HashSet of 4 Washable objects is allocated. One of them should be a plastic spoon with color "red", and another one should be a Fork with dirtyness = 0.
- The set of Washables is printed to screen.
- All objects of the list are loaded into the Dishwasher through the load(...) method. If an exception is thrown when an item is loaded a message must be printed on screen, but other loads should be executed anyway.
- The launchWash() method is called and the return value is printed to screen.

## SQL
Given the following table:
```
Author(
  username VARCHAR(64) PRIMARY KEY,
  fullName VARCHAR(64),
  shares INTEGER,
)

Post(
  id VARCHAR(255) PRIMARY KEY,
  authorName VARCHAR(64) FOREIGN KEY REFERENCES Author(username),
  likes VARCHAR(64),
  shares INTEGER,
)
```

Write the following queries:
1. Insert a Post entry with random values.
2. Report the count of posts for each author present in the table.
3. Select all users which posts have gained more than 50 likes in total.
4. Select all authors without any shares.
