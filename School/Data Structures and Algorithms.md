Data Structure:

- can be defined as a way to store and organize data so that it can be used efficiently
- named location that can be used to store and organize data
    - large amounts of data is processed by different systems and if not stored properly, leads to data loss
    - easier to search for a particular data if it is organized in a proper format
    - help programs minimize the usage of resources such as memory and space
- can be linear and non-linear

  

Stacks:

- LIFO Data structure: Last in first out
- stores objects into a sorted “vertical tower”
- push() to add to the top
- pop() to remove from the top
- peek() at item at the item at the top of the stack
- empty check if empty
- search the stack


		run-java
		import java.utils.Stack
	
		public class Main{
		public static void main(String[] args) {
	
			Stack<String> stack = new stack<String>();
			
			stack.push("Minecraft"(;
			stack.push("Destiny");
			stack.push("GTA V");
			stack.push("Rainbow Six Siege");
			stack.push("Valorant");
			
			
			//examples
			//returns false since the stack isnt empty
			System.out.print(stack.empty()); 
			
			//returns list of items in the stack
			System.out.print(stack);
			
			stack.pop(); //removes Valorant
			stack.pop(); //removes Rainbow Six Siege
			stack.pop(); //removes GTA V
			stack.pop(); //removes Destiny
			stack.pop(); //removes Minecraft
			//since stacks are LIFO it removes the last object in the stack hence why Valorant goes 1st, then R6, etc...
			//if i pop again i get an Exception called EmptyStackException because the stack is emoty
			
			String myFavGame = stack.pop();
			System.out.println(stack);//this removes Valorant becuase i popped it and assigned it to the variable myFavGame
			System.out.println(myFavGame);//returns Valorant
			
	
	}
}




