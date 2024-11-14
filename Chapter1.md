# Chapter 1. How to Create a Jupyter Book
To create a Jupyter Book there a few thing that one can manage before attemping creating the Jupyter Book.
Keep in mind that this content is for the Ubuntu OS users. You must have a github account, if you don't have please create one [here](https://github.com/login).

## Steps to Create a Jupyter Book
1. Open the terminal.
2. It is better to create a separate directory. 
3. Then use the command jupyter-book create my_jupyterbook (my_jupyterbook is the name of your Jupyter Book you can give any name you want to name your Jupyter Book).
4. Do ll and you will see my_jupyterbook. Change directory to my_jupyterbook, do ll and you will see different file, a _toc.yml file that defines the structure of your book, and any configuration you’d like in the _config.yml file.
5. You create new files. For example, if you want to include a new chapter in your book use nano Chapter and write a content of the chapter. 
6. Onece you done with it, it is important you have to include Chapter 1 in the _toc.hyml file.
7. Once everthing is done, use jupyter-book build my_jupyterbook.
8. Then see the list of the files again and there will be a file _build, go to this file then go to the html and use the commmand python -m http.server. This will give you a link, copy the link and put in internet browser, it will give take you to your book you just created. 
9. Remember every time you made any changes you have to rebuild the book using the command jupyter-book build ny_jupyterbook.




```{tableofcontents}
```
