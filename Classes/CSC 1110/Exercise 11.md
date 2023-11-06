My javadoc
```java
/**
 * Interface for a schedulable object
 */
public interface Schedulable {
	/** Returns if the user is busy during a time block 
	 * 
	 */
    boolean isBusy(int day, int hour);
    boolean add(Schedulable item);
    boolean remove(Schedulable item);
    String getName();
}
```
