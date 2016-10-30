# PlanningFacts
Extracts facts from classical AI planning tasks according to Yoon, Fern & Givan papers:

Learning Control Knowledge for Forward Search Planning (2008)
<http://www.jmlr.org/papers/volume9/yoon08a/yoon08a.pdf>

Learning Heuristic Functions from Relaxed Plans (2006)
<http://www.cs.orst.edu/%7Eafern/papers/icaps06.ps>

## Credits
This software was built on top of the FastForward (FF) planning algorithm, by Joerg Hoffmann.
<https://fai.cs.uni-saarland.de/hoffmann/ff.html>

## Usage
After downloading the project, simply run the make file to get acces to the runnable ff.
Usage is simillar to the FF algorithm.
Use parameters -o to define the domain file and -f to define the problema file as such:
./ff -o domain_file -f problem_file

## Output
The expected ouput is a series of databases as defined by Yoon, Fern and Givan in the aforementioned papers.
Formatting is as follows:

For each state in the solution set:
* 1st line: Initial State Facts
* 2nd line: Relaxed Plan (actions)
* 3rd line: Delete List from the plan's actions
* 4th line: Add List from the plan's actions
* 5th line: Goal State Facts
* 6th line: Facts both in the Initial State and the Goal State
* 7th line: Blank
* Repeat

When it's the case that no such information exists (e.g. no facts both in initial state and goal state), a blank line is printed, keeping the order of the information fixed.
