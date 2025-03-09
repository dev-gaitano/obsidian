20:54 Mon 30th December 2024

Tags:

---
```
# views.py

from django.http import HttpResponse

# Class Based View

class ProfileView(View):
	def get(self, request):
		user = getUser()
		return render(request, 'profile.html', {'user' :user})

# function Based View

def greeting(request):
	return HttpResponse('Hello World!')
```

### See also:
