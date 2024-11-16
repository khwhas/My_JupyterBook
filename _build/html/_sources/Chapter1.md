---
jupyter:
  jupytext:
    formats: md:myst
    text_representation:
      extension: .md
      format_name: myst
---



# Chapter 1. Jupyter Book.
In this chapter I have collected general information about **Jupyter Book**.
You will learn how you can create your first Jupyter Book, how to link it with your **Github** repository.
If you have a very basic knowledge about how to use terminal `Ubuntu terminal` and basic level of coding.

## 1.1. What is Jupyter Book.
Jupyter Book is a powerful tool for creating beautiful, publication-quality books and documents from computational material. It leverages the flexibility and interactivity of Jupyter Notebooks to combine text, code, and visualizations into a cohesive and engaging format.

**Key features and benefits of Jupyter Book:**

* **Seamless Integration of Text and Code:** Easily incorporate code cells and their outputs directly into your text, making it easier to explain and reproduce computational processes.
* **Rich Text Formatting:** Utilize Markdown syntax for clear and concise writing, and add rich formatting elements like headings, lists, and images.
* **Interactive Exploration:** Enable readers to experiment with code directly in the browser, fostering deeper understanding and engagement.
* **Version Control and Collaboration:** Work seamlessly with version control systems like Git to manage your book's content and collaborate with others.
* **Customizable Output Formats:** Generate various output formats, including HTML, PDF, and ePub, to suit different needs and preferences.
* **Extensibility:** Leverage a growing ecosystem of extensions and plugins to tailor Jupyter Book to your specific requirements.

**Common Use Cases:**

* **Academic Textbooks and Research Papers:** Create interactive textbooks and research papers that allow readers to explore data and code.
* **Technical Documentation:** Develop clear and concise technical documentation with interactive code examples and visualizations.
* **Data Science Tutorials and Workshops:** Share data science knowledge and best practices through interactive tutorials and workshops.
* **Personal Note-Taking and Knowledge Management:** Organize and share your knowledge in a structured and interactive format.

By combining the best of both worlds, Jupyter Book empowers you to create compelling and informative documents that bridge the gap between theory and practice. 


To create a **Jupyter Book** there a few thing that one can manage before attemping creating the Jupyter Book.
Keep in mind that this content is for the Ubuntu OS users. You must have a github account, if you don't have please create one [here](https://github.com/login).


## 1.2. How to  Create a Jupyter Book.

Keep in mind that this content is for the Ubuntu OS users. You must have a github account, if you don't have please click [here](https://github.com/login).
Follow the follwing steps and I hope you will be able to creat your first **Jupyter Book**. 

1. Open the terminal.

```
ctrl+alt+T
```

2. It is better to create a separate directory. In the present case it is `Jupyter_Book`.

```
mkdir Jupyter_Book
```

```{note}
It is better to create your Jupyter Book in a separate ditectory so that you can track it easily.
```

3. Creat a Jupyter Book in this directory.

```
cd Desektop/Jupyter_Book
```

```
jupyter-book create My_JupyterBook
```
`My_JupyterBook` is the name of my Jupyter Book, you can give any name you want to name your Jupyter Book.

4. `ll` all see file in `My_JupyterBook`. Change directory to `My_JupyterBook`, again do `ll` and you will see different file for exapmle, `_toc.yml` file that defines the structure of your book, and any configuration you’d like in the `_config.yml` file.

5. You can create new files. For example, if you want to include a new chapter in your book use nano Chapter1 and write a content of the chapter.

```
nano Chapter1.md
```
 
 A blank terminal window will open where you can write the contant of the Chapter1.
 
```
# Chapter 1. Jupyter Book.

Content of this chapter.
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
jupyter-book build My_JupyterBook
```
```{warning}
Before running the above command it is important you go one directory back. For Exapmle, I have created the `My_JupyterBook` director on `Desktop/Jupyter_Book`, so I will go one directory back (that is in the Jupyter_Book) and then run the above command.
```

```{note}
After making any new changes in the `Chapter1.md` file it is important to rebuild the book.
```
To rebuild it the same command `jupyter-book build my_jupyterbook`

8. Onece the process is done, scroll up and look for any kind of **Warnings** and **Error**.
At the very last line there will be a link beginning with `https` copy that link and past in the internet broweser and you will be directed to your Jupyter Book. 


# 1.2. Connecting your Jupyter Book with the Github repository. 

1. Creat a new repository without initializing it with README, you want your repository public or private is upto you.
2. It is imprtant to note that when you are copy the link to your repository you have to select the `SSH` the `HTTPS`. Becaus from 2021 Github is not accepting to access your repository with your account password ay more. You can still can but you will have to creat a key for it and is bit fustrating, at least for me. 
3. Cofirm you are in a right directory in your local computer. 
4. Initialize the repository in the directory that contain all the files of the your Jupyter Book.

```
git init
```

```
ls -a
```

You will see all the files in the directory something like 

```
(base) ~/Desktop/Jupyter_Book/My_JupyterBook$ ll
total 92
drwxrwxr-x 5 hassan hassan 4096 Nov 16 16:33 ./
drwxrwxr-x 3 hassan hassan 4096 Nov 14 21:08 ../
drwxrwxr-x 5 hassan hassan 4096 Nov 16 03:23 _build/
-rw-rw-r-- 1 hassan hassan 5724 Nov 16 04:42 Chapter1.md
-rw-rw-r-- 1 hassan hassan 1024 Nov 16 16:33 .Chapter1.md.swp
-rw-rw-r-- 1 hassan hassan 1903 Nov 16 01:36 Chapter2.ipynb
-rw-rw-r-- 1 hassan hassan 1012 Nov 16 03:57 Chapter2.md
-rw-rw-r-- 1 hassan hassan  237 Nov 15 00:56 Chapter3.md
-rw-rw-r-- 1 hassan hassan 1192 Nov 15 06:42 _config.yml
drwxrwxr-x 8 hassan hassan 4096 Nov 16 01:41 .git/
-rw-rw-r-- 1 hassan hassan  178 Nov 14 16:55 intro.md
drwxrwxr-x 2 hassan hassan 4096 Nov 16 01:32 .ipynb_checkpoints/
-rw-rw-r-- 1 hassan hassan 9854 Nov 14 16:55 logo.png
-rw-rw-r-- 1 hassan hassan 1898 Nov 14 16:55 markdown.md
-rw-rw-r-- 1 hassan hassan 1787 Nov 14 16:55 markdown-notebooks.md
-rw-rw-r-- 1 hassan hassan 3378 Nov 14 16:55 notebooks.ipynb
-rw-rw-r-- 1 hassan hassan 5524 Nov 14 20:21 references.bib
-rw-rw-r-- 1 hassan hassan   30 Nov 14 16:55 requirements.txt
-rw-rw-r-- 1 hassan hassan  386 Nov 15 00:57 _toc.yml
```

5. Add the remote repository: Use the `SSH` remote URL of your repository of the Github

```
git remote add origin <you github SSH URL>
```
6. Add and commit your files: Add all the files and make an initinal commit

```
git add .
git commit -m "Initial commit"
```

```{note}
It is recommanded that you write a comment when you are commiting. Since it is my first initial commit so I named as `"Initial commit"`.
```

7. Push to Github: Now is the time to push all the file to your Github repository. Push your file to the main branch on Github.

```
git push -u origin main
```

After runing **point.6** if you encounter an error `"sct refspec main does not match"`. It is usually happens if there isn't a branch named **main** in your repositiry yet. This can occour because Git uses master as a default branch in some steps.
You can resolve this by either creating a main branch or pushing to master instead. Here are the two options:

## Option 1: Creat a main Branch.
1. Creat a main branch and switch to it.

```
git checkout -b main 
```

2. Push to Githib on the main branch:

```
git push -u origin main
```

## Option 2: Push to the Default master Branch.
1. If you prefer to use the master branch instead. Commit to your master.

```
git push -u origin master
```

Go to your repository on Github, refresh the page and you will be able to see all the files on your git repository. 


# 1.3. Converting the `.md` file to `.ipynb` file.

```{note}
Before conversion the `.md` file to `.ipynb` file. Make sure you have **jupytertext**. You can check by using `jupytext --version` or if you don't have use `pip install jupytext`. Incase you want to **upgrade** it, use `pip install jupytext --upgrade`

```

You can convert `.md` file to `.ipynb`. It is more easy to work in **Jupyter notebook**. Espically for the coding part.
To conver the `.md` file, add the follwoing lines in it. For instance, I convert **Chapter2.md** file. There I edit my Chapter2.md file added the following lines.

```
---
jupyter:
  jupytext:
    formats: md:percent,ipynb
    text_representation:
      extension: .md
      format_name: myst
    paired_paths: ['Chapter2.md', 'Chapter2.ipynb']
---
```

Make sure the .md and the respective .ipnyb file exists in the same directory, In my case it is like as follows:

```
(base) ~/Desktop/Jupyter_Book/My_JupyterBook$ ll
total 92
drwxrwxr-x 5 hassan hassan 4096 Nov 16 16:33 ./
drwxrwxr-x 3 hassan hassan 4096 Nov 14 21:08 ../
drwxrwxr-x 5 hassan hassan 4096 Nov 16 03:23 _build/
-rw-rw-r-- 1 hassan hassan 5724 Nov 16 04:42 Chapter1.md
-rw-rw-r-- 1 hassan hassan 1024 Nov 16 16:33 .Chapter1.md.swp
-rw-rw-r-- 1 hassan hassan 1903 Nov 16 01:36 Chapter2.ipynb
-rw-rw-r-- 1 hassan hassan 1012 Nov 16 03:57 Chapter2.md
-rw-rw-r-- 1 hassan hassan  237 Nov 15 00:56 Chapter3.md
-rw-rw-r-- 1 hassan hassan 1192 Nov 15 06:42 _config.yml
drwxrwxr-x 8 hassan hassan 4096 Nov 16 01:41 .git/
-rw-rw-r-- 1 hassan hassan  178 Nov 14 16:55 intro.md
drwxrwxr-x 2 hassan hassan 4096 Nov 16 01:32 .ipynb_checkpoints/
-rw-rw-r-- 1 hassan hassan 9854 Nov 14 16:55 logo.png
-rw-rw-r-- 1 hassan hassan 1898 Nov 14 16:55 markdown.md
-rw-rw-r-- 1 hassan hassan 1787 Nov 14 16:55 markdown-notebooks.md
-rw-rw-r-- 1 hassan hassan 3378 Nov 14 16:55 notebooks.ipynb
-rw-rw-r-- 1 hassan hassan 5524 Nov 14 20:21 references.bib
-rw-rw-r-- 1 hassan hassan   30 Nov 14 16:55 requirements.txt
-rw-rw-r-- 1 hassan hassan  386 Nov 15 00:57 _toc.yml
(base) ~/Desktop/Jupyter_Book/My_JupyterBook$
```
You can cee `Chapter2.md` and the corrsponding `Chapter2.ipynb` in the same directory.

```
jupytext --set-formats myst,ipynb Chapter2.md
```
This will set the myst format for the Markdown file and pair it with the `.ipynb` notebook.

Finally you can sync the `.md` file with the `.ipynb` file.

```
jupytext --sync Chapter2.md
```

You can open the `.ipynb` file either in `jupyter notebook` or `jupyter lab`. If you added some code in the `.ipynb` let's say in the notebook. You can use the same above `jupyter --sync <filename.md>`. It will update all the changes in the `.md` file.







```markdown
This this the first markdown.
```
