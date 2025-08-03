---
Course: C212 Java
Date: 2025-03-31
---
### What is an interface?

- they are a way of grouping classes/sets of classes together
- cant instantiate an interface because it would mean its an object, which it isnt
- **Comparable** interfaces is implemented by classes that we want to be able to inhibit “comparable” behavior

### Relationship between Class and Interfaces

- a class can extend another class
- a interface can extend another interface
    
    - **However** a class can implement an interface, but a interface cant implement a class
    
    ![[/image 5.png|image 5.png]]
    
    ### Vehicle interface using ‘implements’
    
    ```Java
    interface Vehicle {
    
    		void changeGear(int a);
    		void speedUp(int a); 
    		void applyBrakes(int a);
    }
    //the Bicycle class implementing the above Vehicle interface
    class Bicycle implements Vehicle{
    		int speed;
    		int gear;
    		
    		//changing gears
    		@Override
    		public void changeGear(int newGear){
    			gear = newGear;
    		}
    		
    		//increase speed
    		@Override
    		public void speedUp(int increase){
    			speed = speed + increase;
    		}
    		
    		//decrease speed
    		@Override
    		public void applyBrakes(int decrease){
    			speed = speed + decrease;
    		}
    		public void printStates() {
    			System.out.println("SPEED: " + speed + "GEAR: " + gear);
    		}
    	}
    	
    	//Motorcycle class implementing the vehicle interface
    	class Motorcycle implements Vehicle{
    			int speed;
    			int gear;
    			
    			//changing gears
    			@Override
    			public void changeGear(int newGear){
    				gear = newGear;
    			}
    			
    			//increase speed
    			@Override
    			public void speedUp(int increase){
    				speed = speed + increase;
    			}
    			
    			//decrease speed
    			@Override
    			public void applyBrakes(int decrease){
    				speed = speed + decrease;
    			}
    			public void printStates() {
    				System.out.println("SPEED: " + speed + "GEAR: " + gear);
    			}
    		}
    		
    		class Main{
    			public static void main(String[] args){
    				Bicycle bicycle = new Bicycle
    					bicycle.changeGear(2);
    					bicycle.speedUp(3);
    					bicycle.applyBrakes(1);
    					
    					System.out.println("Bicycle present state is: ");
    					bicycle printStates();
    					
    					Motorcycle motorcycle = new Motorcycle
    					motorcycle.changeGear(6);
    					motorcycle.speedUp(5);
    					motorcycle.applyBrakes(5);
    					
    					System.out.println("Motorcycle present state is: ")
    					motorcycle.printStates();
    			}
    	}
    	
    	/* Bicycle present state is: speed:... gear:...
    			Motorcycle present state is: speed:... gear:... */
    					
    	
    ```
    
    ### Comparable
    
    ```Java
    class Employee implements Comparable<Employee> {
    		private final String NAME;
    		private final int AGE;
    		private final int SALARY;
    		
    		Employee(String name, int age, int sal) {
    			this.NAME= name;
    			this.AGE = age;
    			this.SALARY = sal;
    		}
    	}
    ```
    
    - **compareTo** must be implemented by any class that implements the **Comparable** interface
    - natural ordering pairs the class implements Comparable
    - we first compare the names, if same name then we do a comparison based on salary
        - if same name and same salary, then compare against ages. otherwise it doesn’t matter
    
    ```Java
    @Override
    public int compareTo
    	(Employee oth) {
    if (!this.NAME equals(oth.NAME){
    return
    }else{
    if(this.SALARY < oth.SALARY) {
    return -1;
    }else if(this.SALARY > oth.SALARY) {
    }else{
    return 0;
    
    //not optimal and time consuming 
    ```
    
    - now lets consider a second way to order Employee instances
        
        ### Comparator
        
        ```Java
        class EmpSalCmp implements Comparator<Employee> {
        @Override
        public int compare(Employee e1, Employee e2) {
        	return e1.getSalary() - e2.getSalary();
         }
        }
        ```
        

  

```Java
class Rect implements IShape {
		private final int W/L;
		
		Rect(...)
		
		public double ...() {
		return this.L * this.W;
		
		public double ....
```

```Java
class Circle implements IShape {
	private final int R;
	Circle (...)...
	
@Override
public double area() {
	return Math.PI......

@Override}
public double perimeter(){
	return 2 + Math.PI + this.R
	}
}
```

```Java
interface IShape {
		double area();
		double perimeter();
	}
	//now any class that implements IShape must override area and perimeter.
	 // the classses in this instance would be Rect and Circle
	
```

- How are the objects ordered?

```Java
double perimeter = 0;
List<IShape>... = new ArrayList<>()
for (IShape o; ...) {
		perimeter ++ o.perimeter();
```

### Dynamic Dispatch

- **Polymorphism**
    - one of the four pillars of OOP
    - objected oriented term for classes implementing some shared interface, but them doing it differently
    - a real world example would be when students go home. everyone goes home differently, some walk, some drive, some take the bus, some scooter but they all go home
    - Designing a simple expression tree interpreter to showcase Polymorphism/Dynamic Dispatch
        
        - consider ‘5+(3+4)’. According to PEMDAS we do 3+4 = 7 +5 = 12
        
        ```Java
        interface IExpr {
        		int eval();
        }
        class Num implements IExpr {
        	private int n;
        	Num(int n) {
        		this.n = n;
        	}
        	
        	@Override
        	public int eval() {
        		return n;
        	}
        }
        	class Add implements IExpr{
        		private final IExpr LEFT;
        		private final IExpr RIGHT;
        		Add(IExpr left.IExpr right) {
        			this.LEFT = left;
        			this.RIGHT = right;
        }
        @Overide
        public int eval() { 
        	return this.LEFT.eval() + this.RIGHT.eval();
        	}
        }
        
        ```