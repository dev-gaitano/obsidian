1. Open your terminal/command prompt.
	1. Use keyboard shortcut 'Windows+r'
	2. Type 'cmd'
	3. Press 'Enter'

2. Navigate to your project directory.
```
cd project\file\path
```

3. Create the [[Virtual environment]] using the [['-m' flag]] and 'venv' as the module ([[Modules]]).
```
python -m venv my_env
```
You should now have a directory named 'my_env' in your project directory.

4. Activate the virtual environment.
```
my_env\Scripts\activate
```
Activating the virtual environment will ensure that all project dependencies are installed in the virtual environment you've created.

**See also**
[[Python programming language]]
[[Virtual environment]]