---
id: App route decorator
aliases: []
tags:
  - flaskframework
  - python
  - webdevelopment
  - programming
status: adult
---
---

11:33, Tue 04 November 2025

---

```
@app.route('/')
```
An app route is a decorator ([[Decorator]]) that tells Flask ([[Flask web application framework for python|flask web application framework for python]]) what page to direct the user to in a web app.

It is usually followed by a function, that once accessed, the function defined below it is cued.
```python
@app.route('/') 
def home():
	return "Welcome to the Home Page!"
```

### See also:
