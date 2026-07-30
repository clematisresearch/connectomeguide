---
title: Programming Guide
authors:
  - name:
      given: Hannah
      family: Perez
---

# Introduction

## Welcome

Welcome to the programming guide! Whether you have never written a single line of code or have experimented with programming before, this guide is designed to help you develop the practical skills needed for scientific research.

Everyone starts from a different place. Some students have taken computer science courses, while others may have only used software such as Excel. Many students beginning scientific research have little or no programming experience, and that's completely normal. This guide is written especially for those who are new to programming, so don't feel intimidated if the code initially looks unfamiliar. Every experienced programmer started exactly the same way: by not understanding what they were looking at.

Programming is simply another language. Like learning any new language, it can seem confusing at first, but with practice the pieces gradually begin to fit together.

---

## There Are Many Ways to Learn

Today there are countless resources for learning Python, as well as other programming languages such as **R**, **MATLAB**, and **Bash**. You can find online courses, YouTube videos, textbooks, interactive websites, and university lectures. While having so many resources is a great advantage, it can also feel overwhelming.

You may find yourself wondering:

> *"Where do I even begin?"*

The truth is that there is no single "correct" learning path. Different people learn in different ways, and many approaches can lead to the same destination.

It is always valuable to study a programming language in depth. However, many beginners fall into the trap of believing they must first master all of Python before they can begin doing scientific research from analyzing complex biological datasets to producing pretty figures. 

Fortunately, that simply isn't true.

---

## Learn by Applying

One of the most effective ways to learn programming is to **use it while learning it**.

Many beginners experience something like this:

* Learn about programming concept A (e.g., variables).
* Learn about programming concept B (e.g., loops).
* Learn about programming concept C (e.g., functions).
* Complete a few small exercises.
* Then suddenly face a real neuroscience dataset and wonder:

> *"I know the syntax, but I have no idea how to solve this problem."*

This happens because learning programming syntax alone is different from learning how to **use programming to solve problems**.

Instead, try to learn programming and neuroscience together.

For example, after learning about variables, immediately use them to store participant ages. After learning loops, use them to process multiple MRI scans. After learning functions, write one that calculates a simple statistic from your data.

By repeatedly applying basic programming concepts to real research questions, you will:

* understand programming concepts more deeply,
* develop intuition for solving problems,
* become more confident writing your own code,
* and most importantly, stay motivated because you're working on questions that actually interest you.

This creates a positive learning cycle:

> **Learn a concept → Apply it to research → Encounter a new problem → Learn another concept → Apply it again**

This guide is built around that philosophy.

---

## Our Goal

Although there are many different ways to become a programmer, there are several fundamental ideas that every programmer/scientist should understand.

This guide suggests one possible learning path through those ideas.

It is **not** the only path.

You may see different coding styles, different libraries, or different solutions elsewhere online. That's perfectly normal. Programming rarely has only one correct answer.

Rather than memorizing every command, we hope you develop an understanding of **why** the code works and **how** to adapt it to new problems.

Those skills will stay with you long after you forget individual pieces of syntax.

---

## Programming in the Age of Generative AI

Generative AI tools such as ChatGPT have dramatically lowered the barrier to learning programming. They can explain concepts, help debug errors, generate example code, and answer questions almost instantly.

When used responsibly, they can be excellent learning partners.

However, there is an important difference between **getting an answer** and **understanding the answer**.

Imagine asking ChatGPT:

> "What is 3 + 5?"

It will correctly respond:

> **8**

While that solves the immediate problem, it doesn't teach you *why* 3 + 5 equals 8.

Now imagine asking:

> "Can you explain why 3 + 5 equals 8 using a simple example?"

Now you're learning the underlying idea of addition.

That understanding becomes the foundation for multiplication, algebra, calculus, statistics, and many other subjects.

Programming works exactly the same way.

Instead of only asking AI to write code for you, try asking questions like:

* Why does this function work?
* Why do we use a loop here?
* What does this error message mean?
* Can you explain this code line by line?
* Can you show me a simpler example?

By focusing on understanding rather than copying, you'll become a much stronger programmer over time. 

Throughout this guide, we encourage you to use AI as a **teacher**, not simply as a code generator.

---

# Outline of This Guide

The rest of this programming guide is organized into several short tutorials that introduce the essential tools you'll need for scientific research.

## 1. Why Learn Python?

We'll begin by answering a simple question:

> **Why use Python at all?**

Why not simply use Excel?

Or a graphical statistics program?

We'll use simple everyday examples to illustrate how programming becomes invaluable once your data become larger, more complicated, or require repeated analyses.

By the end of this section, you'll understand why Python has become one of the most widely used programming languages in science.

---

## 2. Programming Fundamentals

Before working with neuroscience data, we'll build a strong foundation by learning the core concepts that appear in almost every Python program.

Topics include:

* Installing Python
* Setting up Visual Studio Code
* Using Jupyter/Python notebooks
* Variables
* Data types
* Conditional statements (`if`)
* Loops (`for`, `while`)
* Functions
* Basic data structures
* Working with folders and directories
* Importing files

These concepts may seem simple at first, but they form the building blocks of nearly every analysis you'll write.

---

## 3. Learning How Code Works

Writing new code is just as important as adapting other people's code or troubleshooting your own code.

In this section, you'll learn practical techniques for understanding unfamiliar code and troubleshooting when something goes wrong.

For example, if a function contains dozens of lines of code, you don't always need to understand everything at once. You can execute it piece by piece, inspect intermediate variables, and gradually build your understanding.

Similarly, if a loop processes hundreds of participants, you can temporarily replace:

```python
for participant in participants:
```

with a single participant:

```python
participant = participants[0]
```

This allows you to follow the code step by step before scaling up to the full dataset.

These simple debugging strategies are techniques that experienced programmers use every day.

---

## 4. Managing Your Programming Environment

Scientific projects often depend on many external packages.

We'll introduce:

* Conda
* Virtual environments
* Installing packages
* Managing package versions

Learning these tools early will save countless hours later when working on larger research projects.

---

## 5. Essential Python Libraries for Data Science

Finally, we'll introduce several of the most commonly used libraries in data analysis for scientific research.

These include:

* **NumPy** for working with arrays and matrices.
* **Pandas** for organizing and manipulating tabular data.
* **Matplotlib** for creating figures and visualizations.

We'll then bring everything together in a small example project that combines many of the concepts introduced throughout the guide, including:

* importing data,
* defining variables,
* writing functions,
* using loops,
* organizing data,
* performing simple analyses,
* and visualizing the results with a figure.

By this point, you'll have seen how the individual pieces fit together into a complete programming workflow similar to what you'll encounter in real neuroscience research.

---

# Final Thoughts

Learning to program is not about memorizing every command or becoming an expert overnight.

It is about developing a way of thinking: breaking large problems into smaller ones, testing ideas, learning from mistakes, and gradually building confidence.

You will encounter errors. Every programmer does.

You may sometimes spend an hour looking for an incorrect logic, a missing parenthesis or a typo in the variable name.

That is not a sign that you are bad at programming. It is simply part of programming.

Be patient with yourself, stay curious, and keep experimenting. Every concept you learn becomes another tool that allows you to ask bigger scientific questions and explore increasingly complex datasets.

We hope this guide gives you not only the technical skills needed for Connectome2026, but also the confidence to continue learning long after you've finished these tutorials.

