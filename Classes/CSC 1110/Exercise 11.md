## 1: My Javadocs
```java
/**
 * Interface for a schedulable object
 */
public interface Schedulable {
	/** 
	 * Returns if the user is busy during a time block 
	 * @param day the day requested
	 * @param hour the hour requested
	 */
    boolean isBusy(int day, int hour);
	/**
	 * adds an item to the schedule
	 * @param item the item to add
	 * @return if the operation was successful
	 */ 
    boolean add(Schedulable item);
	/** 
	 * Remove an item from the schedule
	 * @param the item to remove
	 * @return if the operation was successful
	 */
    boolean remove(Schedulable item);
	/** 
	 * returns the name of the item
	 * @return the name of the item
	 */
    String getName();
}
```

## 2: ChatGPT's Javadocs
```java
/**
 * The Schedulable interface represents an entity that can be scheduled for various time slots.
 * Implementing classes should provide functionality to manage scheduling and check availability.
 */
public interface Schedulable {

    /**
     * Checks if the entity is busy at a specified day and hour.
     *
     * @param day  The day of the week (0 for Sunday, 1 for Monday, ..., 6 for Saturday).
     * @param hour The hour of the day (0 to 23).
     * @return true if the entity is busy at the specified day and hour, false otherwise.
     */
    boolean isBusy(int day, int hour);

    /**
     * Adds a Schedulable item to the schedule of this entity.
     *
     * @param item The Schedulable item to be added to the schedule.
     * @return true if the item was successfully added, false if it couldn't be added.
     */
    boolean add(Schedulable item);

    /**
     * Removes a Schedulable item from the schedule of this entity.
     *
     * @param item The Schedulable item to be removed from the schedule.
     * @return true if the item was successfully removed, false if it couldn't be removed.
     */
    boolean remove(Schedulable item);

    /**
     * Gets the name of the entity.
     *
     * @return The name of the entity as a String.
     */
    String getName();
}
```

## 3: Compare Javadocs
ChatGPT's Javadocs are much more robust, probably because I was a bit lay with them. It also understood exactly what this interface was doing quite quickly. I may have been more concise, but ChatGPT's answer provided better documentation overall.

## 4: ChatGPT's UML diagram
```sql
+-------------------+
|    Schedulable   |
+-------------------+
| - isBusy(int, int): boolean     |
| - add(Schedulable): boolean     |
| - remove(Schedulable): boolean  |
| - getName(): String             |
+-------------------+
```
note: I'm not entirely sure if considering the methods as private is correct.

## 5: ChatGPT's extended UML diagram
```sql
+-------------------+
|    Schedulable   |
+-------------------+
| - isBusy(int, int): boolean     |
| - add(Schedulable): boolean     |
| - remove(Schedulable): boolean  |
| - getName(): String             |
+-------------------+
       ^
       |
       |
+------------------+
|    Calendar      |
+------------------+
| - items: List<Schedulable>     |
| - name: String                |
| - startOfDay: int             |
| - endOfDay: int               |
+------------------+
| + Calendar(String, int, int, Schedulable...): Calendar |
| + Calendar(String, Schedulable...): Calendar          |
| + isBusy(int, int): boolean                           |
| + add(Schedulable): boolean                          |
| + remove(Schedulable): boolean                       |
| + getName(): String                                   |
| + toString(): String                                 |
| - getScheduleMatrix(): int[][]                       |
+------------------+
```

## 6: what's missing
The plaintext diagram has some issues making the boxes look clean, additionally, in a plain text representation of UML, you need to use textual descriptions and conventions creatively to convey the same information that would be visually represented in a graphical UML diagram.

## 7: Drawing
I did this in Visio:
![[Pasted image 20231106113608.png]]