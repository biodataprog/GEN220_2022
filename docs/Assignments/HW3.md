# Homework 3

The homework template in [github classroom](https://classroom.github.com/a/J8gwkyZo)

Lists, combinations, and permutations

Consider the experiment you want to establish comparing the interactions between pairs of organisms. This could be plants or microbes where you want to establish these in common growing wells
or you could imagine this is a genotype of a plant/animal and a combination of a treatment (pesticide, fertilizer etc).

Consider the simple case of a set of 10 individuals you can label A-J.
You want to first make a list of all the unique pairwise combinations. This means AB is the same as BA so you only want to see it once.

For a set of 5 individuals A-E the number of pairwise combinations is AB,AC,AD,AE, BC,BD,BE, CD,CE. If we consider a pairing of the same organism as a control we need to add in
AA, BB, CC, DD, EE. So the total count is 14.

```
---------------------
| AB | AC | AD | AE |
| ------------------|
| BC | BD | BE | CD |
| ------------------|
| CE | AA | BB | CC |
|-------------------|
| DD | EE |    |    |
|-------------------|
```
1. Write a program to generate the set of all pairwise combinations given a single input list of individuals.

2. Print out this list in a grid. Make the number of columns that are printed a variable. You can keep it simple and just print out a comma delimited. for example if the number of columns is 3 this will suffice.
If you have your program produce this result, make sure the name of the file is ".csv" and save it into your github for the project it will show up as a nicely formatted table on the web.
```
,Col1,Col2,Col3
Row1,AA,AB,AC
Row2,AD,AE,BC
....
````

3. Write a second program or option to your program that randomizes the list so the output order of the sample pairs is shuffled

![Seed Trays](https://ag.umass.edu/sites/ag.umass.edu/files/fact-sheets/images/openseedtrays.jpg)
