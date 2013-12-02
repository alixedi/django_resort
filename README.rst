=============================
django_resort
=============================

.. image:: https://badge.fury.io/py/django_resort.png
    :target: http://badge.fury.io/py/django_resort
    
.. image:: https://travis-ci.org/alixedi/django_resort.png?branch=master
        :target: https://travis-ci.org/alixedi/django_resort

.. image:: https://pypip.in/d/django_resort/badge.png
        :target: https://crate.io/packages/django_resort?version=latest


Implement sorting for ListView columns without changing your views.

Installation
------------

Get it from the cheeseshop: ::

	pip install django_resort

Usage
-----

Read on:

1. Include `django_resort` in your `INSTALLED_APPS` settings.

2. Load the tags: ::

	{% load resort %}

3. Jut before the for loop iterating through the object_list, include: ::

    {% auto_sort object_list %}
    {% for object in object_list %}

4. In your table header: ::

	<th>{% sort_link field.verbose_name|title field.name %}</th>

Credits
-------
This project is primarily based upon `django-sorting <https://github.com/agiliq/django-sorting>`_ which it seems is no longer actively maintained as I could not get it to install using pip.