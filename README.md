# SMT Solving for Formulas in the Flat Monadic Metric Time Normative Logic:

This project's goal is to reason about the satisfiability of formulas in  FMMTNL 
Written in Python and using the Z3 solver, the tool computes a formula in the logic and checks weather it is satisfiable and returns the shortest trace in terms of number of events when it exists.


## Installation
Python 3.11.3 or above.

Z3 library in python:
```
pip install z3-solver
```
## Usage
1- Execute the satisfiability checker
```
python satcheck.py
```
2- Type a valid formula according to the syntax, the file Examples contain a list of formulas one can copy and paste, example:

```
O open {[0,7],[12,inf]} & (O Load {[3,27]} || F complain {[2,200]})
```


## Syntax :
Norm ::=  O Action IS  , F Action Is , Norm  & Norm, Norm  || Norm

Action ::=  String 

I ::= [Int,Int] | [Int,inf] $~~~~~~~~~~(Interval)$

Is ::= \{I, ..., I\} $~~~~~~~~~~\quad\quad(Interval Set )$

inf ::= $+\infty$

& is for conjunction 

|| is for disjunction

