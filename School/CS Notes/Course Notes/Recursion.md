---
Course: C212 Java
Date: 2025-01-27
---
### Recursion

- occurs when a method calls itself to solve a smaller instance of a problem
    - **base case** which stops the recursion
    - **recursive case** which reduces the problem and calls itself

```Java
public class Factorial {
		public static int factorial(int n) {
			if (n ==0) {
					return 1; //base case
			}
			return n * factorial(n - 1); //recursive call
	}
	
	public static void main(String)[] args) {
			System.out.println(factorial(5)); //output: 120
	 }
}	 
```

### Common Recursive problems

### Fibonacci Sequence

```Java
public class Fibonacci {
		public static int fibonacci(int n) {
				if (n <= 1) {
						return n; // base case
				}
				return fibonacci(n - 1) + fibonacci(n - 2); //recursive call
			}
			
			public static void main(String[] args) {
				System.out.println(fibonacci(7)); //output: 13
```

### Sum of an Array

```Java
public class ArraySum {
		public static int sum(int[] arr, int n) {
				if (n <= 0) {
						return 0; //base case
				}
				return arr[n - 1] + sum(arr, n - 1); //recursive call
			}
			
			public static void main(String[] args) {
					int[] numbers = {1, 2, 3, 4, 5);
					System.out.println(sum(numbers, numbers.length)); //output: 15
			}
	}
```

### Tail Recursion

Tail recursion is a special case of recursion where the recursive call is the last operation in the method. The key advantage is that it can be optimized by the compiler to use constant stack space, effectively turning it into a loop.

- Characteristics of tail recursion:
    - The recursive call is the last operation in the method
    - No operations are performed on the result of the recursive call
    - More memory efficient than regular recursion

### Example: Factorial with Tail Recursion

```Java
public class TailFactorial {
    public static int factorial(int n) {
        return factorialHelper(n, 1);
    }
    
    private static int factorialHelper(int n, int accumulator) {
        if (n == 0) {
            return accumulator; // base case
        }
        return factorialHelper(n - 1, n * accumulator); // tail recursive call
    }
    
    public static void main(String[] args) {
        System.out.println(factorial(5)); // output: 120
    }
}
```

### Example: Sum Array with Tail Recursion

```Java
public class TailArraySum {
    public static int sum(int[] arr) {
        return sumHelper(arr, 0, 0);
    }
    
    private static int sumHelper(int[] arr, int index, int accumulator) {
        if (index >= arr.length) {
            return accumulator; // base case
        }
        return sumHelper(arr, index + 1, accumulator + arr[index]); // tail recursive call
    }
    
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};
        System.out.println(sum(numbers)); // output: 15
    }
}
```

Notice how in both examples, the recursive call is the last operation and its result is immediately returned without any additional computation. This makes it possible for the compiler to optimize the recursion into a loop, preventing stack overflow for large inputs.

L

Here are the examples with detailed inline documentation:

### Regular Recursion - String Reversal

```Java
/**
 * Reverses a string using regular recursion
 * @param str The input string to reverse
 * @return The reversed string
 */
public static String reverse(String str) {
    // Base case: if string is empty, return it
    if (str.isEmpty()) {
        return str;
    }
    // Recursive case: take first char and put it at end of reversed substring
    return reverse(str.substring(1)) + str.charAt(0);
}
```

### Tail Recursive - String Reversal

```Java
/**
 * Main method to reverse a string using tail recursion
 * @param str The input string to reverse
 * @return The reversed string
 */
public static String reverse(String str) {
    return reverseHelper(str, "");
}

/**
 * Helper method that does the actual tail recursive reversal
 * @param str The remaining string to process
 * @param acc The accumulator containing the reversed portion
 * @return The final reversed string
 */
private static String reverseHelper(String str, String acc) {
    if (str.isEmpty()) {
        return acc;  // Base case: return accumulated result
    }
    // Tail recursive call: add current char to front of accumulator
    return reverseHelper(str.substring(1), str.charAt(0) + acc);
}
```

### Regular Recursion - Power Function

```Java
/**
 * Calculates base raised to exp power using regular recursion
 * @param base The base number
 * @param exp The exponent
 * @return base raised to exp power
 */
public static int power(int base, int exp) {
    if (exp == 0) {
        return 1;  // Base case: anything raised to 0 is 1
    }
    // Recursive case: multiply base with base^(exp-1)
    return base * power(base, exp - 1);
}
```

### Tail Recursive - Power Function

```Java
/**
 * Main method to calculate power using tail recursion
 * @param base The base number
 * @param exp The exponent
 * @return base raised to exp power
 */
public static int power(int base, int exp) {
    return powerHelper(base, exp, 1);
}

/**
 * Helper method that does the actual tail recursive calculation
 * @param base The base number
 * @param exp Remaining exponent to process
 * @param acc Accumulator storing intermediate result
 * @return The final result
 */
private static int powerHelper(int base, int exp, int acc) {
    if (exp == 0) {
        return acc;  // Base case: return accumulated result
    }
    // Tail recursive call: multiply current acc by base
    return powerHelper(base, exp - 1, acc * base);
}
```

Remember that in tail recursion, the recursive call must be the last operation, and no additional computations are performed after the recursive call returns. This optimization allows the compiler to transform the recursion into a loop, making it more memory efficient.