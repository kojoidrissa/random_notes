#Notes on Django and related topics

##Videos to watch
-  [Building a Blog with Django 1.7 in 16 mins](https://www.youtube.com/watch?v=7rgph8en0Jc)
    +  [Recreating the “Building a Blog in Django” Screencast](http://arunrocks.com/recreating-the-building-a-blog-in-django-screencast/)
-  [Kenneth Love: Getting Started with Django, a crash course - PyCon 2014](https://www.youtube.com/watch?v=KZHXjGP71kQ)
-  [Django for Web Designers and Front End Developers](http://pyvideo.org/video/2624/django-for-web-designers-and-front-end-developers)
    +  I think I've got this going in YouTube at the moment (2014-12-11T13:04:47-06:00)
    +  A 3 hour-tutorial by the same person who did "How I went from Designer to Django Dev in 6 weeks"
-  [DjangoCon 2014- AngularJS + Django = A Perfect Match](https://www.youtube.com/watch?v=vWJorwEQWLk)
-  [PyTexas 2014](https://www.youtube.com/results?search_query=pytexas+2014&page=1) on YouTube
-  [django: Web Development for Perfectionists with Deadlines - Google Talks 2012](https://www.youtube.com/watch?v=n8KnFywpXOE)

##DjangoGirls
-  DjGirls [Resources](http://djangogirls.org/resources/) page. This has links to all their tutorials and their Github repos.

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
    -  This is also probably a good time to break out *Introducing Regular Expressions*.
*  In the updated index view, what does the '-pub_date' mean? Is that telling it to take things in reverse order? [Yes](https://docs.djangoproject.com/en/1.7/ref/models/querysets/#order-by) it does.
    -  `latest_question_list = Question.objects.order_by('-pub_date')[:5]`
*  I need to fully grok Template Namespacing. The [reusable apps tutorial](https://docs.djangoproject.com/en/1.7/intro/reusable-apps/) may help with this. I used  `polls/templates/polls/index.html`. This allows me to use `polls/index.html` as the name of the template in my views.index.
*  "See the [template guide](https://docs.djangoproject.com/en/1.7/topics/templates/) for more about templates."

###Part 4: Forms
-  I'm not familiar with the "for" attribute in the HTML `<label>` tag.
-  read up on the [`{% csrf_token %}`](https://docs.djangoproject.com/en/1.7/ref/templates/builtins/#std:templatetag-csrf_token) tag.
-  read up on [`HttpResponseRedirect`](https://docs.djangoproject.com/en/1.7/ref/request-response/#django.http.HttpResponseRedirect) and [`reverse()`](https://docs.djangoproject.com/en/1.7/ref/urlresolvers/#django.core.urlresolvers.reverse)
-  "As mentioned in Tutorial 3, request is a [HttpRequest](https://docs.djangoproject.com/en/1.7/ref/request-response/#django.http.HttpRequest) object. For more on HttpRequest objects, see the [request and response documentation](https://docs.djangoproject.com/en/1.7/ref/request-response/)."
-  from the polls/results.html template: `vote{{ choice.votes|pluralize }}`; is that the UNION of...something?
-  Go back through "Use generic views: Less code is better" section

###Part 5

##Django Docs
Specific stuff I want to go back and read

-  [Deploying Django](https://docs.djangoproject.com/en/1.7/howto/deployment/)
-  [“How-to” guides](https://docs.djangoproject.com/en/1.7/howto/)
-  [Settings.py](https://docs.djangoproject.com/en/1.7/ref/settings/#core-settings)
-  [django-admin.py and manage.py](https://docs.djangoproject.com/en/1.7/ref/django-admin/)
-  [Making queries](https://docs.djangoproject.com/en/1.7/topics/db/queries/#field-lookups-intro)

##Web Server Setup
-  Learn more about the CHMOD commands I used in sections [`f, g & g`](http://docs.webfaction.com/user-guide/access.html#linux-and-mac-os-x) of the WebFaction docs 

