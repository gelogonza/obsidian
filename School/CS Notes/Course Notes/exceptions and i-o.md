---
Course: C212 Java
Date: 2025-04-14
---
- what is an exception?
    - control flow altering operation
        - control flow operators
    - reasons for exceptions? unexpected situations
        
        ```Java
        if (n ==) return 1;
        else return n * fact (n-1);
        ```
        
        if we enter a number < 0, the method will infinitely recurse, which leads to a StackOverflow error, It’s handled by:
        
        ```Java
        if(n < 0) throw new llegalArgumentException("");
        else if(n == 0) return 1;
        else return n * fact (n - 1);
        ```
        

  

- exceptions versus errors
    - errors are something you dont want to encounter, think of a StackOverflowError; which means something s wrong with your program’s logic which led to that crash
    - when you forget to use a .limit() on a stream, it leads to an OutOfMemoryError, and crashes
- unchecked versus checked exception
    - Unchecked - excpetion you dont have to surround with a try-catch block
    - checked - wont compile if you dont havea try catch block
- Some types of exceptions
    - ArrayIndexOutOfBoundsException
    - NullPointerException
    - RuntimeException
    - ArithmeticException
    - ClassCallException
    - IndexOutOfBoundsException
- read and write content from a file
- try catch block
- wrap tests in lamda for try catch junit test
    - assertThrows
    - illegal argument
        - illegalargumentexception.class
    - Superclass of IOException
        - filenotfoundexception
- I/O means input and output

```Java
/* returns the contents of the file as a string */

static String readFile(String fileName) {
	try (FileInputStream fis = new FileInputStream(fileName)) {
		String result = “”;
		while (true) {
			int nextValue = fis.read(); 
			if (nextValue == -1) {
				break;
			} 
			else {
				result += (char) nextValue; 
			}
		}
		return result; 
	}
	catch (IOException e) {
		throw new RuntimeException(e);
	}
} 
```

```Java
static String readFile(String fileName) {
	try (FileInputStream fis = new FileInputStream(fileName)) {
		String result = “”;
		while (true) {
			int nextValue = fis.read(); 
			if (nextValue == -1) {
				break;
			} 
			else {
				result += (char) nextValue; 
			}
		}
		return result; 
	}
	catch (IOException e) {
		throw new RuntimeException(e);
	}
} 
```

```Java
static List<String> getLines(String 
```

- dont use throws