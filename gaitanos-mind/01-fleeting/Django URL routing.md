---
id: Django URL routing
aliases: []
tags:
  - django
  - python
  - programming
status: child
---
---

21:01, Mon 30th December 2024

---

```python
# my_app/urls.py

from django.urls import path
from . import views

# URLconf
urlpatterns = [
	path('plaground/intro/', views.greeting),
]

# my_project/urls.py

from django.urls import path, include

urlpatterns = [
	...
	path('my_app/', include('my_app.urls))
]
```

### See also:
[[Django web application framework for python]]
