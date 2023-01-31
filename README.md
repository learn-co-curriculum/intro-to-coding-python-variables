# What are Variables?

## Learning Goals

- Explain a variable.
- Declare variables in Python.
- Access variables in Python.

## Introduction

Variables are a way to make the computer remember values. A variable is a label
to which a value can be assigned.

Variables allow programmers to give meaning to values and use those values
throughout the program easily. For example, the number `238900` doesn’t mean
anything but if we label it as “the distance to the Moon from the Earth” it’s
easier to reference. We don’t necessarily have to remember the exact value as we
can look it up using the phrase “distance to the moon from the Earth”.

Here’s how we would use a variable in Python:

```python
distance_from_moon_to_earth = 238_900
print(distance_from_moon_to_earth)
```

We can use `_` (underscore) to make big numbers easier to read in Python. Notice
that we’re also using the `_` to separate words in the variable name.

Output:

```python
238900
```

## Variable Naming Conventions

It is important to follow consistent guidelines when naming variables. The
projects you work on will likely have their own guidelines. For example, here’s
[Google’s Python style guide](https://google.github.io/styleguide/pyguide.html#s3.16-naming).

The following are common variable naming conventions that are used across the
industry:

- Variable names can only contain letters, numbers, and underscores (`_`).
- They can only start with a letter or an underscore (`greeting1` and
  `_greeting1` are valid but `1greeting` is not).
- Variables are case-sensitive (`greeting` and `Greeting` are separate
  variables).
- Multiple words must be separated using `_` (`my_birthday`,
  `number_of_people`). This convention is called
  [snake_case](https://en.wikipedia.org/wiki/Snake_case).
- Variable names must be meaningful (`max_speed` instead of `m`).

## Visualizing Computer Memory

Whenever we ask the computer to represent a string, number, or boolean it
creates the representation in its memory. You can think of the computer memory
as a giant container that can store information for the duration of a program’s
execution.

At the start of program execution, the computer’s memory is empty. We can
visualize it like this:

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/01.png)

Now let’s run some code and visualize how the memory will change during
execution:

```python
print("I love cats!")
print(1)
print(5.5)
print(True)
```

For each of the values, a representation will be created in the memory during
execution.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/02.png)

Once the program completes execution, the memory will be empty again.

Note that if we had two `print(1)` statements, there would still be only a
single representation of the integer `1`. This is the case for strings and
booleans too.

## Variable Declaration and Assignment

Let’s look at how to create a variable again:

```python
cat_name = 'Fifi'
```

There are 3 parts to this line:

- `cat_name` is the variable name.
- `=` is an assignment operator.
- `'Fifi'` is an expression that produces the value `Fifi` of type `str`.

So this is the general structure:

```python
variable_name = expression
```

- The right side of the `=` operator is evaluated first.
- The value produced by the expression evaluation is then assigned to the
  variable name or label.

The line `cat_name = 'Fifi'` is usually verbalized as “declare a variable called
cat_name and assign the value ‘Fifi’ to it”

### Visualizing Declaration and Assignment

We are going to visualize the following line:

```python
cat_name = 'Fifi'
```

First, the computer evaluates the expression which in this case produces the
string `'Fifi'` and stores it in the memory.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/03.png)

The computer would then declare the variable with the given name. Notice that
the string is in `''` while the variable name is not.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/04.png)

Finally, the computer makes the variable name point to the value, i.e., it
assigns the value to the variable label.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/05.png)

## Variable Access

We’ve seen how a computer declares variables and assigns values to them. Now we
will look at what happens when the computer accesses a variable.

Here’s the code we will be working with:

```python
cat_name = 'Fifi'
print(cat_name) # 'Fifi'
```

When a computer sees a variable label it checks its memory for the label. If the
label exists, the value that the label points to is used by the computer.

We can visualize this by checking the memory diagram and following the arrow
from the variable label (`cat_name`) to the value (`’Fifi’`).

## Variable Reassignment

Variable values can be changed during the execution of the program. For example:

```python
current_year = 2022
print(current_year) # 2022
current_year = 2023 # reassignment
print(current_year) # 2023
```

The first line will result in the following memory state:

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/06.png)

On the second line, the computer will look up the `current_year` label in its
memory and display the value `2022`.

On the third line, a few things happen:

- The computer creates the representation of `2023` in its memory (remember the
  right hand side of the `=` operator is evaluated first).
  ![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/07.png)
- The `current_year` label arrow is pointed to the `2023` representation.
  ![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/08.png)
- Since no variables are pointing to the `2022` value anymore, it gets removed
  from memory.
  ![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/what-are-variables/09.png)

On the 4th and final line, the computer checks its memory for the
`current_label` again but this time it’s pointing to a new value (`2023`).

As a reminder, this mental model works for strings and booleans too!

## Conclusion

Variables are one of the most convenient features of a programming language. We
will make use of them all the time!
