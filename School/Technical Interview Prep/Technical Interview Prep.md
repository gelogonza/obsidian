what is something i hope to learn from this course?

- learn how to effectively solve problems and get better in interviews

![[/image 2.png|image 2.png]]

Indexing and length checks in Python Lists

- list in python is like a shelf
- each item has a position(index), starting at 0
- for example:
    
    ```Python
    list = ['a', 'b', 'c']
    # indexes 0, 1,   2
    \#negative indexes would start backwards so starting at c it would go from right to left
    \#which would be -1, -2, -2
    # in order to get the last item it would be last_item = list[-1] which would return 'c'
    ```
    
- if the list is empty it will throw an error

  

In order to get the first item of a list or return None

- check if the list has items
- if it does return lst[0]
- if not then return None

```Python
def get_first(lst):
	if lst:
		return lst[0]
	else:
		return None
		
print(get_first([1,2,3,4,5])) \#should print 1 since its looking for the number at index 0
print(get_first([])) \#returns none since its an empty list
```

  

Get the middle item of a list

- check if the list has values and has an odd number or elements
- variety of ways to solve:
    - can check how many and choose the index the middle number is at
    - OR use len(lst) // 2 to get to the middle index if its an odd number of elements

```Python
def get_middle(lst):
	if lst and len(lst) % 2 == 1:
		middle_index = len(lst) // 2
		return lst[middle_index]
	else:
		return None
```

  

To get to the last index of a list

- use -1 to get the last element in the index from the right
    - most efficient

Examples:

```Python
def get_last(lst):
	return lst[-1]
	
print(get_last([0,6,3,9,2])) \#returns 2 since we're getting the end of the list starting from the right
```

```Python
def get_last(lst):
	if lst:
		return lst[-1]
	else:
		return None
		
print(get_last([0,6,3,2,5])) \#returns 5
print(get_last([])) \#returns None since list is empty
```

  

### UMPIRE Strategy :

- Understand
    - understand what the interviewer is asking with clarifying questions
    - generate basic sample input and output
    - explore more unusual edge cases
    - explore tradeoffs (memory, performance, code simplicity)
- Match
- Plan
    - describe the overall approach in one or two sentences
    - write down steps in English
    - each step should be simple and clear
- Implement
    - translate your plan to code
    - clear plan should be relatively easy to translate
    - look up basic python that you need
- Review
- Evaluate

Also think out loud to let the interviewer know what you’re thinking of

  

  

How to count all the elements in a list

- Example Problem: Write a function that returns the sum of all the elements in a list. Do not use the built-in sum function
    - start with a total of 0
    - loop through each element in a list
    - add each element to the total
    - return the total at the end

```Python
def find_sum(lst):
	total = 0
	for num in lst:
		total += num
	return total
	\#if you're input is 1,2,3,4,5 the expected output would be 15
```

  

Writing a function that returns the product of all numbers in a list without using the math.prod()

- starting point for multiplication is 1
- loop through each number in the list
- multiply into the total
- return the final result

```Python
def multiply_list(lst):
product = 1
for num in lst:
	product *= num
return product
```

  

write a function above_threshold() that takes in a list of integers lst and an integer threshold as parameters. the function iterates through an original list and returns a new list containing only numbers that are greater than threshold

```Python
def above_threshold(lst, threshold):
```

[[Dictionaries]]