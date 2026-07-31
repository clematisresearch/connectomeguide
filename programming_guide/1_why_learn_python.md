---
title: "Why Learn Python?"
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

# Why Learn Python?

Before writing our first line of code, it's worth asking a simple question:

> **Why learn Python at all?**

After all, many analyses can already be done using Excel, SPSS, GraphPad Prism, or other software with graphical interfaces (GUIs). If those tools already exist, why spend time learning to program?

The short answer is:

> **Programming allows you to automate repetitive tasks, work with larger and more complex datasets, and build analyses that are reproducible.**

These advantages become increasingly important in neuroscience, where datasets can contain hundreds of participants, thousands of brain regions, and millions of measurements.

---

# A Simple Everyday Example

Imagine you have a folder containing **500 holiday photos**.

You decide that every photo should:

* be resized,
* have the brightness increased slightly,
* and be saved into a new folder.

There are two ways you could do this.

## Option 1: Do everything manually

Open the first photo.

Resize it.

Adjust the brightness.

Save it.

Repeat...

...499 more times.

Although each photo might only take 20 seconds, you've now spent several hours doing exactly the same task.

---

## Option 2: Write instructions once

Instead, imagine telling a computer:

> "For every photo in this folder, resize it, increase the brightness, and save the result."

Now the computer performs exactly the same steps for every image automatically.

You only wrote the instructions once.

This is one of the central ideas behind programming.

Rather than repeatedly performing a task yourself, you describe **how** to perform the task, and let the computer repeat it as many times as needed.

---

# What Is a Loop?

The previous example introduces one of the most common programming concepts:

> **A loop repeats the same set of instructions multiple times.**

In everyday life, you already use loops without realizing it.

Imagine you're a teacher handing out worksheets.

Instead of thinking:

* Give worksheet to Student 1.
* Give worksheet to Student 2.
* Give worksheet to Student 3.
* ...

You naturally think:

> **"For every student, hand them one worksheet."**

That is exactly how a computer thinks.

Instead of writing the same instructions hundreds of times, we write them once and ask the computer to repeat them.

In Python, this might eventually look something like:

```python
for student in classroom:
    give_worksheet(student)
```

Don't worry about the syntax yet. The important idea is that the computer is simply repeating the same instruction for every item in a collection.

---

# What Is a Function?

Another important programming idea is a **function**.

A function is simply a set of instructions that performs a specific task.

Think about making tea.

Every time you make a cup, you follow roughly the same sequence:

1. Boil water.
2. Add a teabag.
3. Pour the water.
4. Wait.
5. Remove the teabag.

Rather than thinking through every individual step each time, we can group them into a single task:

> "Make tea."

Programming works the same way.

Instead of rewriting the same code or sequence of instructions over and over, we place those instructions inside a function that can be reused whenever needed.

In Python, this might eventually look something like:

make_tea()

You don't need to worry about how this function is written just yet. The important idea is that make_tea() represents a collection of instructions that have been grouped together under a single name.

Later in this guide, you'll learn how to write your own functions for tasks such as loading data, analysing data, calculating statistics, or generating figures. 

---

# Why Not Just Use Excel?

Excel is an excellent tool for many tasks.

If you have a small spreadsheet with a few dozen rows, it may be the fastest and easiest option.

However, imagine you collect data from **200 participants**, and for each participant you need to:

* import their MRI data,
* calculate several measurements,
* create a figure,
* save the results,
* and repeat the process whenever new participants are added.

Doing this manually would be extremely time-consuming and prone to mistakes.

A Python program, however, can perform exactly the same sequence every time with only a single command.

This is known as **automation**.

---

# A Neuroscience Example

Suppose you're analysing MRI scans from **200 participants**.

For every participant, you need to:

* load the brain image,
* measure the volume of several brain regions,
* save those measurements,
* and create a figure showing the results.

The analysis pipeline is identical for every participant.

Rather than repeating these steps manually 200 times, you can write the analysis once and allow Python to repeat it automatically.

This is how automation could be very useful in neuroscience. Once the analysis has been written, the computer can perform the same set of steps consistently for every participant.


---

# Reproducibility Matters

Programming offers another major advantage:

**reproducibility**.

Imagine you analyse your data today.

Six months later, your supervisor asks:

> "Can you rerun the analysis after excluding five participants?"

If every step was performed manually in Excel, reproducing exactly what you did may be difficult.

If your entire analysis is written in Python, you simply run the program again.

Every calculation is repeated exactly the same way.

This makes your work easier to verify, easier to share with collaborators, and easier to extend in the future.

Reproducibility is one of the reasons programming has become central to modern scientific research.

---

# Python Is More Than Neuroscience

Although this guide focuses on neuroscience, Python is used in many different fields, including:

* data science
* machine learning
* artificial intelligence
* finance
* engineering
* astronomy
* genomics
* psychology
* web development
* automation

---

# You Don't Need to Memorize Everything

One concern many beginners have is:

> **"There are so many commands—how will I ever remember them all?"**

The answer is that you won't.

Experienced programmers regularly search documentation, read examples, and look up syntax they haven't used in a while.

What matters much more than memorizing commands is understanding the underlying ideas:

* variables store information,
* loops repeat instructions,
* functions organize reusable code,
* and programs combine these pieces to solve problems.

Once these concepts become familiar, learning new libraries and techniques becomes much easier.

---

# Further Reading

If you'd like another beginner-friendly introduction to why Python is so widely used, these resources are excellent:

* The Python Software Foundation's official tutorial: https://docs.python.org/3/tutorial/
* Harvard University's *CS50 Python* (free): https://cs50.harvard.edu/python/
* Automate the Boring Stuff with Python (free online book): https://automatetheboringstuff.com/
* The Carpentries (Programming for Data Science and Research): https://carpentries.org/

All four resources are widely used and freely available.

---

# Key Takeaways

By the end of this section, you should understand that programming is not about making tasks more complicated—it is about making repeated and complex tasks simpler.

Python allows us to:

* automate repetitive work,
* analyse large datasets,
* reduce human error,
* reproduce analyses reliably,
* organise code into reusable functions,
* repeat tasks efficiently using loops,
* and build workflows that scale from a handful of participants to thousands.

These ideas form the foundation of scientific programming. In the next section, we'll start learning the building blocks that make all of this possible.
