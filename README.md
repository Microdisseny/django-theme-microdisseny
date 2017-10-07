Django Theme Microdisseny
=========================

Install
-------

pip install -e git+https://github.com/Microdisseny/django-theme-microdisseny.git#egg=theme_microdisseny


Use
---

Add 'theme_microdisseny' to 'INSTALLED_APPS', before 'django.contrib.admin'

```
INSTALLED_APPS = [
    ...
    'theme_microdisseny',
    ...
    'django.contrib.admin',
    ...
]
```


Customize
---------

Create a ''base_site.html'' file in ''your_app/templates/admin'', with an extends line like in this example:

```
{% extends "theme_microdisseny/base_site.html" %}

{% block branding %}
<h1 id="site-name"><img src="/foo/bar/static/logo.svg" /><a href="{% url 'admin:index' %}">{{ site_header|default:_('Django administration') }}</a></h1>
{% endblock %}
```
