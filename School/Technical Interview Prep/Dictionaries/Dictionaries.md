- Key-value pairs for fast lookups
- Use cases for dictionaries
    
    - used for efficient retrieval and updating of data by unique keys
    
    Example Diagram:
    
    ![[/image 3.png|image 3.png]]
    
    So according to the image keys pair with values so ‘b’ is paired with beauty
    
    ‘j’ is paired with joy, and ‘c’ is paired with computing
    
    - similar to lists because indices are paired with values
        - in a list you start from index 0 and move on
            - 0 is value 1
            - 1 is value 2
            - 2 is value 3
- Common Use Cases
    - Frequency maps: in a frequency map you count the frequency of chars in a string of elements in a list
    - Key-value data storage: You store data for quick lookups like a phonebook or user settings

  

Given a list of strings ‘words’ group the strings that are anagrams of each other

- an anagram is defined as a word formed by rearranging letters of another, such as ‘eat’ and ‘tea’
    - look at each string
    - sort it to get the letters in order
    

```Python
def group_anagrams(words):
		anagrams = {}
		for word in words:
			key = sorted(word)
			if key not in anagrams:
					anagrams[key] = []
			anagrams[key].append(word)
		return anagrams.values()
		
print(group_anagrams(["eat", "tea", "ate", "tan", "bat", "nat"
	
```

  

given an integer list nums, return true if any value appears at least twice in the list, adn return false if every element is distinct

```Swift
def contains_duplicate(nums):
    seen = set()
    for num in nums:
        if num in seen:
            return True  # We've seen this number before
        seen.add(num)  # Add it to the set of seen numbers
    return False  # No duplicates found
    
print(contains_duplicate([1, 2, 3, 4]))      # False
print(contains_duplicate([1, 2, 3, 1]))      # True
```

- set() is used because it checks membership in a set is O(1) on average
- once looping thru each number in the list
    - if already in the set → True, theres a duplicate
    - otherwise add to the set
- if loop finishes without returning early, that means all numbers were distinct → False

Also use a set like in this problem becuase of the time complexity, allows to check if something exists fast