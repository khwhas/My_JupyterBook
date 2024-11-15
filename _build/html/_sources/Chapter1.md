---
jupyter:
  jupytext:
    formats: md:myst
    text_representation:
      extension: .md
      format_name: myst
---



# Chapter 1. How to Create a Jupyter Book
To create a **Jupyter Book** there a few thing that one can manage before attemping creating the Jupyter Book.
Keep in mind that this content is for the Ubuntu OS users. You must have a github account, if you don't have please create one [here](https://github.com/login).

## Steps to Create a Jupyter Book
1. Open the terminal.

```
ctrl+alt+T
```

2. It is better to create a separate directory. In the present case it is `my_jupyterbook`.


mkdir my_jupyterbook

```{note}
It is better to create your Jupyter Book in a separate ditectory so that you can track it easily.
```

3. Creat a Jupyter Book in this directory.

jupyter-book create my_jupyterbook


`my_jupyterbook` is the name of your Jupyter Book you can give any name you want to name your Jupyter Book.
4. `ll` all see file in `my_jupyterbook`. Change directory to `my_jupyterbook`, again do `ll` and you will see different file for exapmle, `_toc.yml` file that defines the structure of your book, and any configuration you’d like in the `_config.yml` file.
5. You create new files. For example, if you want to include a new chapter in your book use nano Chapter1 and write a content of the chapter.


nano Chapter1.md

 
 A blank terminal window will open where you can write the contant of the Chapter1.
 
```
# Chapter 1. Introduction
```
 
```{note}
- The `#` symbol creates a main chapter heading.
- The `##` symbols create subsections within each chapter.
```
 
6. Onece you done writing the contents of Chapter1, save it it. Next, it is important you have to include Chapter 1 in the `_toc.yml file`. The output can be like as follow.

```
# Table of contents
# Learn more at https://jupyterbook.org/customize/toc.html

format: jb-book
root: intro
chapters:
- file: markdown
- file: notebooks
- file: markdown-notebooks
- file: Chapter1   #this is the new chapter added in the Jupyter Book
```

7. Once everthing is done, it is important to biuld the jupyter Book.

```
jupyter-book build my_jupyterbook
```
```{warning}
Before running the above command it is important you go one directory back. For Exapmle, you have created the `my_jupyterbook` director on `Desktop`, so you will go one directory back (that is in the Desktop) and then run the above command.
```

```{note}
After making any new changes in the `Chapter1.md` file it is important to rebuild the book.
```
To rebuild it the same command `jupyter-book build my_jupyterbook`

8. Go to the `build my_jupyterbook` and do 'll' and you will see the list of the files again and there will be a file `_build`, go to this directory. This directory will have three files, `cd` to the `html` and run the following command

```
python -m http.server
```

This will give you a link, copy the link and put in internet browser and it will direct to your book you just created. 

Another is to copy to use the following command

```
file:///home/hassan/Desktop/Jupyter_Book/My_JupyterBook/_build/html/index.html
```

### Section for Markdown

```markdown
This this the first markdown.
```

