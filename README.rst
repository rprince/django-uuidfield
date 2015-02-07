django-uuidfield
----------------

Provides a UUIDField for your Django models.

Installation
============

Install it with pip (or easy_install)::

	pip install django-uuidfield

Usage
=====

First you'll need to attach a UUIDField to your class. This acts as a char(32) to maintain compatibility with SQL versions::

	from uuidfield import UUIDField
	
	class MyModel(models.Model):
	    uuid = UUIDField(auto=True)

Check out the source for more configuration values.

Enjoy!

Known Limitations
=================

* Migrations do not currently work when adding a UUIDField to a model. You will likely get an error like "django.db.utils.IntegrityError: UNIQUE constraint failed".
