---
id: Templates and Static Content
aliases: []
tags:
  - flaskframework
status: adult
---
---

14:09, Tue 04 November 2025

---

1. In a project file create two new directories, called 'templates' and 'static'.
	![[Screenshot 2024-12-05 092922.png]]

2. In the templates directory create a new template ([[Template]]).
	Create a HTML file, e.g. 'index.html'.
	![[Screenshot 2024-12-05 093359 1.png]]
	Add your front-end code into this HTML file.
	This HTML file is our template ([[Template]]), it is embedded into your [[Python programming language]] script, when creating a [[Flask web application framework for python]] web app.
	
3. Embed the template into your python script using the 'render_template' library from 'flask'. import the 'render_template' library from 'flask'.
```python
from flask import render_template
```

4. In your [[App route decorator]] 's defined function, embed your template into your python script using the 'render_template' library
```python
@app.route('/')
def home():
	return render_template('index.html')
```

This will return our HTML code when the app route's URL is accessed by the user. 
A basic Flask app ([[Flask web application framework for python]]) with an embedded HTML template should look like this:
```python
	from flask import Flask, render_template
  
app = Flask(__name__)  

@app.route('/')
def home():
    return render_template('index.html')
  
if __name__ == '__main__':
    app.run(debug=True)
```

5. In the 'static' directory create a new directory called 'CSS'. ([[Creating static content]]). Then you create your [[Static content]] by creating 'CSS' file, e.g. 'style.css', in the 'CSS' directory.
	![[Screenshot 2024-12-05 102103.png]]
	This 'CSS' file will act as the [[Stylesheet]] in the HTML template.

6.  Embed the stylesheet into your HTML template.

### See also:

[[Flask web application framework for python]]
[[Dynamic Templates]]
[[Template Engine]]
