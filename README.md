# Fault Tree (Python)

## Introduction

**Fault Tree** is a special tree structure used to test the weakness in a network (for example, web network or computer network). All inner nodes contains a logic gate ("AND" gate or "OR" gate) and the value of any inner node is determined by its logic gate and its children's values (either 1 or 0). 

A **cut set** of the fault tree is a set of leaf values causing the root value equal to 1. A **Minimal cut set** (MCS) is a cut set with as few 1s as possible in it. If we define broken part of a network as value 1, then minimal cut sets can be used to understand the structural vulnerability of a system. 

Finding a minimal cut set for a fault tree is a NP hard problem. However, we can use Monte Carlo algorithm to find a solution or close solution for the minimal cut set (MCS) problem for a fault tree.

## Usage
Firstly, a raw input file with certain formate is provided (for example, input.txt). An xml file can be generated using parse.py. 

  - To parse the input into an xml file, in command line type python "parse.py" "input.txt"

  - The xml format will be used to form the defult tree

In this code, I used two different structure to represent the fault tree structure and realize its functions:
* A tree structure with node   (Fault_tree.py)
 
  To test the script, in command line type python "Fault_tree.py" "xml.txt" 10000 5

* A dictionary storing nodes with their name as the key (Fault_tree_dict)

  To test the script, in command line type python "Fault_tree_dict.py" "tree.txt" 10000 5

The test cases (input.txt, input1.txt, xml.txt) are in the folder Test_cases. Specially, input.txt and input1.txt are inputs for parse.
xml.txt is already in xml format and can serve as the input for Fault_tree and Fault_tree_dict.


## Credit
Thanks Dr.Ennan Zhai for comments.
Thanks Zhe (Bob) He for discussion
