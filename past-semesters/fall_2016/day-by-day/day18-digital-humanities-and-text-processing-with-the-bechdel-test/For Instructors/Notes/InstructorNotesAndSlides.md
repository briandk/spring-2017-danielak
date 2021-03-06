There's a Very Simple Test Most Movies Fail
===========================================

The Bechdel Test (named for its inventor, Alison Bechdel)
---------------------------------------------------------

Does the movie have

1.  At least one scene
2.  Where at least two women are talking to each other
3.  About something other than a man?

It's such a low bar, and yet...
===============================

Movies that fail the Bechdel Test
---------------------------------

-   *Deadpool*
-   *The Magnificent Seven (2016)*
-   *Star Trek: Beyond*

Imagine if we rephrased the test
--------------------------------

Does the movie have:

1.  At least one scene
2.  Where at least two **men** are talking to each other
3.  About something other than a **woman**?

Collectively *Deadpool*, *The Magnificent Seven (2016)*, and *Star Trek:
Beyond* have **dozens** of scenes that pass this modified male-centric
test. But among those movies, not one passes the Bechdel Test

The question helps us think about the roles and characters available to women.
==============================================================================

Today we'll try using computation to administer the Bechdel Test
================================================================

Learning Goals
--------------

You will:

-   Transform the Bechdel Test from plain English into a precise
    question that a program can answer
-   Use component program pieces to assemble such a program that answers
    that question
-   Reflect on the strengths and limitations of your approach

Why are these goals important?
------------------------------

-   Turning ideas into questions that programs can answer is at the core
    of all computational science.
-   Programming is like building with Legos.
    -   We get certain basic pieces for free because someone else wrote
        them (`pandas`, `re` for pattern-matching, `matplotlib`
        for graphics)
    -   We arrange and connect those pieces in new ways to create our
        programs
    -   Our programs can become basic pieces *someone else* can use to
        build in even bigger new ways
-   You will almost always be working by composing more basic pieces
-   Sometimes data is dirty

We're giving you some raw materials
-----------------------------------

You'll get a collection of functions and other code snippets, like this:

    def extract_character_name(dialogue_element):
        """
        Get a character's name from a dialogue_element dictionary
        """
        if dialogue_element is not None:
            return dialogue_element["character_name"]
        else:
            return None

They *should* all do what they say they do. Putting them together is up
to you.

You mean I can copy-paste code?
-------------------------------

Yes. When you think about it, any time you do this:

    import pandas as pd

you're copying and pasting the entire `pandas` library code into your
project. Then, you use pieces like `pandas.read_csv` and
`pandas.DataFrame.mean()` as building blocks for your analysis.

Let's get started!
------------------

Pay attention to the *inputs* (stuff in parentheses after a function
name) and the *outputs* (what a function returns). That should help you
in composing pieces.
