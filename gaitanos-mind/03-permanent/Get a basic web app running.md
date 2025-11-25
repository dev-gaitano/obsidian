---
id: Get a basic web app running
aliases: []
tags:
  - flaskframework
  - python
  - webdevelopment
  - programming
status: adult
---
---

14:03, Tue 04 November 2025

---

1. Open a project directory and create a new [[Python programming language]] script.
	![[Pasted image 20241207171841.png]]
2. From 'flask' Import 'Flask'
```python
	from flask import Flask
```
3. Create a new app by declaring the variable "app".
```python
	app = Flask(__name__)
```
4. Create an app route ([[App route decorator]]).
```python
	@app.route('/')
```
5. Define a function for the landing page of your web app. This is the path of the app route created above.
```python
	def home():
        return 'Hello World!'
```
6. Save and run the application by typing 'localhost:5000' in your internet browser search bar.
```python
	if __name__ == '__main__':

    app.run(debug=True)
```
	*debug=True* allows Flask to the server with debugging enabled

The boilerplate code will look something like this;
```python
from flask import Flask

app = Flask(__name__)  

@app.route('/')
def home():
    return'Hello World!'

if __name__ == '__main__':
    app.run(debug=True)
```

### See also:

[[Python programming language]]
[[Learn Flask for Python(FreeCodeCamp.org)]]

