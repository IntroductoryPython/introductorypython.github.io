# FAQ

This document is meant to answer a number of commonly-asked questions about the final project. We hope you find it helpful as you develop your awesome projects!

Note for IntroductoryPython: this FAQ answers questions, following the guidelines for the University course. These answers may be useful, but you of course do not need to follow specific guidelines for the class.

---

### File Structure and Requirements

#### Do we still need a .py file if all our code and functions are in a Jupyter notebook?
Yes, you need at least one .py file - either a module or a script. It can have both, but that is not required.

#### What is the difference between a script and a module?
A module stores functions/classes that you'll want to use later, perhaps in your script or notebook. Scripts include code intended to run from top to bottom and will likely use the functions in your module.

#### How do I create a script or module?
On Datahub or Anaconda, in the new tab at the top right, select text file. When you save that file, save it with a .py extension. Alternatively, from the terminal, you can use the `touch` command.

#### What goes in requirements.txt?
You should mention if you installed any new packages via pip for your project that aren’t included by default in the anaconda distribution/datahub so we'll be able to run your code properly. If you didn't install anything to run your code, you don't need to include this file.

#### How do I install a library?
Use pip in the terminal. On datahub, the command will look something like: `pip install --user package`.

#### Is there a set number of functions or classes we need to include?
You need at least 3 original functions or methods. There is no class requirement. (For example, you could have a single class with 3 methods. Or, no classes and 3 separate functions.)

#### Can I write my entire project code into one class?
Yes, as long as the class includes a modular design where there are multiple independent methods.

#### Are we supposed to call our files and directories functions.py, ProjectNotebook.ipynb, etc. or should we call them something related to the project itself?
You could change the names if you'd like or keep them as they are. Just make sure to import using the correct file names.

#### Can I submit the project using a different file structure than the template provided?
Yes, the specific file structure is not important. We care that you have a folder that contains a notebook and a script/module file (or both). Other files can also be included if applicable. Use an oganization structure that makes sense for your project.

#### How/in what format should the files be submitted?
For submitting your final projects, you will either 1) zip up all the files for your project (i.e. Notebook + module directory with tests and functions) and submit the zipped file on Canvas or 2) submit on datahub.

---

### Importing Modules

#### I wrote a function in a file, and I am trying to use it a separate file; however, it says that my function "is not defined".
Check to make sure you imported your function before trying to call it. You will need to import any functions you write if you want to use them.

#### I am trying to import specific functions from my module, but it says that my module does not exist?
Check the location of the file that contains your functions. If your my_functions.py file is within a folder (let's say called `modules/`), you would need to call `from modules.my_functions import func1, func2` instead of just   `import my_functions`.

More resources for importing modules:
https://docs.python.org/3/tutorial/modules.html

---

### Citations

#### If I went back through my class notes because I couldn't remember how do X, and I found an example of how in the notes, would this require a citation?
No. This would not require a citation if you're referencing something taught in class; however, if you copy and paste a function used in an Assignment or lecture directly for your project, this would require citation.

#### I looked up how to do X and found a thread about it on a website that helped me figure out my problem. I cited this in my Jupyter notebook, is that necessary?
This is fine and good practice. Including a comment (`#`) with the URL is sufficient for this project. Specify whether you've modified code (changed it) or used it directly - either is fine, but best to be clear about this. You can also mention the sources in the docstring of a function if a major part of that function code was referenced from an external source.

#### Is it okay to use the code from Assignment X as long as I make some modifications? Will I be marked down for not coming up with it on my own?
This is fine as long as you cite your sources with a comment and write at least 3 original functions/methods that are not from the Assignment.

---

### Documentation and Comments

#### Where should I include docstrings and comments?
Your module with your functions should have docstrings for functions and inline comments as needed. The Notebook would likely then (depending on your project) have a description of your project in a markdown cell, import your functions, and then run your main function to demonstrate how your project works. If you choose to run your project using a script rather than a Notebook, the Notebook should contain a short description of the project and a line of code that runs your script, such as `%run -i 'script.py'` or `!python script.py`. Note that test functions don’t require docstrings, but including them is fine.

#### Do we need a docstring for `__init__` functions of classes?
Depends on how complicated your `__init__` function is. Can the reader tell at a glance what the init function is doing or which class variables are being set and why? If not, maybe describe those variables in code documentation and have a simple method comment that says "Class constructor for class Foo." When in doubt, make comments!

#### For a class docstring, there is a methods section to list the methods of the class. Is it necessary to have a short description of those methods again in the class docstring since there are methods docstrings?
No need to describe the methods; just describe what the class is used for briefly. Repetitions can be avoided.

More resources for formatting docstrings:
https://numpydoc.readthedocs.io/en/latest/format.html#documenting-class-instances

---

### Testing

#### How many tests are needed? Do we need tests for only one function or for all of them in the project?
You need to test at least three methods/functions, using at least three test functions. These tests should be for your original code.

#### I used a function from Assignment X, and I was wondering if I could make a test for that one rather than a function I wrote.
You may also (and are encouraged to) write test these functions as well; however, your three required tests must test your original code.

#### Do we need to import our test functions into our script/Notebook?
You can leave them in the test file; however, it's recommended that you use `pytest` to ensure all your tests pass.

#### How do I run pytest?
If you open up a terminal and navigate to the directory where your test functions are, you can run the following: `pytest name_of_file_with_test_functions.py`

#### How would I test a function that needs user input?
The simplest way is to move the user input outside of the function and give it as a parameter to the function. Otherwise, we recommend checking out this link:
https://stackoverflow.com/questions/35851323/how-to-test-a-function-with-input-call

---
*This document was originally written by [Severine Soltani](https://github.com/SevSoltani), an awesome COGS 18 Instructional Assistant. Thanks to Severine for taking the time to draft this to help students going forward!*
