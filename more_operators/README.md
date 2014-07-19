# More Operators

* Ternary Operator
 * `?`
* Bitwise Operators (bitmasking and shifts)
 * ``<<``, ``>>``, ``>>>``
 * [Explaination](http://stackoverflow.com/questions/141525/absolute-beginners-guide-to-bit-shifting#141873)

* __EXERCISE:__ Write a simple app which applies these in a loop to integer values
  * Integer.toBinaryString(x)

* Read more about them [here](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/op3.html)

```
class BitDemo {
    public static void main(String[] args) {
        int bitmask = 0x000F;
        int val = 0x2222;
        // prints "2"
        System.out.println(val & bitmask);
    }
}
```
