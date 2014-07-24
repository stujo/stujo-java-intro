
# Iterator and Iterable

* The for each construct works on Collections because they implement Iterable

```
public interface Iterable
{
   Iterator<T>	iterator();
}
```


```
public interface Iterator<E>
{
  // Returns true if the iteration has more elements.
  boolean hasNext();

  // Returns the next element in the iteration
  // Throws: NoSuchElementException
  E	next();

 // Removes from the underlying collection the
 // last element returned by the iterator
 // (optional operation ->
 //   UnsupportedOperationException)
 void	remove();
}

```
