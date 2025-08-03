- programming language for iOS, macOS, and any other OS in the apple ecosystem
- Originally written in Objective-C
- Type safe language

variable in Swift

```Swift
var AngeloGonzalez
func didDoubleTapDrink(_ sender:
		UITap
```

type annotations

- variable and constant types can be inferred, however you may also provide a type animation when they are declared

```Swift
var welcomeMessage: String implies Declaration
wellcomeMessage = "Welcome!"
```

Collection types

- swift supports Arrays, sets, and Dictionaries
    - mutability pf a collection is dependent upon wehther it is defined as a variable or a constant
    - collections are generic: they can hold any type, but all elements must be of the same type
    - index arrays go 0,1,2,3 and 0= value 1 = value 2, 3= value 4
        - applies for these types
    - sets and its values are colletion of things in a set
- Arrays
    
    - create an array of a specified type by using initializer syntax
    - elements can be accessed and modified using the arrays methods and properties or subscript syntax
    
    ```Swift
    // Creates a new array to contain String values
    var groceryList: [String] = []
    
    // Adds an item
    groceryList.append("eggs")
    
    // Append another array
    groceryList += ["cheese", "apples"]
    
    // Accesss and modify a value
    groceryList[2] = "tomatoes"
    
    // Prints the number of items in the list
    print(groceryList.count)
    
    // Prints the valid indices
    print(groceryList.indices)
    ```
    

Dictionaries

- Keys and Values
    - Examples:
    - MSP → Minneapolis
    - LAX → Los Angeles
    - IAD → Washington DC
    - Key → Values

Functions

```Swift
func findHypotenuse(side1: Double, side2, Double) -> Double {
let sideSquared = side1 * side1 + side2 * side2
return sqrt(sideSquared)
)

let hypotenuse = findHypotenuse(side1: 8.0, side2: 6.0)

//func -> function declaration keyword
//(side1: Double, side2: Double) is the parameter format; parameterName: Type
//Double -> return format
```

  

  

```Swift
import UIKit

struct Person {
		let name: String
		var age: int
}

class ViewController: UIViewController {

	override tune viewDidLoad() {
		super: viewDidLoad()
		
		let firstPerson = Person(name: "angelo", age: 23)
		let secondPerson = Person(name: "bob", age: 21)
		
		print(firstPerson.age)
		
		//array of persons
		var allPeople: [Person} = [firstPerson]
		//can also do this, which is preferred
		varallPeople = [firstPerson
		allPeople.append(secondPerson)
		
		
		var setOfNames: Set<String> = [firstPerson.name, secondPerson.name] //set of different names
		
		//dictionary
		var dictionary: [String: int] = [:]
		dictionary["angelo"] = 23
		
		dictionary["angelo"]
		
		}
	
	
	
	}}
```

  

func printThis() → String(

return ‘’

}

  

func noPrint(input: String) {

// does nothing if empy

}

  

func addValues(a: Int, b: String, c: [String]

  

Closures:

- closures are built of functions
- arbitrary blocks of code which can be passed and executed at some point in time
    - like an anonymous function in JavaScript or Python
- can be assigned to variables
- Closures capture (or enclose) variables from the surrounding context
- closure format:
    
    ```Swift
    { (<Parameters>) -> <Return Type> in
    
    	<Statements>
    	
    }
    ```
    

```Swift
// function

func saysHello() {
		print("Hello")
)

//call the function
saysHello()
```

```Swift
// Closure

var greeting = {
    print("Hi There!")
}

// Call the closure
greeting()
```

```Swift
override func viewDidLoad() {
	super.viewDidLoad()
	
	
	}
	
	var fullName: {String, String -> String in
		return "/(first) \(second)"
	
	}
	
	func someFunction(val1: String, val2: String, closure: (String, String) -> String) -> String {
	
```

|   |   |   |   |
|---|---|---|---|
||**Python**|**Java**|**Swift**|
|variable|**num_students = 25**|**int numStudents = 25**|**var numberOfStudents = 25**|
|constant|**GRAVITY = 9.8**|**final int GRAVITY = 9.8**|**let gravity = 9.8**|

- value of a constant cannot change once it has been declared, whereas the value of a variable can
- you can declare multiple constants or variables on a row separated by commas
- if you dont plan to change a value, store it as a constant

  

**Naming Conventions**

- include all words needed to avoid ambiguity
- Omit needless words
- Name variables, parameters, and types according to their roles (rather than avoid constraints)
- avoid abbreviations

Case conventions

- names of types and protocols are UpperCamelCase
    - everything else is lowerCamelCase

```Swift
var kartView0
var kartView1
var kartView2

func didDoubleTapKart(_ sender:
				UITapGestureRecognizer) {
}

func didPinchKart(_ sender:
				UIPinchGestureRecognzer) {
}
```