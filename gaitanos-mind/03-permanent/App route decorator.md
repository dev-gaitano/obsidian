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

An app route [[What is a decorator (Python)|decorator]], is a function that tells [[Flask web application framework for python|Flask]] what page to direct
the user to in a web app.

The app route decorator is followed by a function, that is executed when the
route in the decorator is accessed.

```python
@app.route('/') 
def home():
	return "Welcome to the Home Page!"
```

### See also:
