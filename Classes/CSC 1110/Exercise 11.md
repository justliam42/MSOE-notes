My javadoc
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
