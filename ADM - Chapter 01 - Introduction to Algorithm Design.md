Links: [[Algorithm Design Manual]]
Tags: #Algorithms #Computer_Science

# TOC
- [[#1.0 Introduction to Algorithm Design]]
- [[#1.1 Robot Tour Optimization]]
- [[#1.2 Selecting the Right Jobs]]
- [[#1.3 Reasoning about Correctness]]
	- [[#1.3.1 Problems and Properties]]
	- [[#1.3.2 Expressing Algorithms]]
	- [[#1.3.3 Demonstrating Incorrectness]]
- [[#1.4 Induction and Recursion]]
- [[#1.5 Modeling the Problem]]
	- [[#1.5.1 Combinatorial Objects]]
	- [[#1.5.2 Recursive Objects]]
- [[#1.6 Proof by Contradiction]]
- [[#1.7 About War Stories]]
- [[#1.8 War Story Psychic Modeling]]
- [[#1.9 Estimation]]
- [[#1.10 Exercises]]


## 1.0 Introduction to Algorithm Design

### What is an Algorithm?
- *algorithm* - <i>a procedure to accomplish a specific task, taking any of the possible inputs of an</i> *algorithmic problem* <i>and transforming it into the desired output</i>.

An algorithm must solve a general, well-specified problem. An *algorithmic problem* is the complete set of instances (<i>or cases</i>) the algorithm must correctly solve. In other words:
- *algorithmic problem* - <i>a specific and general issue that an algorithm could solve all cases of</i>.

For example: "Sort a given array." is an algorithmic problem. But "sort the array: [1, 5, 7, 2, 21, 3]" is an instance/case of the same algorithmic problem stated earlier. The key difference here being that the second one is generalized.

### What makes a Good Algorithm?
#### 3 Desirable Properties of a Good Algorithm
1. The algorithm is <u>correct</u>.
2. The algorithm is <u>efficient</u>.
3. The algorithm is <u>easy to implement</u>.

These properties may not be simultaneously achievable for every algorithm. This chapter will focus on algorithm <i>correctness</i>. Chapter 2 will focus on algorithm <i>efficiency</i>.

### It is Rarely Obvious that an Algorithm is Correct.
It is rarely obvious that an algorithm correctly solves a given problem. Correct algorithms usually come with a <i>proof</i>: 
- *proof* - <i>explains why we know an algorithm takes every instance of a problems' input and produces the desired output of a problem</i>.

The next sections demonstrates why <i>"it's obvious"</i> never suffices as a proof of correctness, and is usually flat-out wrong.


## 1.1 Robot Tour Optimization
[[#TOC|Back to Top]]

### What is a Heuristic?
- *heuristic* - <i>a technique/procedure used to solve a problem or make decisions more efficiently, even if it does not guarantee a correct nor optimal solution. NOTE: A HEURISTIC IS NOT AN ALGORITHM</i>.

*The fundamental difference between algorithms and heuristics is:*
- algorithms ALWAYS produce a correct result.
- heuristics may do a good job, but provide NO guarantee of correctness.

### Traveling Salesman Problem/Robot Tour Optimization
The rest of this section is based off the following problem:
- Suppose that we have a robot arm that needs to solder and connect wires between points on a plane in a 2d space. It takes the robot arm some amount of time to get between two points. Design an algorithm to efficiently connect all the points, creating a cycle, and taking the least amount of time possible.

A more appropriate definition of the problem:
- Problem: Robot Tour Optimization
- Input: A set $S$ of $n$ points in the plane.
- Output: What is the shortest cycle tour that visits each point in the set $S$?

#### Nearest Neighbor
There are many possible solutions to this problem, but one of the first (and maybe obvious idea) would be the <i>nearest-neighbor heuristic</i>:
1. Starting from a starting point $p_0$, walk to its nearest neighbor $p_1$.
2. From $p_1$ walk to its nearest uninvited neighbor(<i>a point we've yet to been at</i>).
3. Repeat steps $1$-$2$ until we've visited all points in the set $S$.
4. Upon reaching the final point $p_n$ in the set $S$, return back to $p_0$ to close off the tour.

In pseudo-code nearest-neighbor would look like:
```pseudo-code
NearestNeighbor(P)
	Pick and visit an initial point p_0 from P
	p = p_0
	i = 0
	While there are still unvisited points
		i = i + 1
		Select pi to be the closest unvisted point to p_i-1
		Visit p_i
	Return to p_0 from p_n-1
```

![[ADM-Ch01-f1.2.jpg]]
This first instance of points are roughly evenly spaced from each other in a roughly circular pattern.

![[ADM-Ch01-f1.3.jpg]]
This second instance of points are each laid out in a straight line with varying distances from each other. The point `0` is our starting point, with every other point being labeled by it's distance (<i>positive or negative</i>) from our start point.

#### Closest Pair

![[ADM-Ch01-f1.4.jpg]]
This last instance shows the points laid out in 2 straight lines in the same format. The distance between the two horizontal lines of points is shorter than the distance between two points in the same line.

## 1.2 Selecting the Right Jobs
[[#TOC|Back to Top]]


## 1.3 Reasoning about Correctness
[[#TOC|Back to Top]]

### 1.3.1 Problems and Properties

### 1.3.2 Expressing Algorithms

### 1.3.3 Demonstrating Incorrectness


## 1.4 Induction and Recursion
[[#TOC|Back to Top]]


## 1.5 Modeling the Problem
[[#TOC|Back to Top]]

### 1.5.1 Combinatorial Objects

### 1.5.2 Recursive Objects


## 1.6 Proof by Contradiction
[[#TOC|Back to Top]]


## 1.7 About War Stories
[[#TOC|Back to Top]]


## 1.8 War Story: Psychic Modeling
[[#TOC|Back to Top]]


## 1.9 Estimation
[[#TOC|Back to Top]]


## 1.10 Exercises
[[#TOC|Back to Top]]