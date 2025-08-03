---
Course: C212 Java
Date: 2025-01-13
---
  

```Java
//want a method to convert a given temp in Fahrenheit to Celsius
//FtoC(32)--> 0
//FtoC(212) --> 100
//FtoC(-40) --> -40
/* Test Driven development: write examples for our method then use those to 
design a method */


//Class is the name
/* converts temperature from fahrenheit to celsius
* @ return f temp in degrees C */
class TempConverter{
	/* method header */static double FtoC(double F){
					return(F-32)*(5/9); //wont work 
					return(F-32)*(5.0/9.0); //this works
					//only really encounter this issue with division
					//can occur with all primitive operations

//method body

	}

}
```

double- data type is for decimals

Syntax includes a return type; double, method name, and parameters

methods are often declared static for utility purposes

int- is for integers

method FtoC returns a double value

  

  

# Test Driven Development

@Test

```Java
//Example of test using JUnit
@Test
void testfToC() {
		Assertions.assertEquals{0, TempConverter.fToC(32)); // 32ºF is 0ºC
}
```

- when writing test methods dont use static

```Java
void test FtoC(){
		assertEquals(expected ouput, actual output
}
```

```Java
void test FtoC(){
		assertEquals(100, TempConverter.FtoC(212));
		assertEquals(-40, TempConverter.FtoC(-40));
		asserEquals(-17.78, TempConverter.FtoC(0),0.01/*delta value*/);
	}
}
```

  

```Java
//VARIABLES

int x = 5;
double y = 7.4;
char a = 'c';
boolean b = true;

double z = x + y; //12.4
int w = x + y; //causes a compile-time error, next line fixes the issue
int w = (int) (x+y); // this works bc ur telling this to interpret as an int

double q = x * 10; //50.0 
double u = x + 5 * 10 - 8.0; //47.0 due to PEMDAS
	
```

```Java
class PointDistance{
/* Finds the distance between the points
@param x1
@param y1
@param x2
@param y2
@ return hypotenuse between point 1 and 2
*/
		static double Distance(int x1, int y1, int x2, int y2){
			return Math.sqrt(Math.pow(x2-x1, 2)+ Math.pow(y2-y1, 2));

}
```

```Java
class PointDistanceTest{
	@Test
	void test PtDistance(){
		assertEquals(Math.sqrt(18),
		PointDistance.ptDistance(0,0,3,3);

(x2-x1) * (x2-x1)
Math.pow (x2-x1, 2);
	}
}
```

## Primitive data Types:

- int, double, char, boolean, etc…
- integers are 32 bit, doubles are 64-bit floating points
- follows strict typing, case-sensitive unlike dynamically typed languages

### common issues

- integer division (for example; 5 / 9 equals 0 unless one operand is a double).
- remember the importance of using Math.pow and Math.sqrt for calculations

```Java
int a =  5 / 9; //results in 0 because both operands are integers
double b = 5.0 / 9 // correct way, returns 0.555...
```

### String Manipulation

- strings in java are immutable
- common operations would be:
    
    ```Java
    String s = "Hello, ";
    s = s + "World!"; //concatenates to form "Hello, World!"
    System.out.println(s.length()); //output would be 13 (length of string)
    ```
    

  

### Standard input/output (I/O)

- standard output with system.out:
    - print methods:
        - System.out.println() : adds a newline at the end
        - System.out.print() : prints without adding a newline.
        - System.out.printf(): formats the output string
            - Example:
                
                ```Java
                System.out.printf("The result is: %.2f\n", 3.14159);
                //%.2f formats to 2 decimal places
                ```
                

|   |   |   |
|---|---|---|
|Format Specifier|Description|Example|
|%d|integer|42|
|%f|floating-point|3.14|
|%s|string|Hello|
|%c|character|H|
|%b|boolean|true|

Formatted output table above for reference ^

  

### Standard input with a scanner

in order to read from the console:

```Java
Scanner in = new Scanner(System.in); // creates a scanner object
int num = in.nextInt(); //reads an integer
String str = in.nextLine(); //reads a line of text
```

Common issues:

- nextInt() reads an integer but leaves a newline in the buffer
- Fix to the issue
    
    ```Java
    int num = in.nextInt();
    in.nextLine(); // Consumes the remaining newline
    ```
    

  

## Example: Simple Calculator

```Java
import java.util.Scanner;

class Calculator {
		public static void main(String[] args) {
				Scanner in = new Scanner(System.in);
				System.out.print("Enter first number: ");
				int a = in.nextInt();
				System.out.print("Enter second number: ");
				int b = in.nextInt();
				System.out.println("Sum: " + (a + b));
		}
}
```

  

# 1.4

### Generating random numbers:

- Using ==Random== ==class:==
    
    ```Java
    Random random = new Random();
    int randomNum = random.nextInt(10); //generates a number in [0,9]
    ```
    
    - nextInt(n) generates a number between 0 and n-1
- Custom range example