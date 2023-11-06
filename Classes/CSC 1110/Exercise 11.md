My javadoc
```java
/**
 * Interface for a schedulable object
 */
public interface Schedulable {
    boolean isBusy(int day, int hour);
    boolean add(Schedulable item);
    boolean remove(Schedulable item);
    String getName();
}
```
