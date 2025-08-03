---
Course: C212 Java
---
while loop

```Java
public class loopExample {
	public static void main (String[] args) {
		int x = 1;
		System.out.println("Before the loop");
		while (x < 4) {
			System.out.println("In the loop");
			System.out.println("Value of x is " + x);
				x = x + 1;
			}
			System.out.println("This is after the loop");
		}
	}
	/* output: Before the loop
	In the loop
	Value of x is 1
	In the loop 
	Value of x is 2
	In the loop
	Value of x is 3
	This is after the loop
	*/
	//was in the loop because x was less than 4.once at 4 the loop ends
	
```

  

IF statements