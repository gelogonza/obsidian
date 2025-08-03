---
Course: C212 Java
---
```Java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
	
		Scanner scanner = new Scanner(System.in);
		
		System.out.print("Enter you name: ");
		String name = scanner.nextLine();
		
		System.out.print("Enter your age: ");
		int name = scanner.nextInt(); //if i input a double i would get an error
		
		System.out.println("What is your gpa: ");
		double gpa = scanner.nextDouble();
		
		System.out.println("Are you a student: ");
		boolean isStudent = scanner.nectBoolean();
		
		
		System.out.println("Hello " + name);
		System.out.println("You are " + age + " years old");
		System.out.println("Your gpa is " + gpa);
		
		if(isStudent) {
			System.out.println("You are enrolled as a student")
		
		
		scanner.close();
```