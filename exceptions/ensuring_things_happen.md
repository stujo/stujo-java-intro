# Ensuring things Happen

* Storage Locker Example

```

import java.util.ArrayList;
import java.util.List;

public class App {
	public static void main(String[] args) {
		System.out.println("Hello World!");

		String storageLocker[] = new String[5];

		List<String> myStuff = new ArrayList<String>();

		myStuff.add("Sofa");
		myStuff.add("Table");
		myStuff.add("Bed");
		myStuff.add("Fridge");

		openStorageLocker(storageLocker);

		moveStuff(myStuff, storageLocker);

		closeStorageLocker(storageLocker);
	}

	private static void moveStuff(List<String> myStuff, String[] storageLocker) {
		for (int i = 0; i < myStuff.size(); i++) {
			String thing = myStuff.get(i);

			System.out.println("Adding '" + thing + "' to storage Locker #"
					+ storageLocker.hashCode());

			storageLocker[i] = thing;
		}
	}

	private static void openStorageLocker(String[] storageLocker) {
		System.out.println("Open Storage Locker #" + storageLocker.hashCode());
	}

	private static void closeStorageLocker(String[] storageLocker) {
		System.out.println("Closing Storage Locker #"
				+ storageLocker.hashCode());
	}
}


```
