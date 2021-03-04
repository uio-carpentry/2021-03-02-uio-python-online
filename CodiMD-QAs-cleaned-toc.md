---
permalink: /CodiMD-QAs-cleaned-toc/
---

Carpentry@UiO Plotting and Programming in Python
===

<div style="color: #31708f; background-color: #d9edf7; border-color=#bce8f1; padding: 15px; margin-bottom: 20px; border: 1px solid transparent; border-radius: 4px;">
- Lesson material of this workshop: [Plotting and programming in Python](http://swcarpentry.github.io/python-novice-gapminder/index.html), episodes 1-16.
- Please complete [The Carpentries Post-workshop survey](https://carpentries.typeform.com/to/UgVdRQ?slug=2021-03-02-uio-python-online) as well!
</div>

# Table of Contents
- [Carpentry@UiO Plotting and Programming in Python](#carpentryuio-plotting-and-programming-in-python)
- [Table of Contents](#table-of-contents)
- [Day 1](#day-1)
  - [Questions in Ep. 1-3](#questions-in-ep-1-3)
  - [Exercises part 1](#exercises-part-1)
    - [Ep. 2 Variables and Assignment](#ep-2-variables-and-assignment)
      - [Predicting Values](#predicting-values)
      - [Slicing practice](#slicing-practice)
    - [Ep. 3 Data Types and Type Conversion](#ep-3-data-types-and-type-conversion)
      - [Fractions](#fractions)
      - [Automatic Type Conversion](#automatic-type-conversion)
      - [Arithmetic with Different Types](#arithmetic-with-different-types)
  - [Questions in Ep. 4-6](#questions-in-ep-4-6)
  - [Exercises part 2 until 10:50](#exercises-part-2-until-1050)
      - [Spot the Difference](#spot-the-difference)
      - [Jigsaw Puzzle (Parson’s Problem) Programming Example](#jigsaw-puzzle-parsons-problem-programming-example)
      - [When is Help Available?](#when-is-help-available)
      - [There are Many Ways To Import Libraries!](#there-are-many-ways-to-import-libraries)
  - [Questions in Ep. 7-8](#questions-in-ep-7-8)
  - [Exercises part 3: until 11:50](#exercises-part-3-until-1150)
    - [Ep. 7 Reading Tabular Data into DataFrames](#ep-7-reading-tabular-data-into-dataframes)
      - [Reading Other Data](#reading-other-data)
    - [Ep. 8 Pandas DataFrames](#ep-8-pandas-dataframes)
      - [Selection of Individual Values](#selection-of-individual-values)
      - [Reconstructing Data](#reconstructing-data)
  - [Questions and comments at the end of Day 1](#questions-and-comments-at-the-end-of-day-1)
- [Day 2](#day-2)
  - [Icebreaker questions and answers](#icebreaker-questions-and-answers)
  - [Exercises part 1](#exercises-part-1-1)
    - [Ep. 9 Plotting](#ep-9-plotting)
      - [Minima and Maxima](#minima-and-maxima)
      - [(Extra: Correlations)](#extra-correlations)
    - [Ep. 11 Lists](#ep-11-lists)
      - [Fill in the Blanks](#fill-in-the-blanks)
      - [Working With the End](#working-with-the-end)
      - [Slice Bounds](#slice-bounds)
  - [Questions in ep. 9-11 (Plotting/Lists)](#questions-in-ep-9-11-plottinglists)
  - [Questions in ep. 12-14 (For Loops/Conditionals/Looping Over Data Sets)](#questions-in-ep-12-14-for-loopsconditionalslooping-over-data-sets)
  - [Exercises part 2 until 10:50](#exercises-part-2-until-1050-1)
    - [Here's some bonus questions if you've done them all:](#heres-some-bonus-questions-if-youve-done-them-all)
  - [Questions in Ep. 16 (Writing Functions)](#questions-in-ep-16-writing-functions)
  - [Exercises part 3 Until 11:45](#exercises-part-3-until-1145)
    - [Ep. 16 Writing Functions](#ep-16-writing-functions)
      - [Encapsulation](#encapsulation)
      - [Find the First](#find-the-first)
      - [Calling by Name](#calling-by-name)
      - [(extra: Encapsulating Data Analysis)](#extra-encapsulating-data-analysis)
  - [Questions at the end of Day 2](#questions-at-the-end-of-day-2)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


# Day 1

## Questions in Ep. 1-3 
(Example of questions and answers)

- Q. How to run the code?
    - A. Press `shift+Enter` 
- Q. What is the shortcut for inserting a new line?
    - A. Press `a` to insert a line above, `b` 
    
(End of example of questions and answers)
    
- Q. Can you say a bit about the characters that are not on the keyboard?
    - A: this depends on the operating system. What operating system are you using and what keys are you wondering about? 
    - A2: On Windows, the special character `~` is found  between `enter` and `å` on a Norwegian keyboard.

- Q. I do no access my desktop folder
    - A: On Mac and Linux's terminal, `cd ~/Desktop` for the absolute path or move through your folder using `pwd` to know where you are (your path) and use `cd my_path_to_my_folder`
    - A2: It depends on your OS. Are you on Linux, Mac or Windows? -> windows
        - So your problem is to changed folder then? -> yes. 
        - Do you manage to open a terminal? -> yes I have anaconda open and my folder extracted in the desktop
    - A3: If you type the command `pwd` you will see which folder you are currently in. What does it say? ->'pwd' is not recognized as an internal or external command, operable program or batch file
        - Im in C:\
            - A: I'm sorry. I was mixing windows and linux command (I'm on linux). Try `cd` which should be the equivalent for you. The command `$ cd Desktop` should change your directory.
    - A4: For all the cd error, make sure that you are in your terminal not a in the python console

    - A5: If you're on a computer managed by UiO, try to run the command "cd M:\pc\Desktop". This only works in Anaconda PowerShell Prompt, not the other Anaconda Prompt.
        - "cd M:/pc/Desktop" (regular slashes) works fine on git bash as well (just checked it)
    - A6: If you get an error on that, try to find where your desktop is: Open (double-click) the `python-novice-gapminder-data`  folder, or `data` if you have that, and Click on the address bar. Copy that text and paste it after "cd". If you only had `data`, remove `\data` off the end, to go to the desktop. Use that location, e.g. for me it is: `cd C:\Users\(username)\Desktop\python-novice-gapminder-data` 
    ![](https://codimd.carpentries.org/uploads/upload_20bb86cede70a5639292ad2250f2ca72.png)
    - A7: One problem we had was with navigating to the desktop on a UiO laptop. It turns out that the apparent desktop area is actually under onedrive. I don't know exactly how that works because I'm not on a UiO laptop right now. Anyway the solution was to right-click-then-copy the unzipped python-... folder, then navigate to M:/pc/Desktop and paste it there. After that one can cd to the folder and move on. I guess the point for the instruction is that "copy the folder to your desktop" is not going to work for people with this setup because what they see as desktop is neither ~/Desktop nor M:\pc\Desktop 
        - > [NB! the comment above is moved from original place to more relevant placeoriginal place]

- Q. running windows, get error messages for all the cd desktop, skrivebord command
    - A: **for now, it does not matter too much where you start Jupyter Lab, we can fix this in first exercise session**

- Q. My jupyter notebook keeps becoming unresponsive for a few moments. I think it may have to do with git refreshing or saving, but I am not sure. It gets rather annoying as it interrupts typing a lot. Any ideas?
    - A: Is the kernel maybe dying?
        - Doesn't really look like it. Python is idle during the freezes, and comes back online after a few moments, no problems there so far.
    - A2: One thing to try is to save the notebook, and choose 'Kernel' from the menus and then 'Restart'
        - trying that now... not much change, still freezes occasionally (with "git: refreshing" at the bottom)
    - A3: next thing to try is saving, closing the JupyterLab, interrupting what is going in the terminal, and starting JupyterLab again
        - trying that now... not much change here either. I'll just grin and bear it, it's OK.


## Exercises part 1

### Ep. 2 Variables and Assignment 

#### Predicting Values
![](https://codimd.carpentries.org/uploads/upload_cac5205b3a4fcbeb54a7d042b9a1cedb.png)
#### Slicing practice
![](https://codimd.carpentries.org/uploads/upload_a3df99c91614c75aaa618269a2bd0fa9.png)

### Ep. 3 Data Types and Type Conversion

#### Fractions
![](https://codimd.carpentries.org/uploads/upload_b5be54793fee939c19eab7cfd1d05ff8.png)

#### Automatic Type Conversion
![](https://codimd.carpentries.org/uploads/upload_1c3403f2c1cb89a73084b4eae85e5712.png)

#### Arithmetic with Different Types
![](https://codimd.carpentries.org/uploads/upload_25be5140f227a6342627c1de52a3efe7.png)

## Questions in Ep. 4-6
- Q: in the last exercise why does "2.0 * second" gives an error?
    - A: `second` is a string, and you can do `2 * second` (try this!) but Python will not allow you to multiply a float with a string
- Q: Is there a difference between using ''or " " for defining a string?
    - A: no, but you canot mix them!

- Q: slicing in Python is confusing to me. E.g., atom_name[1:3] results in 2 letters only, the second and the third. Can you try and explain this so it makes more sense please? :-) 
    - A: maybe this image can help: ![](https://codimd.carpentries.org/uploads/upload_685bba6f7ec9f9cf44a8e0fb98403521.png) (from https://www.geeksforgeeks.org/python-list/). This kind of image was what helped me understand it originally. One way to think about this is that the index points to the boundary before the item and not the item itself. If you look at the image (index numbers above the string) you will see that between 1 and 3 there are indeed two letters.
    - A: that is because slicing works from the first index, to, but _not_ including the second index, so from 1 to 3 (not including). This also means the length of the slice is the difference between the indexes (3 - 1 = 2).
    - A: By writing `print(atom_name[1:])`  you would print from the second index (the latter a) to the end of the string 
        
- Q: What is the difference between single quotes and double quotes, please? I think, print() works with both.
    - A: both are fine but you cannot mix them!
    - A: if you want a single quote to appear in the output, use double quotes around it: `print("do 'it' like this")` (or the other way around)

## Exercises part 2 until 10:50

#### Spot the Difference
![](https://codimd.carpentries.org/uploads/upload_3532e6b307a8fe2e20fff27f99323429.png)

#### Jigsaw Puzzle (Parson’s Problem) Programming Example
![](https://codimd.carpentries.org/uploads/upload_e1f088bc2af268c215553e023a5948e0.png)

#### When is Help Available?
![](https://codimd.carpentries.org/uploads/upload_81cd6111c61b9c34d08a0ae530f1bca6.png)

#### There are Many Ways To Import Libraries!
![](https://codimd.carpentries.org/uploads/upload_11b8256a85fc1eacae6df68cfc7bc40a.png)


- Q: How is the max function working? 
    - A: It chooses the largest value. If it is a letter, it chooses the highest letter value.
    - A2: See [here](https://stackoverflow.com/questions/20463204/how-does-the-max-function-work-on-list-of-strings-in-python) for a Stack-answer

<div style="color: #31708f; background-color: #d9edf7; border-color=#bce8f1; padding: 15px; margin-bottom: 20px; border: 1px solid transparent; border-radius: 4px;">
For the next session, please down load [Gapminder dataset](href=https://swcarpentry.github.io/python-novice-gapminder/files/python-novice-gapminder-data.zip), unzip it and have it on the desktop in "data" folder<br>
![a handwritten circle on data folder shown in the Jupyter Lab left-side menu](https://codimd.carpentries.org/uploads/upload_b47814ded20b514eebc7472ddd07fc2f.png)
</div>

- Q: I was a bit slow in the last exercise and can't get the Jigsaw Puzzle code to work. I get an error for the line there after I start using the `random.randrange` line saying I have an invalid literal for int() with base 10
    - A: Do you get an error on ___ = len(bases) ?
        - I already get an error for ___ = random.randrange(n_bases)
            - This indicates that n_bases is not an integer.
            - You have to change the orders of the lines, so you can define n_bases as len(bases). Then you can use it in the line with random.randrange. Does that make sense?
                - yes, thanks! with the n_bases = len line first i make the string to an integer and allow the second line to randomize that, correct?
                    - The first line gets the length of the string as an integer only, it doesn't change the string itself.
                        - Great, yes that makes sense! Thanks!

## Questions in Ep. 7-8

- Q: How could I see the sidebar in Jupyter? I really don't see it. Just using !ls to check.
    - A: (Sorry to write on top) Click on the Folder icon on the left. Does that work?
        - I dont even see this icon. I started it in the terminal just with jupyter-notebook
    - A2: Jupyter notebook is different from jupyter lab. Notebook doesn't have the sidebar. It's good you found an alternative, !ls.
        - Just installed jupyter-lab in my conda env. Sorry. Thanks for the help :-)

- Q: Is there any similar to ? in R or help in STATA for python?
    - A: You can always use `help(something)` in python -- But Jupyter actually has ?`something`, so that works! For example `?print`. 
        - Thanks!

- Q: my pandas package won't load (import). I've tried to pip install it again, but it still doesn't load
    - A: You are in Jupyter note, installed Anaconda3, right? I believe that mixing up pip and conda is causing a problem.. If you type in the jupyter note `conda list`, and if you cannot find `pandas`, please write back here.
        - The pandas package is on the conda list  
    - A2: I just had the same problem. I installed in a terminal pandas into the conda env, and re-executed the cell with import pandas as pd and it worked.
        - Thanks for this advice. This may work better?
            - tried to conda install, the package is there, but it does not load in jupyter. the conda install also require some permissions to access the anaconda folder
                - I cannot answer the permission question, but I did 'conda install pandas'. In worst case, save your notebook. Restart jupyter-lab after installing pandas? <- this is the  way:)
                    - ok, i'll try to restart (but later:)
    - A3: When you start Jupyter Lab, it doesn't use the current conda environment by default, it uses the `base` environment. Have you created a new conda environment? 
        - no, how do I do that?  
            - It's easier if you haven't done that, so never mind.

- Q: In Jupyter, there are no tab that helps guesssing the function or variable as far as I know. Is that correct?
  - A: It only works for some things. If you have already defined a variable and run a cell, then it will auto-complete the name in another cell. It can also auto-complete file names. And functions. -> 👍

## Exercises part 3: until 11:50

### Ep. 7 Reading Tabular Data into DataFrames

#### Reading Other Data
![](https://codimd.carpentries.org/uploads/upload_95b14b38537fc114b86520fd9d2bb762.png)

### Ep. 8 Pandas DataFrames
#### Selection of Individual Values
![](https://codimd.carpentries.org/uploads/upload_9c21f0bb1a47cd7864bb65edcf15a4a4.png)

#### Reconstructing Data
![](https://codimd.carpentries.org/uploads/upload_62ad52717f7fdf24e22fffcbc599bf1e.png)

## Questions and comments at the end of Day 1
- Q: What is the difference between Jupyter lab and jupyter notebook?
     - A: Jupyter Lab is a newer project, made to replace jupyter notebook. Jupyter lab can have multiple noteboks open, and other items like scripts and a file browser. Jupyter notebook can only show a single notebook at a time. Both work similarly in the notebook, and you can use the one you prefer.

- Q: how did you make this page, is there something similar to Rmarkdown in phyton
??
    - A: The Carpentries organisation has set up a server that runs CodiMD: https://github.com/hackmdio/codimd . That's the one we're using.
        - sound good! I was refering to this one http://swcarpentry.github.io/python-novice-gapminder/index.html
is the same code? Thanks
            - This is set up using Github Pages. It requires some script to run and make html pages from the code that's in the github repository. It uses a "static site generator".
                - thanks

- Q: I wasnt able to run the help command as recommends in jupyter.
    - -A: Have you initalised the variable or the library? 
        - I just include pandas and the other commands
             - `import pandas as pd` `help(pd)`  
                - it works! thanks
                     - Nice! Thank you for the feedback!
    
- Advice to organizers: We had problems with Jupiter Lab and few had it installed and the solution was just to use a notebook or a python interpreter. A windows tutorial for installing Jupiter Lab with conda would be nice addition to the online material
    - Thanks for the feedback. Did you see the setup instructions on the course website? https://uio-carpentry.github.io/2021-03-02-uio-python-online/ That just shows anaconda, but by default Anaconda will also install Jupyter Lab and all the necessary Python packages. We will keep in mind that using notebook directly, or python interpreter can help, thanks.
        - The people on Windows could not get their Jupyter lab running and I do believe that they have problems running a conda environment or lack an installed Jupyter Lab. Jupyter notebook was installed with conda it seems. In group 9, only the helper had the Lab running. 
          - Excellent point. We should make sure the setup instructions include Jupyter Lab as a separate item. Some people may have older Anaconda without Jupyter lab. 👍  
          - I've added an issue on Github (https://github.com/carpentries/workshop-template/issues/731). It's a bit complicated because there are two Python lessons in Software Carpentry, but only one set of instructions


# Day 2

## Icebreaker questions and answers

**What do you think is the best about Day1 of this workshop?**

- That Jupyter notebook tells where the error is.+1
- Easy to follow exercises.
- Introduction to software and language
- Interesting discussion/questions
- Very well organized
- Well structured
- Great to learn something new from very competent instructors/helpers
- Small group thing
- Lex
- the link you provided in the end was very useful
- lots of content
Good answers to questions
-Friendly environment


**Where do you want to go first when we can go abroad without any quarantine?**

- Home country +9
- In a warm place +
- visit my parents +3
- To visit friends and family! +2
- Go hiking at Madagascar!
- Mars +1
- Visit friends and family in the UK, US 
- Go to the Netherlands +1
- USA
- Lars Lerin's gallery in Sweden


## Exercises part 1

### Ep. 9 Plotting 

#### Minima and Maxima
![](https://codimd.carpentries.org/uploads/upload_5bc60a040072a3eae0eb4818ba2d9c6a.png)

#### (Extra: Correlations)
![](https://codimd.carpentries.org/uploads/upload_01650cd5a7cc3ba6e7866ae439288b5d.png)
![](https://codimd.carpentries.org/uploads/upload_8b774ecb4ab2b3e431e5bde88d36e1e0.png)

### Ep. 11 Lists

#### Fill in the Blanks
![](https://codimd.carpentries.org/uploads/upload_396f99ab4a90dac4e7479aa564634e57.png)

#### Working With the End
![](https://codimd.carpentries.org/uploads/upload_243b71fd1ab9d9e358c1336d023d054e.png)

#### Slice Bounds
![](https://codimd.carpentries.org/uploads/upload_485e52726f6d34437a0d35d0bc856cb9.png)



## Questions in ep. 9-11 (Plotting/Lists)
**Please write questions below**


- Q: Yes, I wonder something. Exercise: `element[-1:3]` This confused me. -1 is the last element.
    - A: If you try element[-1:3:-1] this is a valid index sequence so you get what you expect (i.e., elements -1, -2, and -3: 'mui'); there is no index between -1 and 3, so you get nothing.
        - What does the 3 mean in your sequence `element[-1:3:-1]`, please?
            - 3 is the position right before the 3rd element (index-3 element, actually the 4th by regular counting); -1 is the position right before the last element; and the third argument (+1 by default) is the stepping ; reposting the graph here: ![](https://codimd.carpentries.org/uploads/upload_685bba6f7ec9f9cf44a8e0fb98403521.png) (from https://www.geeksforgeeks.org/python-list/)
        - I was not aware I could mix negative and positive indices.
            - Sure you can. Try element[-4:4] (it gives you 'h'). These indices are just positions in the list or string, it does not matter if they are specified with reference to the beginning or the end. Once you have two points, then they are stepped through by the third argument and then you get the content of the result. (I should probably add here that it gets tricky with negative step, so you should be careful; a lot of the gory details are shown for example here: 
                - element[-4:4] this is also confusing for me, because in both directions, h is the fourth letter. Upps, wrong, sorry.
                - element is 'lithium' 0 is before 'l', 1 is before 'i', 2 is before 't', 3 is before 'h', 4 is before 'i' (hence after 'h'); -1 is before 'm', -2 is before 'u', -3 is before 'i', -4 is before 'h'. So [-4:4] (implied [-4:4:1]) means "From before 'h' to after 'h' with a step of 1" so you get 'h'
            - Just to clarify, right of -1 it starts with 0, 1, 2 etc.?
        - A better example is `element[-6:5]`, you take the element `len(element)-6=1` which is `element[1]='i'` up to `element[5]='u'`.The final result is `element[-6:5]='ithi'`
        - For info, to take the reverse of an *array* use `::-1`  see the difference between `pressures[::-1]` and `pressure[::1]`.         
            - `element[-6:5]` --> Understood! I start with negative index and finish with a postive index.

- Q: can one slice every second element?
    - A: yes. `elements[start:stop:step]`. For example `elements[1:5:2]` will take every second element
    - A2: `elements[::2]` also works for the entire string

- Q: can we get the figure in vector format
    - A:`.eps` and `.svg` work. Hope that helps. More complex answers [here](https://stackoverflow.com/questions/9266150/matplotlib-generating-vector-plot).

- Q: I had in my room the question what happens when I import only matplotlib and not matplotlib.pyplot. This means I would import more functions? And I would need to write something like  pyplot.plot is used as new plot command?
    - A: yes, you would import more (not sure what, tough) and have to use `matplotlib.pyplot.plot(x,y)` instead of `plt.plot(x,y)`
        - Thank you!  

## Questions in ep. 12-14 (For Loops/Conditionals/Looping Over Data Sets)
**Please write questions below**

- Q: sorry, I missed it. Could you have several "else", or you need to use "elif", and have only one "else"?
    - A: One else and multiple elif.

## Exercises part 2 until 10:50
**If you need more time, please write here!**

10 more minutes please?

![](https://codimd.carpentries.org/uploads/upload_8adfa4471957715281dd816df9d137c0.png)


![](https://codimd.carpentries.org/uploads/upload_fd3d78ead627436a79a72373fd966caa.png)

![](https://codimd.carpentries.org/uploads/upload_b7562bec17118d9caeea99fc39c7fd42.png)

![](https://codimd.carpentries.org/uploads/upload_d193d4b57c9255d2a4a7c47e07b7beed.png)

- Room 7 are doing fine. Some discussions and finally we did not finish Exe. 4.
- Room 11: We managed the first 3 exercises together and I lost one participant due to comuter problems.

### Here's some bonus questions if you've done them all:

![](https://codimd.carpentries.org/uploads/upload_390e53648f699e5446c4cfaf1c5f291c.png)

- The answer for the last "bonus" exercise is a bit difficult. Solution is `fewest = float('Inf')` !! But you could have used `fewest = 999999`.

- Q: What is total += number short for?
  - A: It's the same as `total = total + number`
  - A2: Short hand for lazy programmers ;)

- Just a comment: I like to add a print statement into the loops to check what they are doing :-)
  - that is a very good practice and helps with debugging your code!
  - You can also use the Python Tutor to see what your code is doing: http://pythontutor.com

## Questions in Ep. 16 (Writing Functions)
- Q: Why not use else?
    - A: It would give the same result, but I think "else" would be clearer. So, good idea!

- Q: can you state the difference in functions and  
    - > the question stopped here 

## Exercises part 3 Until 11:45

### Ep. 16 Writing Functions

#### Encapsulation
![](https://codimd.carpentries.org/uploads/upload_6f31073e511f6332274baa3dd44cadfd.png)

- I have a question- we do not manage to get the minimum value returned, instead we get a mix of characters and numbers
    - Which breakout room are you in?
    - 8
    - Coming!
#### Find the First
![](https://codimd.carpentries.org/uploads/upload_188cb53d14ed63ea96ea282bafbf3c04.png)

#### Calling by Name
![](https://codimd.carpentries.org/uploads/upload_1b92ff279ca9f56500e2ebc3a1b2e8ee.png)

#### (extra: Encapsulating Data Analysis)
![](https://codimd.carpentries.org/uploads/upload_ddf5841850a47763c83340ee5417a6a3.png)

## Questions at the end of Day 2
- Q: Could you kindly explain again what the implication of "return None" is for the example we did with date_result = print_date(x , y , z)? From group (6)
    - A: In python every function returns something, so in the example, the print_date function did not have a return in the body of the function there but when calling it, it would return None. 
        - Thank you :) 

- Q: Was there a link to the content of the course that we can later refer to? 
    - A: https://swcarpentry.github.io/python-novice-gapminder/index.html ✨
 
- Q: Do you know if we can use codimd for our classes?
     - A: You can use hackmd.io as exactly the same interface.
     - A2: etherpad as well: https://etherpad.wikimedia.org for an 'open' one
     - A3: overleaf for LaTeX

- Q: How do you deal with matrices in Python?
    - A: the Numpy package has functionality for working with matrices (and arrays/vectors)
