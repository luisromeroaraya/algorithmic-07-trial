# [Trial by pseudo code](https://github.com/becodeorg/BXL-Swartz-4-27/blob/master/1.The-Field/7.Algorithmic/07-trial.adoc)
* Type of challenge: **consolidation**
* Duration: **2 hours**
* Turn in method: **email**
* Team challenge: **solo**

## Missions objectives
At the end of this challenge you should have improved your understanding of:
* variables
* conditions
* loops
* arrays
* functions

## The mission
Now that you know the fundamental concepts of programming, it’s time to test your newly acquired knowledge in a trial. Complete the exercises below in a [text file](https://en.wikipedia.org/wiki/Text_file), then send it to your coach by **email**.

## Exercises
Instructions
* complete the exercises in a text file
* send the file to your coach

*I will be using [Python3](https://repl.it/languages/python3) to write and test the algorithms*

I - list of random numbers
- [x] Write a function which returns an array of *n* random numbers, *n* being the **only** received **parameter**.
```
import random
def randomArr():
    array=[]
    n=int(input("Please enter the number of elements for an array (1-10):"))
    for x in range(n):
        array.append(random.randint(1,10))
    return array

array=randomArr()
print(array)  
```

II - translate
- [ ] The main goal of pseudo code is to write down the logic behind an algorithm, so that you can easily **translate** it into *human speech* or *code*.

Given the algorithm below
```
function in_array(element,list_elements) {
	boolean exist = false
	for I = 0 until length($list_elements) do {
		if $element == $list_elements[I] then {
			$exist = true
		}
	}
	return $exist
}
```
- [x] with your word explain its purpose
```
The algorithm looks inside a given list for a certain element and returns a boolean response.
```
* translate it into *Python* and *Javascript*


III - sort an array
- [x] Write a function which receives an array of ten random integers as **parameter** and returns an ascendantly ordered array of integers.
```
import random
def randomOrderedArr():
    array=[]
    newArray=[]
    n=int(input("Please enter the number of elements for an array (1-10):"))
    for x in range(n):
        array.append(random.randint(1,10))
    for i in range(0,len(array)):
        for j in range(0,len(array)-i-1):
            if array[j] > array[j+1]:
                array[j], array[j+1] = array[j+1], array[j]
    return array
    
array=randomOrderedArr()
print(array)
```
