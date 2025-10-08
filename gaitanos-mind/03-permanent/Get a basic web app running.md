1. Open a project directory and create a new [[Python programming language]] script.
	![[Pasted image 20241207171841.png]]
2. From 'flask' Import 'Flask'
```
	from flask import Flask
```
3. Create a new app and name it, e.g. 'app'.
```
	app = Flask(__name__)
```
4. Create an app route ([[App route decorator]]).
```
	@app.route('/')
```
5. Define a function for the landing page of your web app. This is the path of the app route created above.
```
	def home():

    return 'Hello World!'
```
6. Save and run the application by typing 'localhost:5000' in your internet browser search bar.
```
	if __name__ == '__main__':

    app.run(debug=True)
```
	*debug=True* allows Flask to the server with debugging enabled

The boilerplate code will look something like this;
```
from flask import Flask

app = Flask(__name__)  

@app.route('/')
def home():
    return'Hello World!'

if __name__ == '__main__':
    app.run(debug=True)
```

**See also**
[[Python programming language]]
[[Learn Flask for Python(FreeCodeCamp.org)]]

