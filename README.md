# Anagram-python
# approach1 Using sorted() function
# function to check if two strings are
# anagram or not 
def check(s1, s2):
	
	# the sorted strings are checked 
	if(sorted(s1)== sorted(s2)):
		print("The strings are anagrams.") 
	else:
		print("The strings aren't anagrams.")		 
		
# driver code 
s1 ="listen"
s2 ="silent"
check(s1, s2)

# approach2 Using Counter() function
# Python3 program for the above approach
from collections import Counter

# function to check if two strings are
# anagram or not
def check(s1, s2):

	# implementing counter function
	if(Counter(s1) == Counter(s2)):
		print("The strings are anagrams.")
	else:
		print("The strings aren't anagrams.")


# driver code
s1 = "listen"
s2 = "silent"
check(s1, s2)

# approach3 Using Inbuilt List and Sort() Methods
## Example 1 for "The strings are anagrams."

#Declare Inputs
inp1 = "listen"
inp2 = "silent"

#Sort Elements
x = [inp1[i] for i in range(0,len(inp1))]
x.sort()
y = [inp2[i] for i in range(0,len(inp2))]
y.sort()

# the sorted strings are checApproach#5:using list and dictionaryked
if (x == y):print("The strings are anagrams.")
else: print("The strings aren't anagrams.")

## Example 2 for "The strings aren't anagrams."

#Declare Inputs
inp1 = "listen"
inp2 = "silenti"

#Sort Elements
x = [inp1[i] for i in range(0,len(inp1))]
x.sort()
y = [inp2[i] for i in range(0,len(inp2))]
y.sort()

# the sorted strings are checked
if (x == y):print("The strings are anagrams.")
else: print("The strings aren't anagrams.")

# Approach4:using list and dictionary
s1 = "dad"
s2 = "bad"

char_list_1 = list(s1)
char_list_2 = list(s2)

char_count = {}

for char in char_list_1:
	if char not in char_count:
		char_count[char] = 0
	char_count[char] += 1

for char in char_list_2:
	if char not in char_count:
		print("The strings are not anagrams.")
		break
	char_count[char] -= 1

else:
	for count in char_count.values():
		if count != 0:
			print("The strings are not anagrams.")
			break
	else:
		print("The strings are anagrams.")


