# Combinatorials

Combinatorics is the study of arrangements of objects.   
This subject arose in the study of gambling games.

## The basics of counting

**The product rule**   
Suppose that a procedure can be broken down into a sequence of   
two tasks. if there are $n_1$ ways to do the first task and for 
each of these wways of doing the first task, there are $n_2$ ways
to do the second task, then there are $n_1 n_2$ ways do to the
procedure

### Example 01
A new company with just two employees, Sarah and Paul, rents 
a floor of a building with 12 offices. How many ways are there to 
assign different offices to these two employes?

### Example 05
How many different license plates can be made if each plate
contains a sequence of two uppercases English letters
followed by four digits and followed by three uppercase 
English letter?

**The sum rule**   
If a task can be done either in one of $n_1$ ways or in one of 
$n_2$ ways, where none of the set of $n_1$ ways is the same as
any of the set of $n_2$ ways, then there are $n_1 + n_2$
ways to do the task.

### Example 12  
Suppose that either a member of the information systems study 
programme or a student who is an information systems major
is chosen as a representative to an institute committee. How many
different choices are there for this representative if there are
37 members of the information systems study programme abd 83
information systems majors and no one is both a study programme
members and a student?


**The subtraction rule**   
If a task can be done in either $n_1$ ways or $n_2$ ways, 
then the number of ways to do the task is $n_1 + n_2$ minus
the number of ways to do the task that are common to the two 
different ways.

### Example 19 
A computer company receives 350 applications from college graduates
for a job planning a line of new web servers. Suppose that
220 of these applicants majored in informatics, 
147 majored in business, and 51 majored
in both in informatics and business. How many of these applicants
majored neither in informatics nor in business?

**The division rule**   
There are $n/d$ ways to do a task if it can be done using a 
procedure that can be carried out in $n$ ways, and for every way
$w$, exactly $d$ of the $n$ ways correspond to way $w$.

### Example 20
Suppose that an automated system has been developed that counts
the legs of cows in a pasture. Suppose that this system
has determined that in a farmer's pasture there are exactly 572 
legs. How many cows are there is this pasture, assuming that
each cow has four legs and that there are no other animal present?

### Example 21

## Tree diagrams
A tree consists of a root, a number of branches laving the root, 
and the possible additional branches leaving the endpoints of
the other branches.

### Example 24
Suppose that "I Love Balikpapan" T-shirts come in five different
sizes: S, M, L, XL, and XXL. Further suppose that each size
comes in four colors, white red, green, and black except for XL,
which comes only in red, green, and black, and XXL, which
comes only in green and black. How many different shirt does a 
souveninr shop have to stock to have at least one of each available 
size and color of the T-shirt?

## Permutations and combinations

A **permutation** of a set of distinct objects is an ordered
arrangement of these objects.   
An ordered arrangement of $r$ elements of a set is called an
**$r$-permutation**.

### Theorem 1
> If $n$ is a positive integer and $r$ is an integer with 
> $1 \leq r \leq n$, then there are
> $$
>   P(n, r)  = n(n-1)(n-2) \cdots (n-r + 1)
> $$
> $r$ permutations of a set with $n$ distinct elements.

### Corollary 1
> If $n$ and $r$ are integers with $0 \leq r \leq n$, then
> $P(n, r) = \dfrac{n!}{(n-r)!}$

An **$r$-combination** of elements of a set is an unordered
selection of $r$ elements from the set.

### Theorem 2
> The number of $r$-combinations of a set with $n$ elements, 
> where $n$ is a nonnegative integer and $r$ is an integer
> with $0 \leq r \leq n$, equals
> $$
>   C(n, r)  = \frac{n!}{r!(n-r)!}
> $$

## Permutations with repetitions and combinations with repetitions

### Example 1

### Theorem 1
> The number of $r$-permutations of a set of $n$ objects
> with repetition allowed is $n^r$

### Example 2

### Theorem 2
> There are $C(n+r -1, r) = C(n+r-1, n-1)$ $r$-combinations
> from a set with $n$ elements when repetition of elements
> is allowed.

**Table 1** Combinations and Permutation With and Without 
Repetition.
| Type | Repetition Allowed? | Formula |
|------|---------------------|---------|
| $r$-permutations | No      | $\dfrac{n!}{(n-r)!}$    |
| $r$-combinations | No      | $\dfrac{n!}{r! (n-r)!}$ |
| $r$-permutations | Yes     | $n^r$   |
| $r$-combinations | Yes     | $\dfrac{(n+r-1)!}{r!(n-1)!}$ |

## Permutations with indistinguishable objects

### Example 7 
How many different strings can be made by reordering the letters
of the word _SUCCESS_?

### Theorem 3
> The number of different permutations of $n$ objects, 
> where there are $n_1$ indistinguishable objects of type 1, 
> $n_2$ indistinguishable objects of type 2, ..., and 
> $n_k$ indistinguishable objects of type $k$, is
> $$
>  \frac{n!}{n_1! n_2! \cdots n_k!}
> $$