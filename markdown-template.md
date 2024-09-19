The following is the short tutorial how to use markdown.  
It is better to show markdown preview in VSCode than in GitHub.

For the complete tutorial, visit: [Markdown Guide](https://www.markdownguide.org/basic-syntax/)

Each section, subsection, and subsubsection are recommeded to write
using header `#`.

# Title

## Section 1

To write a paragraph you do not need to worry about the line 
break. It will automatically put a line break to maximize the
view in rendering side. For better view, you should consider
to write your paragraph not in single line, just like this
paragraph. I put a break before the character reach the maximum
width of 80 characters.

### Subsection 1.1

#### Subsubsection 1.1.1

#### Subsubsection 1.1.2

### Subsection 1.2

## Section 2

## Section 3

## Text formatting
- To separate between paragraphs, you can use one empty newline.

  paragraph 1

  paragraph 2

- To make a newline, add two spaces at the end of sentences.

  line 1  
  line 2

  or using HTML linebreak `<br>`  
  line 1<br>
  line 2

- Text emphasize:   
  `**bold**`: **bold**,   
  `_italic_`: _italic_

- Inline monospace text (for code): `histogram = ax.plot()`

- Code block:
  ```py
  def scrap_gpa(url, sleep=1.0):
    gpa_list = []
    # some complicated processes
    for name for list_of_names
      # some complicated processes
      gpa_list.append(gpa)
    return gpa_list
  ```

## Add figures
Using markdown format (the figure is maximized to the width of the image)  
`![fugaku](./img-resources/fugaku.png)`  
![fugaku](./img-resources/fugaku.png)

To control the width of the image, you can use HTML tag  
`<img src="./img-resources/fugaku.png" width=200>`   
<img src="./img-resources/fugaku.png" width=200>

Sometimes, figure location is outside the markdown file. You 
can use `../` to move out from the folder where your
markdown file reside.

Do not use absolute path in image source path, please use
relative path to make your markdown code portable.


## Add tables
Using markdown format

```md
| Col 1  | Col 2  |
|--------|--------|
| item a | item 1 |
| item b | item 2 |
| item c | item 3 |
```


| Col 1  | Col 2  |
|--------|--------|
| item a | item 1 |
| item b | item 2 |
| item c | item 3 |

Using HTML format

```html
<table>
  <tr>
    <td> <b>Col 1
    <td> <b>Col 2
  <tr>
    <td> item a
    <td> item 1
  <tr>
    <td> item b
    <td> item 2
  <tr>
    <td> item c
    <td> item 3
</table>
```


<table>
  <tr>
    <td> <b>Col 1
    <td> <b>Col 2
  <tr>
    <td> item a
    <td> item 1
  <tr>
    <td> item b
    <td> item 2
  <tr>
    <td> item c
    <td> item 3
</table>

# Add equations
For the complete tutorial, visit [KaTeX](https://katex.org/docs/supported)

- Inline equation `$ $`:   
  Let us mathematically model the Netflix prize problem. A _recommendation
  system_ relies on ratings of $m$ moviews previously specified by 
  $n$ users. Those are stored in a _rating_ $(n \times m)$-_matrix_ 
  $R = (r_{ij})$. Its entry $r_{ij}$ in the $i$-th row and $j$-th column
  expresses the rating of the movie $j$ by the user $i$.

- Centered equation `$$ $$`:   
  The _cosine similarity_ between the users $i$ and $\ell$ is defined as
  $$
    \operatorname{Cosine}(i, \ell)
      = \frac{
        \displaystyle\sum_{j \in M_i \cap M_\ell} 
          r_{ij} \cdot r_{\ell j}}{
          \sqrt{\displaystyle \sum_{j \in M_i \cap M_\ell} r_{ij}^2}
          \cdot \sqrt{\displaystyle \sum_{j \in M_i \cap M_\ell} r_{\ell j}^2}
        }
  $$

- Compound propositions
  $$
    (p \rightarrow q) \oplus (\neg r \rightarrow p)
  $$

  $$
    ((p \vee q) \vee r) \wedge ((\neg p \vee \neg q) \vee \neg r)
  $$