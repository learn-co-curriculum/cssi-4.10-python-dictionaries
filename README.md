---
tags: cssi, python, string methods
level: 2
languages: python
---
#Python Dictionaries

#Objectives:
+ Understand the syntax of dictionaries in Python
+ Compare the differences of dictionaries and lists

#Motivation
We've seen how to use strings to print words to the command line - just like we printed words to with the javascript console and the python interpreter. But strings have way more power than we've seen so far. We'll look at some of the powerful functions python has for dealing with strings.

#Dictionaries
When you open up a dictionary, what do you see? Words and their definitions. Dictionaries function are like that - they contain pairs of keys, which are usually words, and values. Dictionaries are like lists, but instead of having numbers as indexes, the indexes are something else - usually strings. Check it out:

<img src ="dictionary.png">

In this example, we can associate each of the items on our grocery list with its price. We don't really care about the order of the grocery list - it is way more helpful to know how much each item will cost!

Think of keys like the words in a dictionary and the values as the definitions. A dictionary holds pairs of keys and values. A key in a dictionary must be unique and associated with a value.

How do we use them? The python syntax for declaring a dictionary is with {curly brackets}. To create an empty dictionary, just set a variable equal to curly braces:
```
empty_dict = {}
```
To create a dictionary with values in it, set key-value pairs separated by colons and commas:
```
my_cart = {'Eggs': 2.59,
'Milk': 3.19,
'Cheese': 4.80,
'Yogurt': 1.35,
'Butter': 2.59,
'More Cheese':6.19 }
```
Keys are usually strings, because they are easier to read, but they can be other data types too.  Values can be anything!

They could be strings:
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}
```
or lists:
```
cartoon_friends = {'bugs': ['daffy','porky', 'foghorn leghorn'],
                   'mickey': ['minnie', 'goofy', 'donald'],
                   'woody': ['buzz', 'rex', 'slinky'],}
```
or other dictionaries:
```
cartoon_relationships = {'friends' : cartoon_friends,
                         'species' : cartoon_species }
```
#Key-Value Pairs
key-value pairs are separated by comma
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}
```
***Keys*** are on the left of the colons (‘bugs’, ‘elmer’, ‘wiley’, ‘tomas’, ‘jerry’)
***Values*** are on the right of the colons (‘rabbit’,‘human’,‘coyote’,‘cat’, ‘mouse’)

Just as in a regular dictionary, the keys must be unique, otherwise the program will throw an error.
```
my_dict = {'bugs': 'rabbit',
      	'bugs': 'non-rabbit'}
```
Also, it doesn't make sense to have two different values for the same key, so python will throw an error.

#Accessing values in dictionary
We get the values out of the dictionary much like we got values out of lists. In order to access the values of a dictionary, you want to pass the key to the dictionary and it will return the value.
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

print my_dict['elmer']
```
#Updating a dictionary
To modify the values inside a dictionary, the same thing applies - you want to use the assignment operator and send it the key value.
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

my_dict['bugs'] = 'bunny' #reassigns rabbit to bunny
```
You can also use this technique to add key-value pairs to a dictionary that don’t already exist. For instance, with my_dict, I could do the following:
```
my_dict['tweety'] = ‘bird’
print my_dict

{'tom': 'cat', 'wiley e': 'coyote', 'elmer': 'human', 'bugs': 'bunny', 'jerry': 'mouse', 'tweety': 'bird'}
```
The {"tweety": "bird"} key value pair has now been added to my_dict.

#Common Dictionary Operations
```
len(my_dict)
5

my_dict.clear()
{}

del my_dict['bugs']
{‘elmer’: ‘human’,
‘wiley e’: ‘coyote’,
‘tom’: ‘cat’,
‘jerry’: ‘mouse’}
```
#Searching for a Key in a Dictionary
What if you wanted to check if the key 'jerry' was in my_dict?  Use the in operator.
```
if 'jerry' in my_dict:
 print 'Hi Jerry!'
```
This only works for keys in a dictionary, not the values.

#Looping over a dictionary
It is often useful to be able to loop over the contents of a dictionary. Using the for-in loop we would write:
```
for cartoon in my_dict:
 print cartoon
```
What do you notice? What is it printing? It’s printing the keys!
```
bugs
elmer
wiley e
tom
jerry
```
How would you print the values? Combine the technique of accessing the dictionary through the key:
```
for cartoon in my_dict:
 print my_dict[cartoon]
```
This prints:
```
rabbit
human
coyote
cat
mouse
```

#In Conclusion
Remember dictionaries are just like lists but rather than having and index (0,1,2,3) you have keys for each value!
