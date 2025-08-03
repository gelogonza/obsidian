---
Course: C212 Java
---
- Classes are blueprints for objects
    
    - when creating a class we declare a new type of object
    - encapsulate data and method definitions for later use
    - to create a class use the ‘class’ keyword then use the name of the class
        - name of the class should be capitalized and describe a noun
            - CLASS : Fruit
            - OBJECT: Apple, Banana, Mango
            - CLASS: Car
            - OBJECT: Volvo, Audi, Honda
    
    ### Example of a class w/ object
    
    ```Java
    public class Main {
    		int x = S;
    		
    		public static void main(String[] args) {
    					Main myObj = new Main();
    					System.out.println(myObj.x);
    		}
    ]
    ```
    
    ### Example of multiple objects
    
    ```Java
    public class Main {
    			int x = 5;
    			public static void main(String[] args) {
    			Main my Obj1 = new Main();
    			Main myObj2 = new Main();
    			System.out.println(myObj1.x);
    			System.out.println(myObj2.x);
    		}
    ]
    ```
    
    ### Using multiple classes
    
    - can create an object of a class and access it in another class
    - name of the java file should match the name of the class
    - below are [Main.java](http://Main.java) and [Second.java](http://Second.java)
    
    ```Java
    public class Main {
    		int x = 5;
    }
    ```
    
    ```Java
    class Second {
    			public static void main (String[] args) {
    						Main myObj = new Main();
    						System.out.println(myObj.x);
    				}
    }
    
    //after complining both files the output should be 5
    ```
    
    - they can inherit methods from other classes; relationship called the superclass/subclass
    - ‘Object’ class is the ultimate superclass
        - Object class has 3 methods
            - ‘equals’ - for comparing 2 classes for equality
            - ‘toString’ - stringifying an object
            - ‘hashCode’ - returns the hash code of a string
                
                ```Java
                public class Main {
                	public static void main(String[] args) [
                		String myStr = 'Hello'
                		System.out.println(myStr.hashCode());
                		}
                		}
                		//ouput: 69609650
                ```
                
                ```Java
                public int hashCode()  // hashCode also returns as an int
                ```