22:57 Sat 8th March 2025

Status: adult

Tags: #python #programminglanguage #programming #youtube 

---
https://youtu.be/YYXdXT2l-Gg?si=pYd3_bebLVOdSv23
Corey Schafer - Youtuber

---
#### Mac / Unix Install

For Mac Python comes pre installed, to check if you have python run the bash command;

```bash
python --version
```

If you have python installed, this should return your python version, e.g. 

```bash
Python 2.7.10
```

It's recommended to use the latest stable version of Python while learning (which at the time of writing this is Python 3.12.3).

 To download the latest version, go to the 'downloads' path in the [python official website](https://www.python.org/)
 ![[Pasted image 20250308231205.png]] 
 The website will automatically detect your Operating System and recommend the latest stable release for that system. Download the release and follow the installation steps.

At this point you should have the latest python version installed on your computer. To confirm this, we'll run the same bash command we ran the first time, but because we're using python v3 now, we use the command `python3`;

```bash
python3 --version
```
```bash
Python 3.12.3
```

If you would like to customize python to use the `python` command instead of `python3`, you can do so in the `~/.bash_profile` file by adding the following line, saving the file and restarting the terminal;

```bash
alias python=python3
```

Make sure to write the line exactly as it is in the snippet to avoid any errors.


#### Windows Install

To check if you have Python already installed in your system run the command;

```bash
python --version
```

Because python does not come pre-installed on windows, this command will return an error;

```bash
'python' is not recognized as an internal or external command, operable program or batch file
```

To solve this error, we need to download python. Go to the 'downloads' path in the [python official website](https://www.python.org/)

![[Pasted image 20250308231205.png]]

The website will automatically detect your Operating System and recommend the latest stable release for that system. Download the release.

While installing python make sure to check, 'Add Python to PATH', this is what allows you to run python from anywhere in your system. ***This step is crucial, if skipped you'll have to go into advanced system setting to setup python***

![[Pasted image 20250308235920.png]]

Follow the installation steps and finish the setup.

Python should now be successfully be installed in your system. To confirm this we run the `python` command;

```bash
python --version
```

The command should now return the python release you installed.

```bash
Python 3.12.3
```

*NB: While using python v3, the command `python3` is only necessary in Unix based systems, for windows `python` or `python3` both work fine.*


#### Installation Complete

Now that the installation is complete, to run python we use the command;

```bash
python   # or python3 for unix based systems
```

This will run what is called an 'Interactive Prompt'. 

```bash
Python 3.12.3 (main, Feb  4 2025, 14:48:35) [GCC 13.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

The interactive prompt allows us to write one line of python at a time. For example,

```bash
>>> print('Hello World')
Hello World
```

To exit the python Interactive Prompt we use the function,

```bash
>>> exit()
```

The Interactive Prompt is very useful but ideally we want to create a python file so that we can have the ability to write multiple lines of code.

Python files are created with a '.py' extension, for example 'intro.py'. Let's create this example file!

![[intro.py]]

Open the new file in a text editor of your choice. When we installed python, an idle app was also installed in our system, you can use this as an editor.

Add any python code line into the file, and save the file.

```python
# Example line of code
print('Hello World')
```

To run a python file we use the `python` command - `python3` for Unix - followed by the file path, or filename if you are already in the folder where the python file is located.

```bash
python intro.py
```

This command will run our file and return the output.

```bash
Hello World
```

*NB: To add a comment in python we use a '#' symbol before the comment. Comments are ignored while the computer is running the python file.*

The python idle app was more than enough for this example but as your projects get more complex you'll need a more robust text editor like vim, emacs, sublime text, etc. or even an IDE which will offer you even more features.

One major advantage of using a text editor or an IDE is that you can run the file right in the editor or IDE.
### See also:
[[Python programming language]]
