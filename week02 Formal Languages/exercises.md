# Week 02 Exercises

## Exercise 01
Describe the language of this automaton:
![](./exercise%20files/ex01_automaton.png)

### Solution
States: {off, dim, bright}\
Transitions: {press, $\epsilon$}\
Initial state: {off}\
Accepting state: {off}\

**To describe the language, we look at the sequences of inputs (press) that can lead to the accepting state off.**

The automaton accepts the language consisting of the string "press press press" (or (press)^3).
It also accepts the empty string ε since the automaton can stay in off without any input.

In summary, the language $L$ of the automaton can be formally described as:

$L=${ϵ,{press, press, press}}

This means the automaton accepts either no input at all (remains in the initial state off via ε transitions) or exactly three press inputs that cycle through dim and bright states back to off.

## Exercise 02:
How many words exist in this language?
![](./exercise%20files/ex02_dfa.png)

### Solution

w1={pass assignment, pass exam}
w2={pass assignment, study, pass exam}
w3={pass assignment, pass exam, study}

## Exercise 03:
Describe in natural language the following automata
![](./exercise%20files/ex03_automata.png)

### Solution

#### Automaton A
States: there are two, lets call them $i$ and $f$\
Transitions: {a, b}\
Initial state: {$i$}\
Accepting state: {$f$}\
Expressions: {(b*, a+)+}
where * is 0 or more times and + is 1 or more times

#### Automaton B
States: there are two, lets call them $i$ and $f$\
Transitions: {a, b}\
Initial state: {$i$}\
Accepting state: {$f$}\
Expressions: {(a|b)*, b+}
where * is 0 or more times and + is 1 or more times

#### Automaton C
States: there are two, lets call them $if$ and $q_1$\
Transitions: {a, b, c}\
Initial state: {$if$}\
Accepting state: {$if$}\
Expressions: 
let $s_1$ = {a, (a | c)*, b}, then 
{$(b|c)\*, $s_1$\*},
where * is 0 or more times and + is 1 or more times

#### Automaton D
States: there are three, lets call them $i$, $f_1$ and $f_2$\
Transitions: {a, b, c}\
Initial state: {$i$}\
Accepting state: {$f_1$, $f_2$}\
Expressions: \
let: 
- $s_1$ = {(a | b | c)*}
- $s_2$ = {(b | c)+}
- $s_3$ = {b+, $s_4$?}
- $s_4$ = {(a | c), $s_1$}

then exp: 
{$s_1$ | $s_2$ | $s_3$},
where * is 0 or more times, + is 1 or more times and ? is 0 or 1 time

#### Automaton E
States: there are three, lets call them $if$, $q_1$ and $q_2$\
Transitions: {a, b, c}\
Initial state: {$if$}\
Accepting state: {$if$}\
Expressions: \
let: 
- $s_1$ = {(b | c)*}
- $s_2$ = {a+, ((c, $s_1$) | $s_3$)}
- $s_3$ = {b, a*, c, $s_1$}

then exp: 
{$s_1$, $s_2$}
where * is 0 or more times and + is 1 or more times

## Exercise 4, 5 and 6 
I dont think will be relevant for the exam