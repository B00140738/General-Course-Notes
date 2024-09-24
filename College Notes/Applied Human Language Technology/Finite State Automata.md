#### Finite State Automata (FSA)

- **Definition**: FSAs describe machines used to recognize regular expressions.
- **Key Elements**:
    - States: q0, q1, q2...
    - Start state: q0
    - Final state: q4
    - Transitions between states represented by arcs

#### 4. Directed Graph Representation

- **Graph elements**:
    - Nodes (states)
    - Directed links (arcs)

#### 5. Formal View of FSAs

- **Components**:
    - Set of states (Q)
    - Alphabet (Σ)
    - Start state
    - Final states
    - Transition function mapping Q × Σ to Q

#### 6. Deterministic and Non-Deterministic FSAs

- **Deterministic**: Algorithm always knows the next state based on input.
- **Non-Deterministic**: Multiple possible transitions for a given input (introduces choice).

#### 7. Operations on Regular Languages

- Regular languages can be combined using:
    - **Union**
    - **Intersection**
    - **Concatenation**

#### 8. Generative Grammars

- **Definition**: Formal languages represented by FSAs can generate or accept languages.
- **Chomsky Hierarchy**: Describes different types of formal languages (context-free, context-sensitive, etc.).
