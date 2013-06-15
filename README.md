django-tinymce
===

**django-tinymce** is a Django application that contains a widget to render a form field as a TinyMCE editor.

Quickstart:
===

Install django-tinymce:

    $ pip install -e git://github.com/willemallan/django-tinymce.git#egg=tinymce

Add tinymce to INSTALLED_APPS in settings.py for your project:

    INSTALLED_APPS = (
        ...
        'tinymce',
    )

Add tinymce.urls to urls.py for your project:

    urlpatterns = patterns('',
        ...
        (r'^tinymce/', include('tinymce.urls')),
    )

In your code:

    from django.db import models
    from tinymce.models import HTMLField

    class MyModel(models.Model):
        ...
        content = HTMLField()

**django-tinymce** uses staticfiles so everything should work as expected, different use cases (like using widget instead of HTMLField) and other stuff is available in documentation.

Documentation:
===
http://django-tinymce.readthedocs.org/

License (and related information):
===
Originally written by Willem Allan.

This program is licensed under the MIT License (see LICENSE.txt)
