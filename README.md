<a href="https://colab.research.google.com/github/sensei-jirving/code-reviews-week-1-python-basics/blob/main/Code_Review_Loops%2C_Dictionaries%2C_and_OOP_BLANK.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Code Review Activity: Python Basics - Loops and Dictionaries

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
## make a list of all everyones name from the table

```

### Slicing / List Indexing


```python
## slice out the first name from names (what index # is first item?)

```


```python
## slice out the last name from names (what index # is last item?)

```


```python
## slice out the first TWO names from names

```

### Looping through Lists

- For each person, print "Hello world, my name is \<their name>"


```python
## for each name, print Hello, my name is <name>

```

### Nested Lists (lists within lists)

- Now, let's make a list of all attendee's names and favorite their favorite color.
    - Each item in the list will also be a list that contains `['Name','Fav Color']`
    - This will be a **nested list**


```python
## make a list of all attendee's names and favorite color 
## Each attendee will become a list of 2 things, name and color

```


```python
# What does the first item in our list look like now?

```


```python
## What is the last person in the lists favorite color?

```

>- Now loop through our nested list and print the following for each person:
    - "Hello, world! My name is \<name> and my favorite color is \<color>."


```python
## Loop through names list again,
# but slice out the correct index for [name, color] for your string

```

>- ***But what if we had a massive list and we wanted to look up a specific person's favorite color?***
    - Dictionaries to the rescue!

## Dictionaries

> Instead of a nested list, let's create a dictionary
with the person's name as the key and their fav color as the value.


```python
## Instead of a nested list, let's create a dictionary called fav_colors
# with the person's name as the key and their fav color as the value.

```


```python
# what is James's favorite color?

```

>- Now loop through our dictionary and print the same message as our nested list.:
    - "Hello, world! My name is \<name> and my favorite color is \<color>."


```python
## Loop through our fav_colors dict and print the above statement

```

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



```


```python
## What does the value for James look like now?

```


```python
## what is James's fav candy?

```


```python
## what is Adam's fav color?

```


```python
## now loop through nested dictionary and print
## my name is ___, my favorite color is ___, and my favorite candy is __

```

### Updating Dictionaries


```python
## james decided he hates purple. His new fav color is Blue. Update the dictioanry to reflect this

```


```python
## confirm that james' fav color is now Blue

```

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

    ## If the person's fav candy choclate:


    ## if the person's fav candy is fruity


    ## otherwise, the persons candy is exotic.


```

# BONUS: Object-Oriented-Programming 

- Our `fav_items` dictionary above is a perfect candidate for creating a class. 

- Our `Person` class will:
    - have a name
    - have a fav color
    - have a fav candy
    - will have a method called `.hello()` that will print out: "👋Hello, world! My name is ___, my favorite color is ____, and my favorite candy is ___


```python


    
```


```python
# now, create a new list called people_list 

# loop through our fav_dict and create a new Person for each person in fav_dict


    ## Maken sure to save the person to your people_list

```


```python
## take a look at People list to confirm there are 4 people

```


```python
## Loop through our list of people and run the .hello method


```


```python

```
