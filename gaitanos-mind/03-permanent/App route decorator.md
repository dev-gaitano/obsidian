```
@app.route('/')
```
An app route is a decorator ([[Decorator]]) that tells Flask what page to direct the user to in a web app.

It is usually followed by a function, that once accessed, the function defined below it is cued.
```
@app.route('/') 
def home():
	return "Welcome to the Home Page!"
```