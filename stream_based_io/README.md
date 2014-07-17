# Stream Based IO
##Streams (Java Platform)
* (NOT TO BE CONFUSED WITH Java8 Streams for Functional Programming)
* [Streams IO](http://docs.oracle.com/javase/tutorial/essential/io/streams.html)
 * byte streams
 * character streams
 * Blocking
 * Use ``try`` and ``finally`` to close streams when done
 * Notices that the streams are declared and initialized to ``null`` outside of the ``try`` and ``null`` is tested in the ``finally`` block

##Canonical Example: File Byte Stream (Java Platform)

```
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class CopyBytes {
    public static void main(String[] args) throws IOException {

        FileInputStream in = null;
        FileOutputStream out = null;

        try {
            in = new FileInputStream("source.jpg");
            out = new FileOutputStream("target.jpg");
            int c;

            while ((c = in.read()) != -1) {
                out.write(c);
            }
        } finally {
            if (in != null) {
                in.close();
            }
            if (out != null) {
                out.close();
            }
        }
    }
}
```

* __EXERCISE:__ Implement a byte based file copy application which takes two paramters on the command line

##Canonical Example: File Character Stream (Java Platform)


```
import java.io.*;

public class CopyFile {
   public static void main(String args[]) throws IOException
   {
      FileReader in = null;
      FileWriter out = null;

      try {
         in = new FileReader("source.txt");
         out = new FileWriter("target.txt");

         int c;
         while ((c = in.read()) != -1) {
            out.write(c);
         }
      }finally {
         if (in != null) {
            in.close();
         }
         if (out != null) {
            out.close();
         }
      }
   }
}
```

* __EXERCISE:__ Implement a character based file copy application which takes two paramters on the command line


##BufferedStreams

* bytes: ``BufferedInputStream`` and ``BufferedOutputStream``
* character: ``BufferedReader`` and ``BufferedWriter``
* ``flush``



* __EXERCISE:__ Implement a character based file copy application which takes two paramters on the command line using ``BufferedReader`` and ``BufferedWriter``



##Appending to a File
* ``new FileWriter("filename", true)``

* __EXERCISE:__ Use your file copy application as a basis for new utility function which takes a text file and converts all the uppercase letters to lowercase and vice versa. All other characters remain unchanged.
* Recommendation: write a utility method which applies the transformation to a given string first, and test it using TestCases. Then use that method in your app.
* @see ``Character.isUpperCase()``

* __CHECKPOINT:__ Basic File Access
* __CHECKPOINT:__ Stream based IO
