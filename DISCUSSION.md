# ECE 2112: Advanced Computer Programming and Algorithms
## EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING
### Aaron Siegfreid R. Jugo
### 2ECE-A
### 9/1/2026 




### **Task 1: Word Rotation Problem**
In the first task, we were asked to create a function that rotates a word by moving the first character to the end while keeping the remaining letters in their original order and capitalization.

To solve this, I used basic sequence indexing and slicing. The slicing expression `text[1:]` takes all characters starting from index 1 to the end, and adding` text[0] `places the very first character at the back:

`return text[1:] + text[0]`

During testing, I noticed that spaces inside or around the word would disrupt the text formatting. To address this, I used `.replace(" ", "")` to clean out spaces first. I also made sure that passing an empty string won't cause an error.


The procedures are as follows:
- make variable `x` that removes the spaces from the string by using `.replace(" ","")`;
- make another variable `t` that ignores the first character and inputs after by using indexing; and 
- return `t`.

`def rotate_word(text):`\
  `  x = text.replace(" ","")`\
 `   t = x[1:] + x[0]`\
`    return t`\

`text = input("\nInput your own word: ")`\
`rotate_word(text)`\

The code returned an output that meets the required result of the second task.


`rotate_word("python")` -> "ythonp"\
`rotate_word("logic")` -> "ogicl"\
`rotate_word("Code")` -> "odeC"\
`rotate_word("A")` -> "A"\



### **Task 2: Username Builder Problem**
Moving on to the second task, we were tasked to create a function that accepts two strings: first_name and last_name. The function must:

1. Convert all letters to lowercase.
2. Remove all spaces from the first name.
3. Remove all spaces from the last name.
4. Join the processed first and last names using one period (.).

Using basic string methods, I was able to write code that runs properly by assigning two strings to lowercase in a variable and using the `.replace(" "."")` 
to remove the spaces.

The procedures are as follows:
- make variable `x` that lowercases the first name element by using `.lower()`;
- make another variable `y` that lowercases the last name element by using `.lower()`; and
- return the value with added codes `x.replace(" ", "") + "." + y.replace(" ", ""))` to add the dot.

`def make_username(first_name, last_name):`\
`    x = first_name.lower()`
 `   y = last_name.lower()`\
 `   return (x.replace(" ", "") + "." + y.replace(" ", ""))`\


The code returned an output that meets the required result of the second task.

`make_username("Ada", "Lovelace")` -> "ada.lovelace"\

`make_username("Alan", "Turing")` -> "alan.turing"\

`make_username("Ana Maria", "De Leon")` -> "anamaria.deleon"\



### **Task 3: Username Builder Problem**

The last task was to create a function that accepts a list containing at least two elements, and unpacks it into three variables:

• first: the first element;

• middle: a list containing everything between the first and last elements;

• last: the last element;


It swaps the first and last elements without changing the order of the middle elements; it resembles the first task but is more complex.

Using sequence indexing and unpacking, I was able to write code that swaps the first and last elements without changing the middle elements. 


The procedures are as follows:
- make the first element be the last using `items[-1]`;
- make the middle element by using `items[1:-1:1]`;
- make the middle variable unpack by using `*`;
- make `items = first, *middle, last` to create the list in that following order; and
- return the variable `items`.



`def swap_bookends(items):`\
   ` first = items[-1]`\
    `middle = items[1:-1:1]`\
  `  last = items[-0]`\
    `items = first, *middle, last `\
    `return items `\


The code returned an output that meets the required result of the last task.
`swap_bookends([1, 2, 3, 4, 5, 6])` -> [6, 2, 3, 4, 5, 1]\
`swap_bookends(["red", "green", "blue"]) `-> ["blue", "green", "red"]\
`swap_bookends([8, 3])` -> [3, 8]\


