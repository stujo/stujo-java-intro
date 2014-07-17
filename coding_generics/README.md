# Coding Generics
##Generics In your Classes (Java Platform)

###Exercise
* __EXERCISE:__   Given this Interface:

Save it as _GenericStack.java_
```
interface GenericStack<T> {
  void push(T obj) throws GenericStackFullException;
  T pop() throws GenericStackEmptyException;
}
```
In separate files define ``GenericStackEmptyException``, ``GenericStackFullException`` and a working implementation of ``GenericStack`` called ``ArrayBasedGenericStack``.

``ArrayBasedGenericStack`` should have a single constructor which takes an ``int`` parameter which is the size of the fixed array to be used to back up the Stack. We are looking for a _LIFO_ : _Last in First Out_ stack.

Before you start coding your implementation, write a JUnit 4 TestCase called ``ArrayBasedGenericStackTest`` which Test the behaviour.
Use ``@Test(expected = GenericStackEmptyException.class)`` to annotate some of your tests

* [Bounded and Unbounded Generics](http://docs.oracle.com/javase/tutorial/java/generics/bounded.html)
