---
Course: C212 Java
---
**1.1 Program Structure & Main Method**

```Java

/**
 * MainApp: Basic greeting and calculation.
 */
public class MainApp {
    public static void main(String[] args) {
        System.out.println("Welcome to the Java Midterm Review!");
        int baseValue = 10, multiplier = 5;
        int result = baseValue * multiplier;
        System.out.printf("Multiplying %d by %d yields %d%n", baseValue, multiplier, result);
    }
}

```

**1.2 Writing Effective Javadocs**

**1.3 Standard I/O & Formatted Printing**

```Java
java
Copy
import java.util.Scanner;
/**
 * IOExample: Reads full name, age, and city.
 */
public class IOExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter your full name: ");
        String fullName = sc.nextLine();
        System.out.print("Enter your age: ");
        int age = sc.nextInt(); sc.nextLine(); // clear newline
        System.out.print("Enter your city: ");
        String city = sc.nextLine();
        System.out.printf("Hello %s, age %d, from %s!%n", fullName, age, city);
        sc.close();
    }
}

```

**1.4 Math Class Usage: 2D Distance**

```Java
java
Copy
/**
 * Computes Euclidean distance between two 2D points.
 */
public static double computeDistance2D(double x1, double y1, double x2, double y2) {
    double deltaX = x2 - x1, deltaY = y2 - y1;
    return Math.sqrt(Math.pow(deltaX, 2) + Math.pow(deltaY, 2));
}

```

**1.5 JUnit Testing Example**

```Java
java
Copy
import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.api.Test;
public class UtilityMethodsTest {
    @Test
    public void testCalculateCircleArea() {
        double expected = Math.PI * 25;
        assertEquals(expected, calculateCircleArea(5.0), 0.0001);
        assertEquals(0.0, calculateCircleArea(0.0), 0.0001);
        assertThrows(IllegalArgumentException.class, () -> calculateCircleArea(-3.0));
    }
    @Test
    public void testComputeDistance2D() {
        assertEquals(5.0, computeDistance2D(0, 0, 3, 4), 0.001);
    }
}

```

────────────────────────────

**2. CONDITIONALS, LOOPS & RECURSION**

**2.1 Conditionals: Number Classifier**

```Java
java
Copy
/**
 * Classifies integer as "Positive", "Negative", or "Zero".
 */
public static String classifyNumber(int n) {
    if(n > 0) return "Positive";
    else if(n < 0) return "Negative";
    else return "Zero";
}

```

**2.2 Loops: Array Sum & Fibonacci**

```Java
java
Copy
/**
 * Sums array elements.
 */
public static int sumArray(int[] arr) {
    int sum = 0;
    for (int num : arr) sum += num;
    return sum;
}

/**
 * Prints Fibonacci numbers up to limit.
 */
public static void printFibonacci(int limit) {
    int a = 0, b = 1;
    while(a <= limit) {
        System.out.print(a + " ");
        int temp = a; a = b; b = temp + b;
    }
    System.out.println();
}

```

**2.3 Recursion: Factorial (Standard & Tail)**

```Java
java
Copy
/**
 * Standard recursive factorial.
 */
public static int factorial(int n) {
    if(n == 0) return 1;
    return n * factorial(n - 1);
}

/**
 * Tail-recursive factorial.
 */
public static int factorialTail(int n) { return factHelper(n, 1); }
private static int factHelper(int n, int acc) {
    return (n == 0) ? acc : factHelper(n - 1, n * acc);
}

```

**JUnit Test for Factorial:**

```Java
java
Copy
@Test
public void testFactorial() {
    assertEquals(120, factorial(5));
    assertEquals(1, factorial(0));
    assertEquals(24, factorialTail(4));
}

```

────────────────────────────

**[BACK SIDE]**

**3. ARRAYS, COLLECTIONS, GENERICS & STREAMS**

**3.1 Arrays & Collections:**

```Java
java
Copy
/**
 * Finds maximum in an integer array.
 */
public static int findMax(int[] arr) {
    int max = arr[0];
    for (int num : arr) if(num > max) max = num;
    return max;
}

/**
 * Reverses a list.
 */
public static <T> List<T> reverseList(List<T> list) {
    List<T> copy = new ArrayList<>(list);
    Collections.reverse(copy);
    return copy;
}

```

**3.2 Generics: Generic maxElement Method**

```Java
java
Copy
/**
 * Returns the maximum element from a list based on comparator.
 */
public static <T> T maxElement(List<T> list, Comparator<T> comp) {
    if (list == null || list.isEmpty()) throw new IllegalArgumentException("Empty list");
    T max = list.get(0);
    for (T e : list) if(comp.compare(e, max) > 0) max = e;
    return max;
}

```

**3.3 Streams: Sum of Even Squares**

```Java
java
Copy
/**
 * Sums squares of even numbers from a list.
 */
public static int sumEvenSquares(List<Integer> numbers) {
    return numbers.stream()
                  .filter(n -> n % 2 == 0)
                  .map(n -> n * n)
                  .reduce(0, Integer::sum);
}

```

────────────────────────────

**4. MIDTERM PROBLEM TEMPLATES & EXAMPLES**

**4.1 Movie Rating Problem (Modified)**

```Java
java
Copy
/**
 * Determines movie rating.
 * @param genre "Action","Comedy","Drama","Horror"
 * @param timeLength runtime in minutes.
 * @param hasViolence, hasStrongLanguage, hasAdultThemes flags.
 * @return rating: "G", "PG", "PG-13", "R", "A"
 */
public static String determineMovieRating(String genre, int timeLength,
                                          boolean hasViolence, boolean hasStrongLanguage,
                                          boolean hasAdultThemes) {
    int ratingNum;
    if(genre.equals("Action") || genre.equals("Horror")) ratingNum = 4;
    else if(genre.equals("Comedy")) ratingNum = 2;
    else if(genre.equals("Drama")) ratingNum = 3;
    else return "Invalid";
    if(timeLength < 70) ratingNum--;
    else if(timeLength > 130) ratingNum++;
    if(hasViolence) ratingNum++;
    if(hasStrongLanguage) ratingNum++;
    if(hasAdultThemes) ratingNum += 2;
    ratingNum = Math.max(1, Math.min(ratingNum, 5));
    switch(ratingNum) {
        case 1: return "G";
        case 2: return "PG";
        case 3: return "PG-13";
        case 4: return "R";
        case 5: return "A";
        default: return "Error";
    }
}

```

**JUnit Test:**

```Java
java
Copy
@Test
public void testDetermineMovieRating() {
    assertEquals("PG", determineMovieRating("Comedy", 80, false, false, false));
    assertEquals("PG-13", determineMovieRating("Drama", 130, false, true, false));
    assertEquals("R", determineMovieRating("Action", 60, true, false, false));
    assertEquals("A", determineMovieRating("Horror", 200, true, true, true));
}

```

**4.2 Word Length (Recursive & Loop Versions)**

```Java
java
Copy
/**
 * Returns max string length (recursive).
 */
public static int findMaxLength(String[] arr) {
    return findMaxLengthHelper(arr, 0);
}
private static int findMaxLengthHelper(String[] arr, int idx) {
    return (idx >= arr.length) ? 0 : Math.max(arr[idx].length(), findMaxLengthHelper(arr, idx+1));
}

/**
 * Returns max string length using loop.
 */
public static int findMaxLengthLoop(String[] arr) {
    int max = 0;
    for(String s : arr) { max = Math.max(max, s.length()); }
    return max;
}

```

**JUnit Test:**

```Java
java
Copy
@Test
public void testFindMaxLength() {
    String[] words = {"apple", "banana", "kiwi", "strawberry"};
    assertEquals(10, findMaxLength(words));
    assertEquals(10, findMaxLengthLoop(words));
}

```

**4.3 Prime Factorization – Factor Tree**

```Java
java
Copy
/**
 * Returns prime factors of n (n>=2).
 */
public static List<Integer> primeFactors(int n) {
    List<Integer> factors = new ArrayList<>();
    for(int i = 2; i <= n; i++) {
        while(n % i == 0 && isPrime(i)) {
            factors.add(i);
            n /= i;
        }
    }
    return factors;
}
/**
 * Checks if n is prime.
 */
public static boolean isPrime(int n) {
    if(n < 2) return false;
    for(int i = 2; i <= Math.sqrt(n); i++) {
        if(n % i == 0) return false;
    }
    return true;
}
/**
 * Returns a factor tree: [n, p, n/p, ...] until n is prime.
 */
public static List<Integer> factorTree(int n) {
    List<Integer> tree = new ArrayList<>();
    tree.add(n);
    List<Integer> factors = primeFactors(n);
    while(!isPrime(n) && !factors.isEmpty()) {
        int p = factors.get(0);
        tree.add(p);
        n /= p;
        tree.add(n);
        factors = primeFactors(n);
    }
    return tree;
}

```

**JUnit Test:**

```Java
java
Copy
@Test
public void testFactorTree() {
    List<Integer> expected = List.of(210, 2, 105, 3, 35, 5, 7);
    assertEquals(expected, factorTree(210));
}

```

**4.4 Interleaving Lists (Generic)**

```Java
java
Copy
/**
 * Interleaves two lists: take m from l1 then n from l2 alternately.
 */
public static <T> List<T> interleave(List<T> l1, List<T> l2, int m, int n) {
    List<T> result = new ArrayList<>();
    int i = 0, j = 0;
    while(i < l1.size() || j < l2.size()){
        for(int count=0; count<m && i<l1.size(); count++, i++) result.add(l1.get(i));
        for(int count=0; count<n && j<l2.size(); count++, j++) result.add(l2.get(j));
    }
    return result;
}

```

**JUnit Test:**

```Java
java
Copy
@Test
public void testInterleave() {
    List<String> l1 = List.of("A","B","C","D","E","F");
    List<String> l2 = List.of("1","2","3","4");
    List<String> expected = List.of("A","B","C","1","2","D","E","F","3","4");
    assertEquals(expected, interleave(l1, l2, 3, 2));
}

```

────────────────────────────

```Plain
pgsql
Copy
Method                     Description
S1 + S2                    Concatenates S2 to S1.
S.length()                 Returns the length of S.
S.charAt(i)                Returns character at index i.
S.substring(i, j)          Returns substring from i (inclusive) to j (exclusive).
S.substring(i)             Returns substring from i to end.
S.indexOf(S')              Returns first index of S' or -1.
S.contains(S')             True if S' is found.
S.repeat(n)                Returns n copies of S.
String.valueOf(v)          Converts v to a string.
Integer.parseInt(S)        Parses S to an integer.

```

```Plain
perl
Copy
Format Specifier    Description
%d                  Integer (int/long)
%nf                 Floating-point (n decimals)
%s                  String
%c                  Character
%b                  Boolean
```