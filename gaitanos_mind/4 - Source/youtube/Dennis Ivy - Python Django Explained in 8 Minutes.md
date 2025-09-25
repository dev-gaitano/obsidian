---
id: Dennis Ivy - Python Django Explained in 8 Minutes
aliases: []
tags:
  - django
  - youtube
  - frameworks
  - webdevelopment
---

10:10 Sun 29th December 2024

------------------------------------
https://youtu.be/0sMtoedWaf0?si=gPmTULRSbTiBqg44
Dennis Ivy - Youtuber

**APPS**
Apps are small pieces of a project that make up the entire website.
We create apps to represent different parts of the website.
![[Pasted image 20241229101639.png]]
Apps contain
	1. Models
	2. Views
	3. URLs
	4. Templates

Apps separate tasks in the website.

**VIEWS**
==*see also: [[Django Views]]*==

Views process the users request when they visit a certain URL.
![[Pasted image 20241229102714.png]]
The view returns a response with data, this data is usually a HTML file.

```python
class ProfileView(View):
	def get(self, request):
		user = getUser()
		return render(request, 'profile.html', {'user' :user})

	def post(self, request):
		pass
```

They are categorized into class based views and function based views.

**URLs**
To handle URL routing, we create URL patterns in a list then attach the path to the required view.
This is how django know which view to call when the client requests a certain URL.

```python
urlpatterns = [
	path('profile/', views.profileView),
]
```

**TEMPLATES**
Development of APIs and frontend Frameworks is making templates less needed

```html
<!-- Variables -->
{{ variable }}

<!-- Tags -->
{% tag %}

<ul>
	{% for athlete in athlete_list %}
		<li>{{ athlete.name }}</li>
	{% endfor %}
</ul>
```

**MODELS**
*"Models are class-based representations of our database tables".*

```python
class Project(models.Model):
	title = models.charField()
	description = models.TextField()
	id = models.UUIDField()
```
==*What is a UUIDField?*==

At the core of how we create and design our database.
Each attribute in our model represents a column in a table in our database.

**DJANGO ORM**
The Django ORM allows you to work with the database you designed using the models.

```python
item = ModelName.objects.get(id=1)
queryset = ModelName.objects.all()
queryset = ModelName.objects.filter()
```

We work with method like, get(), all() and filter() to retrieve data from the database.
	==*How do we add data to the database?* Using CRUD processes==

**ADMIN PANEL**
Django provides a QuickStart interface to work with our data.

**CRUD**
To perform 
	Create,
	Read,
	Update and
	Delete functions,
	
we can use:
1. Methods 
	save()
	delete()

2. Django model forms
```python
	class UserForm(ModelForm):
		class Meta:
			model = User
			fields = '__all__'
```

3. class based views
```python
	class UserCreate(CreateView)
		model = User
		fields = ['username', 'email', 'password']
```

**STATIC FILES**
==*See also: [[Static content]]*==
Static files add a visual layer to our websites.
![[Pasted image 20241229115627.png]]

They also help handle user uploaded content, e.g. profile pictures.

```python
STATIC_URL = '/static/'
MEDIA_URL = '/images/'

STATICFILES_DIRS = [
	BASE_DIR / 'static'
]

MEDIA_ROOT = BASE_DIR / 'static/images'
STATIC_ROOT = BASE_DIR / 'staticfiles'
```

**AUTHENTICATION & AUTHORIZATION**

![[Pasted image 20241229120446.png]]
Django has built-in authentication and authorization methods and forms which simplify processes such as:
	Logging in/out
	User registration
	Password resetting
		Password resetting requires configuration. 

**COMMON COMMANDS**

```bash
# Creates boilerplate django files
django-admin startproject <project_name>

# Creates app folder and files
python manage.py startapp <app_name>

# Preps our database for migrations
python manage.py makemigrations

# Executes our migrations & updates the database
python manage.py migrate

# Creates a user with admin level permissions
python manage.py createsuperuser
```

**SIGNALS**
They listen for events happen in our website and trigger actions when this events occur.
![[Pasted image 20241229121928.png]]
==*See also: [[Microsoft Power Automate]]*==

Signals use senders and receivers
![[Pasted image 20241229121853.png]]

**THIS WORKS TOO!**
1. Connecting with SQL databases

```python
# Settings.py

DATABASES = {
	'default': {
		'ENGINE': 'django.db.backends.postgresql',
		'NAME': 'devsearch',
		'USER': os.environ.get('DB_USER'),
		'PASSWORD': os.environ.get('DB_PASS'),
		'HOST': os.environ.get('DB_HOST'),
		'PORT': '5432'
	}
}
```

2. Using the Django Rest [[Framework]].
Many developers these days use APIs and Frameworks instead of templates for the frontend.

```bash
pip install djangorestframework
```
```python
# Settings.py
INSTALLED_APPS = [
	...
	'rest_framework',
]

# serializers.py
class UserSerializer(serializers.HyperlinkedModeSerializer):
	class Meta:
		model = User
		fields = [ 'url', 'username', 'email', 'is_staff']
```

**DEPLOYMENT**
This is moving your website from localhost to www...
Get familiar with deployment platforms such as, Heroku and AWS.
Deployment requires configuration.
### See also:
[[Django web application framework for python]]
[[IBM Technology - What is Django]]
[[Programming with Mosh - Django Tutorial for Beginners – Build Powerful Backends]]


