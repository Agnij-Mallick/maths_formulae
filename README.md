# A Book of High School and Engineering and Engineering Common Core Mathematical Formulae
I started this book in 2015 to keep track of new formulas I encountered while solving my high school mathematics problems. What started as a small spiral notebook soon needed more pages as I kept adding to it over the next 5 years.

In December of 2020, I realised that it is impossible to maintain this notebook in a physical form anymore. Over 5 years, after noting down formulae as I came across them, the order of chapters became more haphazard. Differential equations was before indefinite integration, boolean algebra appeared in-between two chapters of geometry and a host of other small bits that had to be placed away from other relevant formulae because I was out of space.

So I took it upon myself to, in a way, restore my notebook through digitization. This served three purposes:
1. I was able to reorganise the book into a more coherent order,
2. Make edits less messy than striking out old sections in a notebook and rewriting them, and
3. I would be able to share my work with the world.

I am making the code of this book open-source so that the greater mathematical community can add and improve to it. I am also making this book open-sourced so that anybody, even if they are not familiar with LaTeX, can download the PDF file and use it. I am not profiting from this book and I expect the same from the users of this code.

**For the students who come across this book:** it is not a substitute to your textbook. It is a cheatsheet that you can refer to quickly instead of going through the pages of textbook before you come across the formula you need to solve your problem or use it to revise the night before your exams.

In the subsequent sections I will describe the LaTeX code and the organisation of the files within this project. If you only want access to the book, I would suggest downloading the *main.pdf* file.

## Page Size and Border
The page size and borders have been optimised for an Amazon Kindle 6" screen. Through multiple trials, I have found the B5 paper to be the best fit for the Kindle Screen. The document options *openany* and *oneside* have been used to make this book better suited for digital use.

These settings should also work well with any computer screen.

If you need to change it to suit your needs, adjust line 12 in the *main.tex* file.

## Orgnisation of the Code
The file *main.tex* contains the packages and links to the *subfiles* used in the book. 

Each chapter is a *sublife* which is organised under the respective subtopics in maths. Each subtopic has its own separate sub-directory within the **chapters** directory.

## Packages, Environment, and Code
### Packages
All unnecessary packages from the original version have been removed. They are added as and when they are required. Please ensure that existing packages suffice before adding any new packages.

### Environments
For equations, the *align* environment has been used throughout the new document. If you want to merge your changed into this the **main** branch of the book, I would request that you maintain this practice in your code as well.

All new environments start in a new line.
```latex
\begin{align}
v =
    \begin{vmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    \end{vmatrix}
\end{align}
```

Please punctuate your code with spaces.
```latex
\begin{align}
    c = a + b \\
    e = c + d
\end{align}
```
Instead of
```latex
\begin{align}
    c=a+b\\
    e=c+d
\end{align}
```
This, in my opinion, improves the readability of the code and allows easier rectifications when needed.

### Other Practices
I would request all new code to be properly indented with *TAB*.

If you must insist on using spaces for indentation, like a sociopath, use 4 spaces for indentation.

## Acknowledgement
The original handwritten notebook was inspired by Dr. Rabindranath Das, who was my maths tutor from 2015 to 2017. He guided me through preparing and maintaining the original version of this book, when he would spend 3 hours each Wednesday tutoring my high school self in maths.

Also, a major shoutout to the kind people of [r/LaTeX](https://www.reddit.com/r/LaTeX/) Subreddit whose input was vital to the reorganization and cleanup of the original monolithic code.
