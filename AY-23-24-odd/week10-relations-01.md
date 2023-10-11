# Relations (part 01)

### Objectives:
- Understanding basic concept of relations in mathematics
- An application of relations that is heavily used in 
  technology information: Databases and SQL.


## Relations and their properties

### Introduction

**Definition**: Let $A$ and $B$ be sets. A _binary relation from_
$A$ _to_ $B$ is the subset of $A \times B$.

**Example**: 
- $A = \{\text{all the students in Information Systems}\}$ 
- $B = \{\text{all the courses in Information Systems}\}$
- $R = \{(a, b)\}$, where $a$ is a student enrolled in course $b$.  
  For instance:  
  $R = \{(\text{Andi, SI518}),
            (\text{Debora, SI518}), (\text{Andi, SI510})\}$

**Example**   
- $A = \{\text{all the cities in Kalimantan} \}$ 
- $B = \{\text{all the provinces in Kalimantan} \}$
- $R = \{(a, b)\}$, where $a$ is a capital city of a province $b$   
  For instance:   
  $R = \{(\text{Samarinda, Kalimantan Timur}), 
          (\text{Banjarmasin, Kalimantan Selatan}) \newline
            \qquad\quad,(\text{Pontianak, Kalimantan Barat}), 
          (\text{Tarakan, Kalimantan Utara}), \newline
            \qquad\quad, (\text{Palangka Raya, Kalimantan Tengah})\}$

**Example**  
- $A = \{0, 1, 2\}$   
- $B = \{a, b\}$
- $R = \{(0, a), (0, b), (1, a), (2, b)\}$


### Function as relations

### Relations on a set
**Definition**: A _relation on a set_ $A$ is a relation from $A$ to $A$.

**Example**:  
- $A = \{1, 2, 3, 4\}$ 
- $R = \{(a, b) \mid a \text{ divides } b\}$ where $a \in A$, $b \in A$

**Example**: 
Consider the following relations:
- $R_1 = \{(a, b) \mid a \leq b\}$
- $R_2 = \{(a, b) \mid a > b\}$   
- $R_3 = \{(a, b) \mid a = b \text{ or } a = -b\}$

$(1, 1)$ is in $R_1$, $R_3$;   
$(2, 1)$ is in $R_2$

### Properties of relations
  - Reflexive
  - Symmetric, Antisymmetry
  - Transitive
### (optional) Combining relations
  Definition of composite

## $n$-ary relations and their applications
### Introduction
### $n$-ary relations
### Databases and relations
- **records**
- **fields**
- **tables**
- **attributes**
- **primary keys**

- **extension**
- **intension**

**Table 1**: `students`
| `student_name` | `id_number` | `major`              | `gpa` |
|----------------|-------------|----------------------|-------|
| Ahmad          | 10100201    | Information systems  | 3.88  |
| Andi           | 01100304    | Physics              | 3.45  |
| Candra         | 10100301    | Information system   | 3.49  |
| Galih          | 11100401    | Informatics          | 3.45  |
| Rasyid         | 11100501    | Informatics          | 3.90  |
| Stefani        | 18100102    | Digital business     | 2.99  | 


### Operations on $n$-ary relations

**Table 2**: `gpas`
| `student_name` | `gpa` |
|----------------|-------|
| Ahmad          | 3.88  |
| Andi           | 3.45  |
| Candra         | 3.49  |
| Galih          | 3.45  |
| Rasyid         | 3.90  |
| Stefani        | 2.99  |


**Table 3**: `enrollments`
| `student` | `major`                   | `course` |
|-----------|---------------------------|----------|
| Gilang    | Environmental Engineering | TL 290   | 
| Gilang    | Environmental Engineering | KU 475   | 
| Gilang    | Environmental Engineering | FI 410   |
| Marlan    | Mathematics               | MK 511   |
| Marlan    | Mathematics               | MK 603   |
| Marlan    | Mathematics               | IF 322   |
| Silfi     | Informatics               | MK 575   |
| Silfi     | Informatics               | IF 455   |

**Table 4**: `majors`
| `student` | `major`                   |
|-----------|---------------------------|
| Gilang    | Environmental Engineering |
| Marlan    | Mathematics               |
| Silfi     | Informatics               |


**Table 5**: `teaching_assignments`
| `lecturer` | `department`        | `course_number` |
|------------|---------------------|-----------------|
| Carla      | Oceanography        | 335             |
| Carla      | Oceanography        | 412             |
| Fahmi      | Digital business    | 501             |
| Fahmi      | Digital business    | 617             |
| Gina       | Physics             | 544             |
| Gina       | Physics             | 551             |
| Rahel      | Information Systems | 518             |
| Rahel      | Mathematics         | 575             |


**Table 6**: `class_schedule`
| `department`        | `course_number` | `room` | `time`     |
|---------------------|-----------------|--------|------------|
| Information systems | 518             | G521   |  2:00 P.M. |
| Mathematics         | 575             | G502   |  3:00 P.M. |
| Mathematics         | 611             | G521   |  4:00 P.M. |
| Physics             | 544             | B505   |  4:00 P.M. |
| Digital business    | 501             | A100   |  3:00 P.M. |
| Digital business    | 617             | A110   | 11:00 A.M. |
| Oceanography        | 335             | A100   |  9:00 A.M. |
| Oceanography        | 412             | A100   |  8:00 A.M. |


**Table 7**: `teaching_schedule`
| `lecturer` | `department`        | `course_number` | `room` | `c_time`     |
|------------|---------------------|-----------------|--------|------------|
| Carla      | Oceanography        | 335             | A100   |  9:00 A.M. |
| Carla      | Oceanography        | 412             | A100   |  8:00 A.M. |
| Fahmi      | Digital business    | 501             | A100   |  3:00 P.M. |
| Fahmi      | Digital business    | 617             | A110   | 11:00 A.M. |
| Gina       | Physics             | 544             | B505   |  4:00 P.M. |
| Rahel      | Information systems | 518             | G521   |  2:00 P.M. |
| Rahel      | Mathematics         | 575             | G502   |  3:00 P.M. |


### SQL

**Table 8**: `flights`
| `airline` | `flight_number` | `gate` | `destination` | `departure_time` |
|-----------|-----------------|--------|---------------|------------------|
| Garuda    | 122             | 34     | Balikpapan    | 08:10            |
| Citilink  | 221             | 22     | Jakarta       | 08:17            |
| Citilink  | 122             | 33     | Semarang      | 08:22            |
| Citilink  | 322             | 34     | Denpasar      | 08:30            |
| Garuda    | 199             | 13     | Balikpapan    | 08:47            |
| Citilink  | 222             | 22     | Jakarta       | 09:10            |
| Garuda    | 322             | 34     | Balikpapan    | 09:44            |



```sql
SELECT departure_time
  FROM flights
  WHERE destination="Balikpapan"
```

```sql
SELECT lecturer, c_time
  FROM teaching_assignments, class_schedule
  WHERE department="Mathematics"
  
```

### (optional) Association rules from data mining


Student who solve the problem: Radid (10231076)