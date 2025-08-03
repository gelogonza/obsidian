---
Course: C212 Java
Date: 2024-01-25
---
## Strings in Java

- immutable sequences of characters, enclosed in double quotes; “Hello World!”
    - since they are immutable they cannot change after being created. Any modifications results in a new string
- Not primitive data types like int or double but are objects of the **String** class
- The last index of a string is the length of the string minus 1
    
      
    

## String Methods

- Length: `String.length()` returns the number of characters in a string
- Concatenation: Use `+` or `concat()` to join strings.
- Character reveal: `String.charAt(index)` retrieves a character at a specified position (0-based index)
- Substring: `String.substring(start, end)` extracts part of a string
- Index of substring: `String.indexOf(”substring”)` gives the starting position of a substring or -1 if not found. Can’t have a negative index
    - Case-sensitive
    - can specify starting position from index
- Equality: use `String.equals()` instead of `==` to compare string content
- Lexicographical Order: Strings are compared alphabetically with `compareTo()`
- Contains: returns true f sequence is found
    - case-sensitive
    - more convenient than indexOf when you only need to check presence
- CompareTo: return negative if string lexigraphically precedes argument
    
    - case-sensitive
    - based on unicode value of characters
    - returns 0 if strings are equal
    - returns positive of this string lexicographically follows argument
    
      
    

## Examples of each method

### Declaring and creating strings

```Java
//Declaration and Initialization
String greeting = "Hello World!";
String emptyString = ""; //empty string with no characters
```

### Getting the length of a string

```Java
String s = "Hello";
int length = s.length(); Returns 5
```

### Concatenation

```Java
//Concatenation 
String s1 = "Hello";
String s2 = "World";
String s3 = s1 + " " + s2; // prints "Hello World"
```

```Java
String firstName = "Angelo";
String lastName = "Gonzalez";
String fullName = firstName + " " + lastName; //"Angelo Gonzalez"
```

### Finding Substring

```Java
String sentence = "I love Java!";
int index = sentence.indexOf("Java"); //returns 7
```

### Extracting Substrings

- substring is a smaller string taken from another string

```Java
String s = "programming";
String sub = s.substring(0, 6); //"program"
```

### Character Retrieval

```Java
char c = s.charAt(2); //'c'
```

```Java
String s = "Java";
char firstChar =. s.charAt(0); //'J' (index starts at 0)
```

### Checking Equality

- strings should be compared using `.equals(`) not `==`(which compares memory locations)

```Java
String s1 = "Hello";
String s2 = "Hello";
boolean isEqual = s1.equals(s2); //true
```

  

## Advanced String features

### String Immutability

- When modifying strings, a new one is created

```Java
String s = "Hello";
s = s + " World"; //creates a new string "Hello World"
```

- Use StringBuilder for efficient modifications

```Java
StringBuilder sb = new StringBuilder("Hello");
sb.append("World"); // "Hello World" 
```

### Lexicographical Comparison

- Strings are compared alphabetically using `.compareTo()`

```Java
String a = "apple";
String b = "banana";
int result = a.compareTo(b); // negative because apple < banana
```

## Full example: String Manipulations

```Java
public Class stringExamples {
		public static void main(String[] args) {
				String s = "Java Programming";
				
				//Get length
				System.out.println("Length: " = s.length());

				//Get a character
				System.out.println("First character: " + s.charAt(0));

				//Substring
				System.out.println("Substring: " +s.substring(5, 16));

				//Concatenate
				String newString = s + " is fun!";
				System.out.println(newString);

				//Compare strings
				System.out.println("Equal? " + s.equals("Java Programming"));
    }
}
```

  

# Section 2.1 Conditionals

- Conditionals are statements that allow you to run different code depending on whether a condition is true or false.
- Think of it as asking “if this happens, then do that.”

### Syntax of if-Else statements

```Java
if (condition) {
		//code runs if condition is true
} else if (another condition) {
		//code runs if another condition is true
} else {
    //code runs if all conditions are true
}
```

**Example**

```Java
int age = 20;
if (age < 18) {
		System.out.println("Minor");
} else if (age >= 18 && age < 65) {
		System.out.println("Adult");
} else {
		System.out.println("Senior");
}
/*  age < 18: if the age is less than 18, the first block executes
		age >= 18 && age < 65: the && operator ensures both conditions are true
				(age has to be at least 18 and less than 65)
else: handles all remaining cases where age is 65 or greater
```

### Switch Statements

- best for checking one variable against multiple values
    - each case must end with a break to prevent running into the next case(fall-through)
    - default runs if no cases match

```Java
switch (variable) {
	case value1
				//code implementation
	case value2
				//implementation
	default:
				//code
}
```

```Java
int day = 2;

switch (day) {
		case 1:
				System.out.println("Monday");
				break;
		case 2:
				System.out.println("Tuesday");
				break;
		case 3:
				System.out.println("Wednesday");
				break;
		default:
				System.out.println("Other day");
}
```

### Example of switch statement

- Simple Calculator

```Java
char operator = '+'

switch (operator) {
	case '+':
			System.out.println("Addition selected.");
			break;
	case '-':
			System.out.println("Subtraction selected.");
			break;
	default:
			System.out.println("Invalid operator.");
}
//Cases: each case checks if the variable matches a spec. value
//break statement: prevents the execution from falling thru to next cases
//default: handles unmatched cases
```

### Logical operators

- && AND short circuiting operator: ensures both condtions are true

```Java
if (a > 0 && b > 0) {
	System.out.println("Both numbers are positive.");
}
```

- || OR short circuiting operator: ensures at least one condition is true

```Java
if (a > 0 || b > 0) {
		System.out.println("At least one number is positive.");
}
```

- ! NOT

```Java
if (!(a > 0)) {
		System.out.println("a is not positive.");
}
```

### Advanced: Ternary Operator

- Compact way to write simple conditionals
- syntax: condition ? valueIfTrue : valueifFalse

```Java
int age = 20;
String result = (age < 18) ? "Minor : Adult";
System.out.println(result); //Prints "Adult" if age >= 18
```

### Mistakes to avoid

- forgetting to use `break` in switch
- misusing == instead of .equals() for comparing objects (e.g., strings)

### Practice example: Grading system

```Java
public class Grading {
    public static void main(String[] args) {
        int score = 85;

        if (score >= 90) {
            System.out.println("Grade: A");
        } else if (score >= 80) {
            System.out.println("Grade: B");
        } else if (score >= 70) {
            System.out.println("Grade: C");
        } else {
            System.out.println("Grade: F");
        }
    }
}
```