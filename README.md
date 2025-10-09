# Object Oriented Programming Lab - Bookstore ✅ COMPLETED

This project demonstrates Object-Oriented Programming concepts in Python by implementing two classes that model items in a bookstore. The implementation includes proper encapsulation, validation, and method design following Python best practices.

## The Scenario

This project features two fully implemented classes for modeling a bookstore:
1. **Book Class** - Represents books with title and page count validation
2. **Coffee Class** - Represents coffee products with size validation and tipping functionality

Both classes demonstrate key OOP concepts including constructors, properties, validation, and methods.t Oriented Programming Lab - Bookstore 

This scenario should encompass all of the topics provided in the module. Now that you’ve delved into creating a new class in Python it is now time to practice this concept.

## The Scenario

You are tasked with building two different classes to aid with representing and modeling a bookstore. First will be a book object to allow for reading an online book and the second will be a coffee object as another object carried by the store. Both objects will have several attributes and functions to be called. 

## Quick Start

To use the implemented classes:

```python
# Import the classes
from lib.book import Book
from lib.coffee import Coffee

# Create and use a book
book = Book("Python Programming", 350)
book.turn_page()

# Create and use a coffee
coffee = Coffee("Large", 3.50)
coffee.tip()
```

Run the tests to verify everything works:
```bash
pytest lib/testing/ -v
```

## Tools & Resources

* [GitHub Repo](https://github.com/learn-co-curriculum/python-oop1-lab)
* [Python Classes](https://docs.python.org/3/tutorial/classes.html)

## Instructions

### Set Up

Before we begin coding, let's complete the initial setup for this lesson: 

* Part 1: Fork and Clone- For this lesson, you will need the previously linked GitHub Repo:
  * Go to the provided GitHub repository link.
  * Fork the repository to your GitHub account.
  * Clone the forked repository to your local machine.
* Part 2: Open and Run File
  * Open the project in VSCode.
  * Run `pipenv install` to install all necessary dependencies.
  * Run `pipenv shell` to enter the virtual environment.

This lab is test-driven. You will write your code in `lib/book.py` and
`lib/coffee.py`. Run the tests and work your way through the test errors one by
one until you get everything passing.

You're also encouraged to look at the test files to see what the tests are
expecting to be able to do with your classes. These tests won't force you to
use everything that you've learned in this module- feel free to add any
features that might be useful!

Note that there are separate test files for the two classes inside the `testing`
folder. If you'd like to run the tests separately for the two classes, you can
specify which test file to run:

```console
$ pytest -x testing/book_test.py
```

or:

```console
$ pytest -x testing/coffee_test.py
```

Remember that the optional `-x` flag makes your tests stop after the first
failure - this setting is ideal for test-driven development!

### Task 1: Define the Problem

Build a model for a book and a coffee
<br />
As a user, one should be able to:
* Build a book object
* Build a coffee object
* Call to turn a book page
* Call to tip for the coffee

### Task 2: Determine the Design

Book
* Attributes:
  * title
  * page_Count
* Methods:
  * turn_page()
Coffee
* Attributes:
  * size
  * price
* Methods:
  * tip()

### Task 3: Develop, Test, and Refine the Code

#### Step 1: Feature Branch and Book Class

* Create Feature Branch

* Create Book class:
  * __init__:
    * title
      * Require user to input
    * page_count
      * Require user to input
* Properties:
  * page_count:
    * Ensure it is an integer
    * if not print “page_count must be an integer”
* Methods:
  * turn_page():
    * Will print “Flipping the page...wow, you read fast!”

#### Step 2: Create Coffee Class & Push Feature Branch and Merge

* __init__:
  * size
    * Require user to input
  * price
    * Require user to input
* Properties:
  * Size
    * Ensure size is either Small, Medium, or Large
    * If not print “size must be Small, Medium, or Large”
* Methods:
  * tip():
    * Will print “This coffee is great, here’s a tip!”
    * Will increase price by 1 

#### Step 3: Push Feature Branch and Merge

* Push feature branch and open a PR on GitHub
* Merge to main

### Task 4: Document and Maintain

## ✅ Implementation Complete

Both the Book and Coffee classes have been successfully implemented and all tests are passing!

### Book Class Features

The `Book` class in `lib/book.py` provides:

**Attributes:**
- `title` - The title of the book
- `page_count` - Number of pages in the book (validated as integer)

**Methods:**
- `turn_page()` - Prints "Flipping the page...wow, you read fast!"

**Usage Example:**
```python
from book import Book

# Create a new book
my_book = Book("The Great Gatsby", 180)
print(f"Title: {my_book.title}")
print(f"Pages: {my_book.page_count}")

# Turn a page
my_book.turn_page()  # Output: "Flipping the page...wow, you read fast!"

# Validation works
my_book.page_count = "invalid"  # Output: "page_count must be an integer"
```

### Coffee Class Features

The `Coffee` class in `lib/coffee.py` provides:

**Attributes:**
- `size` - Size of the coffee (must be "Small", "Medium", or "Large")
- `price` - Price of the coffee

**Methods:**
- `tip()` - Adds $1 to the price and prints appreciation message

**Usage Example:**
```python
from coffee import Coffee

# Create a new coffee
my_coffee = Coffee(size="Medium", price=2.50)
print(f"Size: {my_coffee.size}")
print(f"Price: ${my_coffee.price}")

# Add a tip
my_coffee.tip()  # Output: "This coffee is great, here's a tip!"
print(f"New price: ${my_coffee.price}")  # Price increased by $1

# Validation works
my_coffee.size = "Extra Large"  # Output: "size must be Small, Medium, or Large"
```

### Test Results

All 7 tests pass successfully:
- ✅ Book initialization with title and page_count
- ✅ Book page_count integer validation
- ✅ Book turn_page() functionality
- ✅ Coffee initialization with size and price
- ✅ Coffee size validation
- ✅ Coffee tip() message output
- ✅ Coffee tip() price increment

Best Practice documentation steps:
* ✅ Add comments to code to explain purpose and logic. This clarifies intent / functionality of code to other developers
* ✅ Add screenshot of completed work included in Markdown in README.
* ✅ Update README text to reflect the functionality of the application following https://makeareadme.com.
* Delete any stale branches on GitHub
* Remove unnecessary/commented out code
* If needed, update git ignore to remove sensitive data 

## Save your work and push to GitHub

Before you submit your solution, you need to save your progress with git.
1. Add your changes to the staging area by executing git add .
2. Create a commit by executing git commit -m "Your commit message"
3. Push your commits to GitHub by executing git push origin main or git push origin master , depending on the name of your branch (use git branch to check on which branch you are).

## Submission and Grading Criteria

1. Use the rubric in Canvas as a guide for how this lab is graded.
2. Your submission will be automatically scored in CodeGrade, using the most recent commit. Remember to make sure you have pushed your commit to GitHub before submitting your assignment. 
3. You can review your submission in CodeGrade and see your final score in your Canvas gradebook.
4. When you are ready to submit, click the ***Load Lab: Object Oriented Programming (OOP)- Part 1- Bookstore*** button in Canvas to launch CodeGrade.
  * Click on + Create Submission. Connect your repository for this lab.
  * For additional information on submitting assignments in CodeGrade: [Getting Started in Canvas](https://help.codegrade.com/for-students/getting-started/getting-started-in-canvas)

