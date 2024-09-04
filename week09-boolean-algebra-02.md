# Boolean algebra (part 02)

**Motivation**  
We want to simplify sum of product which is a general form
to represent any Boolean function. Efficient circuit highly depends
on this kind of optimization.  
Of course we can simplify any circuit with Boolean algebra   
manipulation procedure. But the way how to simplify the circuit
will help us to gain general understanding how to simplify the
efficient circuits.

Let us consider again the following table for Boolean function:
| $x$   | $y$   | $z$   | $G$   | |
|-------|-------|-------|-------|-|
| 1     | 1     | 1     | 0     | |
| **1** | **1** | **0** | **1** | $\leftarrow$ |
| 1     | 0     | 1     | 0     | |
| 1     | 0     | 0     | 0     | |
| 0     | 1     | 1     | 0     | |
| **0** | **1** | **0** | **1** | $\leftarrow$ |
| 0     | 0     | 1     | 0     | |
| 0     | 0     | 0     | 0     | |  

and from the previous lecture, we have the representation of boolean function   
$G(x, y, z)$ as using S.O.P (sum-of-product)
$$
  G(x, y, z) = x y \overline{z} + \overline{x}y\overline{z}
$$

In the end of this lecture, we can see that using K-maps, we can simply  
reduce the above boolean expression into a simpler one.


## Logic gates

### Introduction

The basic elements of circuits are caled **gates**.

Basic types of gates

Gates with $n$ inputs

When combination of circuits are formed, some gates may share inputs.  
The other method is to indicate the input separately for each gate.


**Example 2** (see textbook)   
A committee of three individuals decides issuess for an organization.  
Each individual votes either yes or no for each proposal that arises.  
A proposal is passed if it receives at least two yes votes.   
Design a circuit that determines whether a proposal passes.

First construct the sum of product for the problem.
Simplify using Boolean algebra identities (or K-maps, we will explain later).
and draw the circuit.

**Example 3** (see textbook)

### [optional] Combination of gates
- Example of circuits
- Half adders
- Full adders


## Minimization of circuits

### Introduction

**Literals**:  
A literal is a Boolean variable or its complement.

**Minterms**:  
A minterm of the Boolean variables $x_1, x_2, \ldots, x_n$ is  
a Boolean product $y_1 y_2 \cdots y_n$ , 
where $y_i = x_i$ or $y_i = \overline{x}_i$.  
Hence, a minterm is a product of $n$ literals, with one literal for each variable.   

**Example**: Find a minterm that equals 1 if $x_1 = x_3 = 0$ and
$x_2 = x_4 = x_5 = 1$, and equals $0$ otherwise.

$$
\overline{x}_1 x_2 \overline{x}_3 x_4 x_5
$$


### Karnaugh maps

K-maps give us a visual method for simplifying sum-of-product expansions.

**K-maps in two variables $(x, y)$**

**Example**

**K-maps in three variables $(x, y, z)$**

The product of literals corresponding to a block of all 1's in the K-map is  
called an **implicant**

It is called a **prime implicant** if this block of 1's is not contained in   
a larger of 1's representing the product of fewer literals than in this product

In the goal of simplifying K-map, we must always choose a block if it is the  
only block of 1's covering all the 1's in the K-map.  
Such a block represents an **essential prime implicant**.

$$
  \text{sum-of-product} =  \text{sum of prime implicant}
$$

Note that there may be <u>more than one way</u> to cover all the 1's using  
the least number of blocks.

**Example**


**K-maps in four variables $(w, x, y, z)$**

**Example**

### (optional) Don't care conditions
### (optional) The Quine-McCluskey Method
