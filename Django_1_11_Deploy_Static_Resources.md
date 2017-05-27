# Deploy Static resources on Django 1.11
1. "mkdir static" under the project folder
2. in the settings.py file, add the following sentences:
``` python
STATICFILES_FINDERS = [
'django.contrib.staticfiles.finders.FileSystemFinder',
'django.contrib.staticfiles.finders.AppDirectoriesFinder',
]

STATICFILES_DIRS = [
os.path.join(BASE_DIR, 'static')
]

```
3. Use static files look like:
``` html
<!-- The static file used in this example is static/images/sitelogo.png-->
<html>
<head>
    <title>{% block title %}{% endblock %}</title>
</head>
<body>
    <img src="{% static "images/sitelogo.png" %}" alt="Logo" />
    {% block content %}{% endblock %}
</body>
</html>
```