in order to reuse strings multiple times in code we can use variables
for example:
```run-python
message = ("Hello World!")

print(message)
print(message)
#what this does is that it outputs Hello World!
```
in the code block above we stores the string "Hello World!" in a variable called **message.** 
- After storing it in that variable called **message** we passed the variable instead of the string
- what this does is that it allows me to print the same string multiple times without having to retype the entire string
- variables are like containers that hold values


**variable naming**
in the code above i named my string variable message
- the name of a variable is how i can refer to it in my code later on
- this means that i cant have 2 different variables with the same name
	- for example if wanted to store the capital of the United Kingdom i could name it **capital_of_uk**, this is good because its easy to understand and its descriptive
```run-python
	capital_of_uk = "London"
	print(capital_of_uk)

```
- there are some strict rules for naming variables, if i break them i get an error
	- variable names can only contain letters, numbers, and underscores
	- they cant start with a number
	- cant contain spaces
	- cant be the same as a Python keyword like `for`, `if`, etc...
- TIPS
	- names should be descriptive and easy to understand because it makes my code easier to maintain and understand
	- in large codebases, you can easily forget what a variable does if it has a bad/irrelevant name

NAMING CONVENTIONS
- there are many different naming conventions
	- Camel Case: the first letter of each word is capitalized except for the first word
		- `myVariableName`
	- Snake Case: words are separated by underscores
		- `my_variable_name`
	- Pascal Case: the first letter of each word is capitalized
		- `MyVariableName`
- Python typically uses snake case, which means that we use underscores to separate words in variable names
	- Example:
```run-python
python_creation_date = "February, 1991"
java_creation_date = "May, 1995"
javascript_creation_date = "December, 1995"

print(python_creation_date)
print(java_creation_date)
print(javascript_creation_date)
```
