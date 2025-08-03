---
Course: C212 Java
---
```Java
public class Main {

    // variable = a reusable container for a value
    // 1. declare the variable
    // 2. assignment for the variable
        //primitive stored in memoru
        //reference variables are stored in a heap
    //data types - int, double, string, boolean, chars
    //doubles have decimals
    //ints are for whole numbers
    //chars are letters and use single quotes '' dont forget!
    //booleans return true/false
    //Strings are series of characters which use double quotes ""
    public static void main(String[] args) {
        String name = "Angelo";
        String alcohol = "Beer";
        String favBeer = "Coors Banquet";
        String food = "tacos";
        String email = "angelo@gmail.com";

        int yearInCollege = 3;
        int age = 23;
        int year = 2025;

        double price = 79.99;
        double temperature = 69.5;
        double majorGPA = 3.7;

        boolean isDrunk = true;
        boolean isNotDrunk = false;
        boolean isOnline = true;

        char gender = 'M';
        char grade = 'A';
        char failing = 'F';


        if(isDrunk) {
            System.out.println("You are drunk!");
        }
        if(isNotDrunk){
            System.out.println("You are sober!");
        }
         
        System.out.println(name);
        System.out.println("My name is " + name +" I am "+ age +" my favorite food to eat is" + food + " my favorite beer is "+ favBeer);
        System.out.println("My grade in Discrete Mathematics is " + grade + " my gpa is "+ majorGPA);
        System.out.print(" Im currently in year " + yearInCollege);
        System.out.print("The year is " + year);
    }
}
```