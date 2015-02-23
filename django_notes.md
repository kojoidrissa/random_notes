#Notes on Django and related topics

##Videos to watch
-  [DjangoCon 2014- AngularJS + Django = A Perfect Match](https://www.youtube.com/watch?v=vWJorwEQWLk)
-  [Django for Web Designers and Front End Developers](http://pyvideo.org/video/2624/django-for-web-designers-and-front-end-developers)
    +  I think I've got this going in YouTube at the moment (2014-12-11T13:04:47-06:00)
    +  A 3 hour-tutorial by the same person who did "How I went from Designer to Django Dev in 6 weeks"
-  [PyTexas 2014](https://www.youtube.com/results?search_query=pytexas+2014&page=1) on YouTube

##Django Tutorial

###Part 2
-  In the [Free Admin Functionality](https://docs.djangoproject.com/en/1.7/intro/tutorial02/#explore-the-free-admin-functionality), they mention, "Each DateTimeField gets free JavaScript shortcuts". Look into thos shortcuts. Seems like they'd be useful for other web apps
-  Why create ModelAdmin objects?
>  This isn’t impressive with only two fields, but for admin forms with dozens of fields, choosing an intuitive order is an important usability detail.
-  Look into the [list_disply](https://docs.djangoproject.com/en/1.7/ref/contrib/admin/#django.contrib.admin.ModelAdmin.list_display) properties
-  learn how to use/reset the `django.contrib.admin.AdminSite.site_header` [attribute](https://docs.djangoproject.com/en/1.7/ref/contrib/admin/#django.contrib.admin.AdminSite.site_header). Do this instead of manually editing the `base_header.html` file
    +  the [template loader](https://docs.djangoproject.com/en/1.7/ref/templates/api/#template-loaders) docs might help

###Part 3
-  In the following code, in `kojoidrissadotcom/kojoidrissadotcom/urls.py` why does polls.urls need quites and admin.site.urls NOT? Is it because polls.urls is a custom module?
<code>url(r'^polls/', include('polls.urls')),
    url(r'^admin/', include(admin.site.urls)),
</code>
-  Get familiar with Python's [re module](https://docs.python.org/3/library/re.html#module-re) so I can read the regex used in urls.py

