# Exercises Week 4

## Exercise 1
![Petri Nets for exercise 1](week4_ex1_PN.png)
Given the following Petri Net, compute: 
1. P, T, F sets 
2. The reachability graph 
3. If the net is bounded or safe 
4. If the net terminates or is live 
5. If the net conforms to a workflow net

**Answers**\
(1)
| Key           | Value         |
| ------------- |:-------------:| 
| P    | {i[^1], P1, P2, P3, P4, P5, o[^1]} |
| T    | {A, B, C, D, E, F, XorS1, XorS2}|
| F    | {(i, A), (P1, B), (P2, C), (P2, XorS1) (P2, XorS2), (P3, E), (P4, F), (P5, D), (A, P1), (B, P2), (C, P3), (XorS1, o), (XorS2, P5), (D, P1), (F, P5)}      |

[^1]: i as in *input*-place/state and o as in *output*-plase/state

(2)
New={m0} dead-end, \
since there are no tokens in any of the places

(3)
To determine whether it is bounded or safe, we analyze the structure of the net and consider the flow of tokens:
1. **Boundedness**: A net is bounded if there is a finite upper limit to the number of tokens that can be present in any place, regardless of the sequence of transitions fired. If we can find a sequence of transitions that can lead to an unbounded increase in tokens in a place, then the net is unbounded.
2. **Safeness**: A net is safe if it is bounded and no place can have more than one token at any time during its execution. Safeness implies boundedness but with the additional constraint that the upper limit for the number of tokens in each place is one.

I guess there is a finite upper limit of 0 tokens present in any place, regardless sequence of transitions? *Hence, the petri net is bound.* And, there are no place can have excactly one token at any time, *hence the petri net is not a 1-Bounded safe*.\

(4)
The graph has a Start and End and the End has no possible outgoing transitions and there are possibilities for loops if a run encountered transitions C or XorS2, however this is irrelevant as there are no tokens and hence cannot run.

(5)
A Petri Net is a workflow net if it contains an input place/initial state and an output state/ final state, and that for every node in the graph is on a path from i to o.\

The net has exactly one start/i and one end/o and even though some paths might run some detours, they all at one point terminate in the End. *Hence, the Petri Net do conform to a workflow net*.

## Exercise 2 
![Petri Nets for exercise 2](week4_ex2_PN.png)
Given the following Petri Net, compute:
1. P, T, F sets
1. The reachability graph
1. If the net is bounded or safe
1. If the net terminates or is live
1. If the net conforms to a workflow net

**Answers**\
(1)
| Key           | Value         |
| ------------- |:-------------:| 
| P    | {i[^1], P1, P2, P3, P4} |
| T    | {A, B, C, D, AndS1}|
| F    | {(i, A), (P1, AndS1), (P2, B), (P3, c), (P4, D), (A, P1), (AndS1, P2), (AndS1, P3), (B, P4), (C, P4), (D, P3) }      |

[^1]: i as in *input*-place/state

(2)
The reachability graph can be seen on the image below. Since there are a loop in the end there are no final m´.
![Reachability graph for exercise 1.2](week4_ex2_b.png)

looking at the professors solution he solved it differently than in the slides - hence i will do that too, and i will use lucid.app instead of draw.io, only bc. i think it is prettier.
![Correct reachability graph for exercise 1.2](week4_ex2_b_better.png)

(3)
Since there can be more than one token in one place *the net is not safe*. There is a finite upper limit of two tokens in P4 and P3, however the limit for Start, P1 and P2 is one and *hence the net is not bound either*.

(4)
Here all paths leads to that all transitions can fire, *hence the net is live*. 

(5)
No, as there is no final place/state.

## Exercise 3
Speedy is a delivery company that wants to create a new reporting system for the top 
management. After inspecting the sales reports, the top management may also need to 
query the existing ERP system, based on Oracle Fusion, to get detailed sales and HR 
information.\
An ArchiMate model representing the process is enclosed below. 
![ArchiMate model for exercise 3](week4_ex3_AM.png)
Starting from this model, create an equivalent Petri Net and try to answer the following 
questions:
1. What is the reachability graph of the net?
1. Is the net sound?

**Answers**
![Petri Net solution of the ArchiMate model for exercise 3](week4_ex3_PN.png)
(1)\
![Reachability Graph solution of the Petri Nets for exercise 3](week4_ex3_RG.png)

(2) There is a termination place/state P5 (which is called p10 in the solution PN bc. i couldn't change it), and if it is an Xor then the net would be sound - since then there would only be tokens in P5, however i dont think it is and hence could lead to a termination with one token in P4 and one in P5 - *hence i think that the PN is not sound*.