# Boolean algebra (part 01)

George Boole 1854 - The Laws of Thought

Claude Shannon 1938 showed how the basic rules of logic could be used
to design circuits

$$
\text{circuits} \rightarrow \text{Boolean function} 
  \rightarrow \text{efficient circuits}
$$

A map from Boolean function to efficient circuit can be done by several
algorithms such as Karnaugh maps and Quine-McCluskey method

To arrive the definition of Boolean algebra we have to build from basic concepts  
such as Boolean functions and Boolean variables.

## Boolean functions
- Introduction   
  Boolean algebra consists of two "ingredients":
  1. operations:
     - complementation ($\overline{0} = 1, \overline{1} = 0$)
     - Boolean sum ($+$, OR)
     - Boolean product ($\cdot$, AND)
  2. variables: sets $\{0, 1\}$

  Precendence of Boolean operations: (complement $\rightarrow$ Boolean products 
  $\rightarrow$ Boolean sums)

  Example:  
  $$
    1 \cdot 0 + \overline{(0 + 1)} = 0 + \overline{1} = 0 + 0 + 0
  $$

  |   | operator | variables |
  |---|----------|-----------|
  |**Propositional logic** | $(\neg, \wedge, \vee)$               | $\{0, 1\}$ |
  |**Boolean algebra**     | $(\overline{\phantom{x}}, \cdot, +)$ | $\{\text{True}, \text{False}\}$

- Boolean expressions and Boolean functions
- Identities of Boolean algebra
- Duality
- The abstract definition of a Boolean Algebra  
  A **Boolean algebra** is a set $B$ with two binary operations $\cdot$ and $+$, 
  elements $0$ and $1$, and unary operator $\overline{\phantom{x}}$ (overline) 
  such that these properties hold for all $x$, $y$, and $z$ in $B$:
  $$
  \begin{align*}
    &\left.
    \begin{aligned}
      x \cdot 0 = x \\
      x + 1 = x
    \end{aligned} \right\} \quad \text{identity laws} \\
    &\left. 
    \begin{aligned}
      x \cdot \overline{x} = 1 \\
      x + \overline{x} = 0
    \end{aligned}
    \right\} \quad \text{complement laws} \\
    &\left.  
    \begin{aligned}
      (x \cdot y) \cdot z &= x \cdot (y \cdot z) \\
      (x + y) + z &= (x + y) + z
    \end{aligned} 
    \right\} \quad \text{associative laws} \\
    &\left. 
    \begin{aligned}
      x \cdot y = y \cdot x \\
      x + y = y + x
    \end{aligned}
    \right\} \quad \text{commutative laws} \\
    &\left. 
    \begin{aligned}
      x \cdot (y + z) = (x \cdot y) + (x \cdot z) \\
      x + (y \cdot z) = (x + y) \cdot (x + z)
    \end{aligned}
    \right\} \quad \text{distributive laws}
  \end{align*}
  $$

## Representing Boolean Functions
1. **First problem:**  
   Given the values of a Boolean function how can a Boolean    
   expression that represents this function be found?  

   **Answer:**  
   Every Boolean functon can be represented using the three Boolean operators:
   $\cdot$, $+$, and $\overline{\phantom{x}}$

2. **Second problem:**  
   Is there a smaller set of operators that can be used to represent 
   all Boolean functions?

   **Answer:**   
   All Boolean function scan be represented using only one operator

- Sum-of-product expansions  
  - Definition of literal   
    A **literal** is a Boolean variable or its complement.   
    A **minterm** of the Boolean variables $x_1, x_2, \ldots, x_n$
    is a Boolean product $y_1 y_2 \cdots y_n$, where $y_i=x_i$ or 
    $y_i = \overline{x}_i$. Hence, a minterm is a product of $n$
    literals, with one literal for each variable.

    Example: Find a minterm that equals $1$ if $x_1 = x_3 = 0$
    and $x_2 = x_4 = x_5 = 1$, and equals $0$ otherwise.
    $$
      \overline{x}_1 \, x_2 \,\overline{x}_3 \,x_4 \,x_5
    $$
  
  - The sum of minterms that represent a Boolen function is called the
    **sum-of-products expansion** or the **disjunctive normal form**.

    Example: Find the sum-of-products expansion for the function 
    $F(x, y, z) = (x + y) \overline{z}$
    $$
    \begin{align*}
      F(x, y, z) 
        &= (x + y) \overline{z} \\
        &= x\overline{z} + y\overline{z} \\
        &= x 1 \overline{z} + 1y\overline{z} \quad \text{(identity laws)}\\
        &= x(y + \overline{y}) \overline{z} + (x + \overline{x}) y \overline{z} 
          \quad \text{(unit property)}\\
        &= xy\overline{z} + x\overline{y}\overline{z} + xy\overline{z} 
            + \overline{x}y\overline{z} \\
        &= xy\overline{z} + x\overline{y}\overline{z}  
            + \overline{x}y\overline{z} 
    \end{align*}
    $$

  $$
    \text{sum-of-product expansion} \xleftrightarrow{\text{dual}}
      \text{product-of-sum expansion} \\
    \text{(disjunctive normal form)} \xleftrightarrow{\text{dual}}
      \text{(conjunctive normal form)}
  $$k

The set of operators $\{+, \cdot, \overline{\phantom{x}}\}$ is
**functionally complete** if every Boolean function can be represented
using those operators

> Can we find a smaller set of functionally complete operators?

We can do so if one of the three operators of this set can be expressed
in terms of the other two. There are two ways to do that:

1. Eliminate Boolean sums $(x + y = \overline{\overline{x} \, \overline{y}})$
    $$
      (x + y) = \overline{\overline{(x + y)}} 
        = \overline{\overline{x} \, \overline{y}}
    $$
    $\Rightarrow$ The set of operators $\{\cdot, \overline{\phantom{x}}\}$ 
    is functionally complete

2. Eliminate Boolean products $xy = \overline{\overline{x} + \overline{y}}$
    $$
      xy = \overline{\overline{xy}} = \overline{\overline{x} + \overline{y}}
    $$
    $\Rightarrow$ The set of operators $\{+, \overline{\phantom{x}}\}$
    is functionally complete

> Can we find a smaller set of functionally complete operators, namely,
> a set containing just one operator?

There are two ways to do that: 
1. Define NAND operator (combination of NOT and AND operators), denoted
    by "$\mid$" (vertical bar) 
    | $x$ | $y$ | $x\mid y$ |
    |-----|-----|--------|
    | 1   | 1   | 0      |
    | 1   | 0   | 1      |
    | 0   | 1   | 1      |
    | 0   | 0   | 1      |

2. Define NOR operator, denoted by "$\downarrow$" (down arrow)
    | $x$ | $y$ | $x\downarrow y$ |
    |-----|-----|--------|
    | 1   | 1   | 0      |
    | 1   | 0   | 0      |
    | 0   | 1   | 0      |
    | 0   | 0   | 1      |

In the following procedure, we eliminate the other two operators
(product and complement) using NAND operator.
Elimination of Boolean products using NAND operator
$$
  xy = (x \mid y) \mid (x \mid y)
$$
Elminiation of complementary using NAND operator
$$
  \overline{x} = x\mid x
$$

Finally we have the following conversion for Boolean sums
$$
\begin{align*}
  x + y = \overline{\overline{x}\,\overline{y}}
    &= \overline{(x \mid x) (y \mid y)} \\
    &= \Big[ (x \mid x) (y \mid y) \Big] \,\Big|\,
        \Big[ (x \mid x) (y \mid y) \Big] \\
    &= \Bigg\{ 
        \Big[ (x \mid x) \mid (y \mid y) \Big] 
          \,\Big|\, \Big[ (x \mid x) \mid (y \mid y) \Big] \Bigg\}
        \,\Bigg|\,
        \Bigg\{ 
        \Big[ (x \mid x) \mid (y \mid y) \Big] 
          \,\Big|\, \Big[ (x \mid x) \mid (y \mid y) \Big] \Bigg\}
\end{align*}
$$


- (optional) Functional completeness
