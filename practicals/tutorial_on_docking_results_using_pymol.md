---
title: Graphical analysis of ClusPro docking results using PyMol
authors:  Allegra Via 
based on: PyMol Getting Started Tutorial
minutes: 30
---

------------

> ## Learning Outcomes
> At the end of this tutorial, successful learners will be able to:
> * describe PyMol's basic features
> * upload a structure (e.g. a ClusPro model)
> * select one or more residues
> * calculate atomic distances
> 
> 
> ## Goal of this task
> The goal of this tutorial is to upload ClusPro models and identify best solutions through a visual study of different models. 
> Each model contains an MKK7-Gadd45B complex, therefore, you have to select each structure and use different colors to distinguish them. Then, you have to select interacting residues and see whether they are close enough to interact, by calculating distances. 
> From the biological background (tutorial on docking), you should be able to see whether a solution is potentially a good solution.
> You should also be able to see and comment the differences between different solutions.

------------

For materials (tutorials, commands, cheat sheet, etc) and community-run support for PyMol, you can browse the [PyMOL Wiki](https://pymolwiki.org/index.php/Main_Page) website. 

# Getting started
Download PyMol at [https://pymol.org](https://pymol.org), install and open it. 
When you open it (the first time), you will be asked to provide a licence file or use a free trial version for 30 days. 
A licence can be bought here: [PyMol licence](https://pymol.org/2/buy.html).

A licence for educational use only can be obtained.
It consists of a .lic file to save on your computer and upload to PyMol when you open the application.


## Opening a structure

Now open a structure. Choose 

```
File → Open 
```

from the menu and enter the first model you downloaded from ClusPro (e.g. model.000.00.pdb). The structure will appear in the graphics window.
Receptor and ligand structure will be listed in the panel on the right. You can use the buttons to work with them.

## Selections 
First we change name to receptor and ligand: 
<br>
```
select rec, rec.pdb
```

```
select lig, lig.000.00.pdb
```

Then we select the residues we used to create the restraints:

```
select rec_res, (resi 165+178+173) and rec
```

```
select lig_res, (resi 65+66+113) and lig
```


Once selections are created, you can use the right panel (where selections are listed) to play with them.



##Calculating atomic distances

You can type the following command:

```
wizard measurement
```

or select from the menu:

Wizard --> Measurement

Then you can click on the atoms of which you want to calculate the distance.

When you are done, you can go to the right panel, under the Measurement section and click on Done.

##Down to business
Calculate the distance between the pair of residues you used to create the restraints:


165 --> 65
<br>
178 --> 66
<br>
173 --> 113

Observe the results, discuss and answer the following questions in the shared notes:

- Which restraints are fullfilled?
- Why not all restraints are fullfilled?
- What could have happened?
- How do you interpret these results?



