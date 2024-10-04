- Set Operations
  - Introduction
    - Definition of union of the sets $A$ and $B$
    - Definition of intersection of the sets $A$ and $B$
    - Definition of two disjoint sets.   
      For two disjoint sets $A$ and $B$, we have the following relations
      $$
        |A \cup B| =  |A| + |B|
      $$    
      For the general case, we will have principle of inclusion-exclusion.

    - Definition of difference of two sets $A$ and $B$.   
      We can represent the difference by intersection and complement   
      $$
        A - B = A \cap (\overline{A \cap B})
      $$
    - Definition of complement of a set 
    - Principle of inclusion-exclusion (use Venn Diagram)
        $$
        \begin{align*}
          A \cup B &= ((A - B) \cup (A \cap B)) \cup (B - A) \\
          |A \cup B|  
            &= (|A - B| + |A \cap B|) + |B - A| \\
            &= ((|A| - |A \cap B|) + (A \cap B)) + (|B| - |A \cap B|) \\
            &= |A| + |B| - |A \cap B|
        \end{align*}
        $$
        In the first row, we use the fact that $(A - B)$, $A \cap B$,
        and $B - A$ are all disjoint sets to each others, and we can use 
        the fact that for the two disjoint sets $P$ and $Q$, we have 
        $|A \cup B| = |A| + |B|$.
      - Some examples of inclusion-exclusion formula application    
        **Example**  
        $U = $ the set of all Information Systems students, $|U| = 400$   
        $A = $ the set of all Information Systems students class 2023
        who get the GPA  more than 3.00, $|A| = 35$  
        $B = $ the set of all Information Systems students class 2023
        who get the GPA less than 3.50, $|B| = 50$    
        $A \cap B = $ the set of all Information Systems students class 2023
        who get the GPA between 3.00 and 3.50 exclusively (without endpoints),
        $|A \cap B| = 15$.   
        Determine the number of students who are not belong to Information 
        Systems students class 2023.


  - Set identities
    - De Morgan's laws    
      Show it with Venn's diagram    
      **Example**   
      Calculate $\overline{((A \cup B) \cap C) \cup D}$
  - Membership tables
  - Proof De Morgan's laws using Venn Diagram and membership table

- (optional) 
  - Generalized Unions and Intersections
  - Computer representation of sets


