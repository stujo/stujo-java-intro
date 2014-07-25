# Fibonacci Example


```

List<Integer> myList = new ArrayList<Integer>();

myList.add(0);
myList.add(1);

int limitLength = 10;

int nextFib;

while (myList.size() < limitLength) {

	nextFib = myList.get(myList.size() - 1)
		+ myList.get(myList.size() - 2);

	myList.add(nextFib);
}

System.out.print(myList);


```
