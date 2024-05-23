# Week 02: Fomal Languages

To describe a **language** $L$, we look at the sequences of inputs (the lables on the transitions) that can lead to the accepting state.

An **Alphabet** $\sum$ is the lables on the transition arrows.

A **string**/word is a sequence of members in the alphabet.

## Deterministic Finite Automaton (DFA)

- **States (Q)**: A finite set of states in the automaton.
- **Alphabet ($\sum$)**: A finite set of input symbols that the automaton can read.
- **Transition Function ($\delta$)**: A function that takes a current state and an input symbol and returns the next state. It is deterministic, meaning there is exactly one next state for each state and input symbol pair.
- **Start State (q₀)**: The state where the automaton begins its computation.
- **Accepting States (F)**: A subset of states that determine if the input string is accepted by the DFA.

### Formal Definition
A DFA is defined by a 5-tuple (Q, Σ, δ, q₀, F):
- \( Q \): Finite set of states.
- \( Σ \): Finite set of input symbols (alphabet).
- \( δ: Q \times Σ \to Q \): Transition function.
- \( q₀ \): Start state.
- \( F \subseteq Q \): Set of accepting (final) states.

### How a DFA Operates
1. **Start**: Begin in the start state \( q₀ \).
2. **Read Input**: Read the input string symbol by symbol.
3. **Transition**: Move from the current state to the next state according to the transition function δ.
4. **Acceptance**: After reading the entire input string, if the DFA is in an accepting state (a state in F), the input string is accepted. Otherwise, it is rejected.

### Example DFA
Recognize binary strings that end with '01'.

1. **States (Q)**: {q₀, q₁, q₂}
2. **Alphabet (Σ)**: {0, 1}
3. **Transition Function (δ)**:

| Current State | Input Symbol | Next State |
|---------------|--------------|------------|
| q₀            | 0            | q₀         |
| q₀            | 1            | q₁         |
| q₁            | 0            | q₂         |
| q₁            | 1            | q₁         |
| q₂            | 0            | q₀         |
| q₂            | 1            | q₁         |

4. **Start State (q₀)**: q₀
5. **Accepting States (F)**: {q₂}

#### String Examples
1. **Input**: "1101"
   - Sequence: q₀ → q₁ → q₁ → q₂ → q₁
   - Result: Rejected (not in accepting state)

2. **Input**: "101"
   - Sequence: q₀ → q₁ → q₂ → q₁
   - Result: Rejected (not in accepting state)

3. **Input**: "001"
   - Sequence: q₀ → q₀ → q₀ → q₁ → q₂
   - Result: Accepted (in accepting state)

### Key Properties
- **Deterministic**: For each state and input symbol, there is exactly one transition.
- **Finite**: The number of states and transitions is finite.
- **Regular Languages**: DFAs recognize regular languages, which can be described by regular expressions.

