<a href="https://colab.research.google.com/github/sensei-jirving/code-reviews-week-1-python-basics/blob/solution/Code_Review_Loops%2C_Dictionaries%2C_and_OOP_SOLUTION.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Code Review Activity:  Loops, Dictionaries, and OOP - SOLUTION

- Week 1
- Written by James Irving

- Reviewing some Python Basics from the Pre-Bootcamp work


## Concepts Reviewed/Practiced:



- Creating Lists and Dictionaries
- Conditionals (If/else)
- Creating a Nested Dictionary
- For loops
    - Looping through dictionaries
- Bonus: Object-Oriented-Programming

## Instructor/TA Data

- Use the table below to reference the different favorite items for each instructor/TA.

|Name|Favorite Color| Favorite Candy|Role |
| --- | --- | --- | ---|
|James|Purple|Jelly Bellies|Instructor |
|Purvi|Red | Milky Way bars| TA|
|Adam|Blue |Snickers | TA |
|Josh|Green| Skittles | Instructor|


<!-- 
{'James':{'color':'Purple',
                      'candy':'Jelly Bellies'},
              'Purvi':{'color':'Red',
                       'candy':'Milky Way bars'} ,
              'Adam':{'color':'Blue', 
                      'candy':'Snickers'},
              'Josh':{'color':'Green', 
                       'candy': "M&M's"}} -->




# Reviewing Datatypes

## Lists


```python
## make a list of all everyone name from the table
names = ['James','Purvi','Adam','Josh']
names
```




    ['James', 'Purvi', 'Adam', 'Josh']



### Slicing / List Indexing


```python
## slice out the first name from names (what index # is first item?)
names[0]
```




    'James'




```python
## slice out the last name from names (what index # is last item?)
names[-1]
```




    'Josh'




```python
## slice out the first TWO names from names
names[:2] #OR names[0:2]
```




    ['James', 'Purvi']



### Looping through Lists

- For each person, print "Hello world, my name is \<their name>"




```python
## for each name, print Hello, my name is <name>
for name in names:
    print(f"Hello world, my name is {name}!")
```

    Hello world, my name is James!
    Hello world, my name is Purvi!
    Hello world, my name is Adam!
    Hello world, my name is Josh!


### Nested Lists (lists within lists)

- Now, let's make a list of all attendee's names and favorite their favorite color.
    - Each item in the list will also be a list that contains `['Name','Fav Color']`
    - This will be a **nested list**


```python
## make a list of all attendee's names and favorite color 
## Each attendee will become a list of 2 things, name and color
names = [ ['James','Purple'],['Purvi','Red'],['Adam','Blue'],['Josh','Green']]
names
```




    [['James', 'Purple'], ['Purvi', 'Red'], ['Adam', 'Blue'], ['Josh', 'Green']]




```python
# What does the first item in our list look like now?
names[0]
```




    ['James', 'Purple']




```python
## What is the last person in the lists favorite color?
names[-1][-1]
```




    'Green'



>- Now loop through our nested list and print the following for each person:
    - "Hello, world! My name is \<name> and my favorite color is \<color>."


```python
## Loop through names list again,
# but slice out the correct index for [name, color] for your string
for person_info in names:
    print(f"Hello, world! My name is {person_info[0]} and my favorite color is {person_info[1]}.")
```

    Hello, world! My name is James and my favorite color is Purple.
    Hello, world! My name is Purvi and my favorite color is Red.
    Hello, world! My name is Adam and my favorite color is Blue.
    Hello, world! My name is Josh and my favorite color is Green.


>- ***But what if we had a massive list and we wanted to look up a specific person's favorite color?***
    - Dictionaries to the rescue!

## Dictionaries

> Instead of a nested list, let's create a dictionary
with the person's name as the key and their fav color as the value.


```python
## Instead of a nested list, let's create a dictionary
# with the person's name as the key and their fav color as the value.

fav_colors = {'James':'Purple',
              'Purvi':'Red',
              'Adam':'Blue',
              'Josh':'Green'}
fav_colors
```




    {'James': 'Purple', 'Purvi': 'Red', 'Adam': 'Blue', 'Josh': 'Green'}




```python
# what is James's favorite color?
fav_colors['James']
```




    'Purple'



>- Now loop through our dictionary and print the same message as our nested list.:
    - "Hello, world! My name is \<name> and my favorite color is \<color>."


```python
## Loop through our fav_colors dict and print the above statement
for name,color in fav_colors.items():
    print(f"Hello, world! My name is {name} and my favorite color is {color}.")
```

    Hello, world! My name is James and my favorite color is Purple.
    Hello, world! My name is Purvi and my favorite color is Red.
    Hello, world! My name is Adam and my favorite color is Blue.
    Hello, world! My name is Josh and my favorite color is Green.


### Nested Dictionaries

>- What if we wanted to keep track of **multiple pieces of information** for each person? 
    - We want to keep track of each persons:
        - favorite color
        - favorite candy



- Instead of a nested list, **let's create a dictionary with each person's name** as the first/outer key. 

- For each person's, the value stored in the outer dictonary will no longer be a string: it will be another dictionary!!
    - Each name will now have a dictionary as its value, and the dictionary will contain "color" and "candy"





```python
## make a dictionary of fav_items with the names as the key and a dictionary of {color:red,candy:jelly bellies}
fav_items = {'James':{'color':'Purple',
                      'candy':'Jelly Bellies'},
              'Purvi':{'color':'Red',
                       'candy':'Milky Way bars'} ,
              'Adam':{'color':'Blue', 
                      'candy':'Snickers'},
              'Josh':{'color':'Green', 
                       'candy': "M&M's"}}


fav_items.keys()
```




    dict_keys(['James', 'Purvi', 'Adam', 'Josh'])




```python
## What does the value for James look like now?
fav_items['James']
```




    {'color': 'Purple', 'candy': 'Jelly Bellies'}




```python
## what is James's fav candy?
fav_items['James']['candy']
```




    'Jelly Bellies'




```python
## what is Adam's fav color?
fav_items['Adam']['color']
```




    'Blue'




```python
## now loop through nested dictionary and print
## my name is ___, my favorite color is ___, and my favorite candy is __

for name,fav_dict in fav_items.items():
    print(f"My name is {name}, my favorite color is {fav_dict['color']}, and my favorite candy is {fav_dict['candy']}")
```

    My name is James, my favorite color is Purple, and my favorite candy is Jelly Bellies
    My name is Purvi, my favorite color is Red, and my favorite candy is Milky Way bars
    My name is Adam, my favorite color is Blue, and my favorite candy is Snickers
    My name is Josh, my favorite color is Green, and my favorite candy is M&M's


### Updating Dictionaries


```python
## james decided he hates purple. His new fav color is Brown. Update the dictioanry to reflect this
fav_items['James']['color'] = "Blue"
```


```python
## confirm that james' fav color is now brown
fav_items['James']['color'] 
```




    'Blue'



### Loops with Conditionals (if/else)

>- **Next, we want to print two different messages, depending on if the candy is chocolatey or fruity.**

- **First, we will need a way to look up if a candy is chocolately or fruity** 
    - We already have two lists for us below.

- **Second, we will loop trough our list of names and use if/else to print:**
    - If their candy is chocolatey:
        - "My name is`<name>`  and I love chocolatey candy."
    - If their candy is fruity:
        - "My name is `<name>` and I love fruity candy."

    - If their candy is in neither list:
        - "My name is `<name>` and I like exotic candy."


```python
## LEAVE THESE LISTS AS THEY ARE!
chocolate_list = ['Snickers','Milky War bars',"M&M's","Hershey's Bar"]
fruity_list= ['Jelly Bellies','Skittles','Starbursts','Gummy Worms']
```


```python
## Loop through our dict of fav_items
for name, favorites in fav_items.items():

    ## If the person's fav candy choclate:
    if favorites['candy'] in chocolate_list:
         print(f"My name is {name} and I love chocolatey candy.")

    ## if the person's fav candy is fruity
    elif favorites['candy'] in fruity_list:
        print(f"My name is {name} and I love fruity candy.")      

    ## if the persons candy is exotic.
    else:
        print(f"My name is {name} and I love exotic candy.") 

```

    My name is James and I love fruity candy.
    My name is Purvi and I love exotic candy.
    My name is Adam and I love chocolatey candy.
    My name is Josh and I love chocolatey candy.


# BONUS: Object-Oriented-Programming 

- Our `fav_items` dictionary above is a perfect candidate for creating a class. 

- Our `Person` class will:
    - have a name
    - have a fav color
    - have a fav candy
    - will have a method called `.hello()` that will print out: "👋Hello, world! My name is ___, my favorite color is ____, and my favorite candy is ___


```python
class Person:
    def __init__(self, name,fav_color,fav_candy):
        self.name = name
        self.color = fav_color
        self.candy = fav_candy

    def hello(self):
        msg = f"""👋Hello, world! My name is {self.name}. My favorite color is {self.color}
and my favorite candy is {self.candy}.\n"""
        print(msg)

    
```


```python
# now, create a new list called people_list 
people_list = []

# loop through our fav_dict and create a new Person for each person in fav_dict
for name,fav_dict in fav_items.items():
    person = Person(name,fav_dict['color'], fav_dict['candy'])

    ## Maken sure to save the person to your people_list
    people_list.append(person)

```


```python
## take a look at People list to confirm there are 4 people
people_list
```




    [<__main__.Person at 0x7fdfa13d3970>,
     <__main__.Person at 0x7fdfa13d3e50>,
     <__main__.Person at 0x7fdfa13d3f70>,
     <__main__.Person at 0x7fdfa13d3fd0>]




```python
## Loop through our list of people and run the .hello method

for person in people_list:
    person.hello()
```

    👋Hello, world! My name is James. My favorite color is Blue
    and my favorite candy is Jelly Bellies.
    
    👋Hello, world! My name is Purvi. My favorite color is Red
    and my favorite candy is Milky Way bars.
    
    👋Hello, world! My name is Adam. My favorite color is Blue
    and my favorite candy is Snickers.
    
    👋Hello, world! My name is Josh. My favorite color is Green
    and my favorite candy is M&M's.
    



```python

```
