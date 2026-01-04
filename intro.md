---
kernelspec:
  name: python3
  display_name: 'Python 3'
---

Rocket Propulsion notes
=======================

This is a book of supplementary notes for the AAE 462/562: Rocket Propulsion course taught by 
[Prof. Kyle Niemeyer](https://niemeyer-research-group.github.io) at Oregon State University.

The primary reference textbook for this course is *Rocket Propulsion Elements*, 
by George P. Sutton & Oscar Biblarz, 9th edition, Wiley {cite:p}`sutton2016rocket`.
Additional references will also be used, including:
- *Fundamentals of Gas Dynamics* by Zucker & Biblarz {cite:p}`ZuckerBiblarz`
- *Rocket and Spacecraft Propulsion: Principles, Practice and New Developments* by Turner {cite:p}`TurnerPropulsion`
- *Mechanics and Thermodynamics of Propulsion* by Hill & Peterson {cite:p}`HillPeterson`
- *Rocket Propulsion* by Heister, Anderson, Pourpoint, & Cassady {cite:p}`Heister2019`

```{image} ./images/logo/logo.jpg
:alt: Apollo 11 Saturn V launch vehicle
:width: 300px
:align: center
```

The logo for these notes shows the Apollo 11 Saturn V launch vehicle, lifting off
on 16 July 1969, carrying Astronauts Neil Armstrong, Michael Collins, and Edwin Aldrin.
It comes from the [Project Apollo Image Gallery](http://www.apolloarchive.com/apollo_gallery.html),
and is in the public domain. It is hosted on Wikimedia Commons: 
<https://commons.wikimedia.org/wiki/File:Apollo_11_Saturn_V_lifting_off_on_July_16,_1969.jpg>.

## How to use this book

First, you may need to set up your Python computing environment:
- Mac
- Windows
- Linux

The book is filled with examples of Python code, sometimes with output. Here is an example:

```{code-cell} python
def add(num1, num2):
    return (num1 + num2)

print(add(6, 7))

hello = "hello"
there = "there"
print(f"{hello}, {there}!")
print()
```

The output above was not pasted in manually, but inserted by the code cell above it.
If you hover over that code cell, you will see an icon in the upper right corner 
that allows you to copy that code to your clipboard. 
You will probably do this kind of thing a lot as you work though this book.
In particular, you may find function definitions throughout to be very useful and 
can copy those into your own files/notebooks.

If you need a primer on using Python, NumPy, and SciPy to solve problems, 
start with the [](./solving-tips.ipynb) module.
Otherwise, jump straight into the [](./fundamentals/thrust-rocket-equation.ipynb) module,
or use the Table of Contents on the left to find the material you need.

## Reporting issues

If you see a problem or find a typo, you can file an [issue](https://github.com/kyleniemeyer/rocket-propulsion-book/issues) via GitHub.
More detailed instructions on this and contributing are in the [](./contributing.md) guide.

## Supporting the author

This resource is provided free and under a permissible open license.
If you find it useful, please consider making [a small donation](https://buymeacoffee.com/kyleniemeyer) to show your support! 
(Students at Oregon State University are excepted from this request, 
because I don’t like the idea of pressuring my own students to pay me. 
After all, I primarily developed this material to be a resource 
for students in my AAE 462/562 Rocket Propulsion class.)

