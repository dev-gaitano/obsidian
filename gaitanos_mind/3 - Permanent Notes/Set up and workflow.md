1. Start by installing [[Python programming language]] on your PC.
2. Create a new project directory.
3. Open your project directory in an [[Integrated Development Environment (IDE)]] of your choice.
4.  Install a [[Virtual environment]].
```
pip install virtualenv
```

5. Create a virtual environment.
```
virtualenv env
```
You should now have a new directory named 'env' in your project directory.

6. Activate the virtual environment you created.
```
env\Scripts\activate
```
Any packages you install will now be installed in this new 'env' directory.

7. Using pip, install the the required [[Libraries]]
	[[Flask web application framework for python]] 
```
pip install Flask
```
	Flasksqlalchemy
```
pip install Flasksqlalchemy
```

**See also**
[[How to install python for windows]]
[[How to create a python virtual environment in windows]]
How to install libraries