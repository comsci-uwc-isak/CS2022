# Unit 1: An Electronic Hardware Store
![](OnlineGroceries.gif)

## Criteria A: Planning 

### Context of the problem
There is a hardware store in Karuizawa. This store is quite old, Like 1000 years old. The owner, Mr Sakamoto, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application tha replaces the accounting book. Mr Sakamoto got a new Mac PC from his nephew, and we would like to use it.

### Justification of the solution
***Here we will write the design statement: what we will do, how, by when***
we want to crate a text based application that runs on a computer, which provides the functionality for the hardware store. The app should provide action such as record of purchases, categorization of items, record of inventory, calculation of totals, billing. We will develop this application using Python. We will use Python because it is the software we are using in class at the moment. In comparison to C++ or C, Python has a lean and simple programming syntax. In addition Python has become the most popular programming language over the last years [1]. Similarly, Python has a large repository of libraries and documentation. 

T.E.L.O.S study: 

[1] MLA citation for the data supporting that Python is the most popular programming language

## Criteria for Success
1. Provides clear feedback to the user (Usability)
1. **There are no bugs in the application**
1. The application should allow to calcualte the total and billing
1. Secure application: importan information is encrypted

## Criteria B: Design

### System diagram

### Flow diagram

### Test Plan
|Test No | Procedure | Inputs | Expected Output | Success Criteria |
|--------|-----------|--------|-----------------|------------------|
|    1   | Secure application: Critical information is kept in an encryted file.  | an uncrypted database file | encrypted file | 4|

### Record of Tasks
| Task No | Planned Action                                                                                           | Planned Outcome                       | Time Estimated | Target Completion date | Criterion |
|---------|----------------------------------------------------------------------------------------------------------|---------------------------------------|----------------|------------------------|-----------|
| 1       | Planning: Discuss the context of the situation. ( Ideally this is the first interview with your client)  | Write the context of the problem      | 15 min         | Sep 11th               | A         |
| 2       | Development: Coded the a text-based menu system for some parts in the hardware store                     | A working program that shows the menu | 80 min         | Sep 18th               | D         |
|         |                                                                                                          |                                       |                |                        |           |

## Criteria C: Development

First test of text based menu:

```.py
welcome_msg = "Welcome to Sakamoto's store"

print(welcome_msg)
print("This is the menu")
print("=" * 20)
```

The following code is a simulation of a dice. It uses the Random Library.
```.py
#3- Repeat process 1000 times and record the counts for each face
import random
counts = [0, 0, 0, 0, 0, 0]
num_trial = 20000
for trial in range(num_trial):
    number = random.randint(0,60)
    if number < 10:
        counts[0] += 1
    elif 9 < number < 20:
        counts[1] += 1
    elif 19 < number < 30:
        counts[2] += 1
    elif 29 < number < 40:
        counts[3] += 1
    elif 39 < number < 50:
        counts[4] += 1
    elif 49 < number < 60:
        counts[5] += 1
for index, c in enumerate(counts):
    error = c - num_trial/6
    print("Number of {}s: {}, expected {}, error {}".format(index+1,c, num_trial/6, error))


```

Program to calculate the taxes: The program below uses pattern recognition to simplify the calculation of the taxes according to the table below

Table 1. Calculation of taxes based on the total
| Rate | Bill total          |
|------|---------------------|
| 5%   | >1000 BTC           |
| 10%  | 750 < total <= 1000 |
| 15%  | 500 < total <= 750  |
| 20%  | 250 < total <= 500  |
| 25%  | 0 < total <= 250    |
```.py
for n in [0,1,2,3]:
    if 250*n < total <= 250*n + 250:
        tax = 0.25 - 0.05 * n
    if total > 1000:
        tax = 0.05

```

## Cirteria D: Functionality
 This is a video. 

## Criteria E: Evaluation
