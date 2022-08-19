# Unit 1: A hardware store 



## Criteria A: Planning


## Criteria C: Development

### Usability

1. watch the video on Norman Doors,
1. Here write a summary
1. define all important terms

### Program to create a Menu

A small description
```.py
items = [("RAM", 10), ("CPU", 15)]


for c, item in enumerate(items):
  print("{}. {} ..... {} USD".format(c+1, item[0], item[1]))

# print("1. RAM ...... 30 USD")
# print("2. CPU ...... 10 USD")

option = input("Enter the part your want [1-2]")

# Check that the user entered a valid option,
# give at least tree trials
# Get the quantity
# show the total 

```
