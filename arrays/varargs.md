# Varargs

* Implicit Array Creation for Parameters

```
static void doSomething(String... withThese) {
	for (String that : withThese) {
		System.out.println(that);
	}
}
```
