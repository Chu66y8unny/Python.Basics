I **floundered** for a long time trying to teach myself. I **slogged** through
dozens of incomplete online tutorials. I **snoozed** through hours of boring
screencasts. I gave up on countless **crufty** books from big-time
publishers.

# Forward

Conversely, you can build real apps with C++, yet there is no gentle 
**on-ramp**.

- <realpython.com>
- <talkpython.fm>
- <insights.stackoverflow.com/trends>
- <https://insights.stackoverflow.com/survey/2018/>

# Chapter 1 Introduction

If so, this book is for you - whether you're a complete beginner or already 
**dabbled** in Python or other languages before.

Not only do you spend most of your time **cramming** things into your head 
you'll never use, it also isn't any fun!

This book is built on the 80/20 principle.

<https://realpython.com/python-basics/>

Good luck on your Python journey, we're **rooting** for you!

<https://realpython.com/python-basics/resources/>

The quick brown Python **slithers** over the lazy hog.

# Chapter 2 Setting Up Python

IDLE - Integrated Development and Learning Environment

<https://realpython.com/installing-python/>

To find out what version(s) you have,

```shell
$ python --version
$ python3 --version
```

You can determine your local Ubuntu version by running the following command:

```shell
$ lsb_release -a
```

Ubuntu 18.04+

```shell
$ sudo apt-get update
$ sudo apt-get install python3.8 idle-python3.8
```

Ubuntu 17 and lower: Python 3.8 is not in the Universal repository. You need to 
get it from a Personal Package Archive (PPA).

```shell
$ sudo apt-get-repository ppa:deadsnakes/ppa
$ sudo apt-get update
$ sudo apt-get install python3.8 idle-python3.8
```

Open IDLE

```shell
$ idle-python3.8
$ idle3
```

# Chapter 3 Your First Python Program

Read-Evaluate-Print Loop, or REPL

A **rite** of passage for every programmer is writing their first "Hello,
world" program that prints the phrase "Hello, world" on the screen.

In Python, **variables** are names that can be assigned a value and used
to reference that value throughout your code.

1. Variables keep values accessible
2. Variables give values context

[Unicode](https://en.wikipedia.org/wiki/Unicode)

[official Python documentation on Unicode support](https://docs.python.org/3/howto/unicode.html#python-s-unicode-support)

The juxtaposition of lower-case and upper-case letters look like **humps** on a 
camel.

In Python, however, it is more common to write variable names in
snake case like `num_students` and `list_of_names`. Every letter is lowercase,
and each word is separated by an underscore.

[PEP8](https://pep8.org/)

You will also learn some conventions for formatting comments, as well as some 
**pet peeves** regarding their over-use.

According to PEP 8, comments should always be written in complete sentences 
with a single space between the `#` and the first word of the comment:

```python
# This comment is formatted to PEP 8.
```

For in-line comments, PEP 8 recommends at least two spaces between the code and 
the `#` symbol:

```python
phrase = "Hello, world"  # This comment is PEP 8 compliant.
```

In general, PEP 8 recommends that comments be used sparingly. Use comments only 
when they add value to your code by making it easier to understand *why* 
something is done a certain way. Comments that describe *what* something does 
can often be avoided by using more descriptive variable names.

- [11 Beginner Tips for Learning Python Programming](https://realpython.com/python-beginner-tips/)
- [Writing Comments in Python (Guide)](https://realpython.com/python-comments-guide/)
- [Recommended resources on realpython.com](https://realpython.com/python-basics/resources/#recommended-resources)

# Chapter 4 Strings and String Methods

- `str`
- `type()`
- `len()`

The PEP 8 style guide recommends that each line of Python code contain no more 
than 79 characters - including spaces. <https://pep8.org/#maximum-line-length>

There are a couple of ways to tackle this. One way is to break the string
up across multiple lines and put a backslash (`\`) at the end of all but the
last line.


```python
paragraph = "This planet has - or rather had - a problem, which was \
this: most of the people living on it were unhappy for pretty much \
of the time. Many solutions were suggested for this problem, but \
most of these were largely concerned with the movements of small \
green pieces of paper, which is odd because on the whole it wasn't \
the small green pieces of paper that were unhappy."
```

Multiline strings can also be created using triple quotes as delimiters
(`"""` or `'''`).

```python
paragraph = """This planet has - or rather had - a problem, which was
this: most of the people living on it were unhappy for pretty much
of the time. Many solutions were suggested for this problem, but
most of these were largely concerned with the movements of small
green pieces of paper, which is odd because on the whole it wasn't
the small green pieces of paper that were unhappy."""
```

Triple-quoted strings preserve whitespace.

concatenation by `+`

If you try to access an index beyond the end of a string, Python raises
an `IndexError`. Strings also support negative indices. Just like positive 
indices, Python raises an `IndexError` if you try to access a negative index 
less than the index of the first character in the string.

If you need more than just the first few letters of a string, getting each 
character individually and concatenating them together is clumsy and 
**long-winded**.

slice

- If you omit the first index in a slice, Python assumes you want to start at 
  index 0
- Similarly, if you omit the second index in the slice, Python assumes you want 
  to return the substring that begins with the character whose index is the 
  first number in the slice and ends with the last character in the string
- If you omit both the first and second numbers in a slice, you get a string 
  that starts with the character with index 0 and ends with the last character. 
  In other words, omitting both numbers in a slice returns the entire string

It's important to note that, unlike string indexing, Python won't raise an 
`IndexError` when you try to slice between boundaries before or after the 
beginning and ending boundaries of a string.

You can use negative numbers in slices.

```python
flavor = 'apple pie'
flavor[-9:-6]  # 'app'
```

Notice, however, that the right-most boundary does not have a negative index. 
The logical choice for that boundary would seem to be the number 0, but that 
doesn't work. If you need to include the final character of a string in your 
slice, you can omit the second number.

```python
flavor[-9:]  # 'apple pie'
```

Strings are **immutable**, which means that you can't change them once you've 
created them.

```python
"Jean-luc Picard".lower()
loud_voice = "Can you hear me yet?"
loud_voice.upper()
```

- `.rstrip()`
- `.lstrip()`
- `.strip()`
- `.startswith()`
- `.endswith()`

IDLE has autocomplete feature.

`input("Hey, what's up")`

When the `*` operator is used with a sequence on either the left or the right 
side, it always expects an integer on the other side.

A sequence is any Python object that supports accessing elements by index. 
Strings are sequences.

If any one of the objects on either side of `+` is a string, Python tries to 
perform string concatenation.

- `int()`
- `float()`
- `str()`

```python
name = 'Zaphod"
heads = 2
arms = 3
f"{name} has {heads} heads and {arms} arms"
"{} has {} heads and {} arms".format(name, heads, arms)
```

f-strings are only available in Python version 3.6 and above. In earlier 
versions of Python, the `.format()` method can be used to get the same results.

<https://realpython.com/python-f-strings/>

`%` operator formating: <https://docs.python.org/3/library/stdtypes.html#old-string-formatting>

`.find()` returns the index of the first occurrence of the string you pass to 
it. If `.find()` doesn't find the desired substring, it will return -1 instead.

```python
my_story = "I'm telling you the truth; nothing but the truth!"
my_story.replace("the truth", "lies")
```

<https://en.wikipedia.org/wiki/Leet>

## Additional Resources

- Python String Formatting Best Practices <https://realpython.com/python-string-formatting/>
- Splitting, Concatenating, and Joining Strings in Python <https://realpython.com/python-string-split-concatenate-join/>
- Recommended resources on realpython.com <https://realpython.com/python-basics/resources/#recommended-resources>

# Chapter 5 Numbers and Math
