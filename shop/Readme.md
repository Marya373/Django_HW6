(.venv) maryafaivisovich@192 shop % python manage.py runserver
Exception in thread django-main-thread:
Traceback (most recent call last):
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/backends/mysql/base.py", line 15, in <module>
    import MySQLdb as Database
ModuleNotFoundError: No module named 'MySQLdb'

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.11/lib/python3.11/threading.py", line 1038, in _bootstrap_inner
    self.run()
  File "/Library/Frameworks/Python.framework/Versions/3.11/lib/python3.11/threading.py", line 975, in run
    self._target(*self._args, **self._kwargs)
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/utils/autoreload.py", line 64, in wrapper
    fn(*args, **kwargs)
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/core/management/commands/runserver.py", line 125, in inner_run
    autoreload.raise_last_exception()
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/utils/autoreload.py", line 87, in raise_last_exception
    raise _exception[1]
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/core/management/__init__.py", line 394, in execute
    autoreload.check_errors(django.setup)()
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/utils/autoreload.py", line 64, in wrapper
    fn(*args, **kwargs)
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/__init__.py", line 24, in setup
    apps.populate(settings.INSTALLED_APPS)
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/apps/registry.py", line 116, in populate
    app_config.import_models()
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/apps/config.py", line 269, in import_models
    self.models_module = import_module(models_module_name)
                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Library/Frameworks/Python.framework/Versions/3.11/lib/python3.11/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1206, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1178, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1149, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 690, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 940, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/contrib/auth/models.py", line 3, in <module>
    from django.contrib.auth.base_user import AbstractBaseUser, BaseUserManager
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/contrib/auth/base_user.py", line 58, in <module>
    class AbstractBaseUser(models.Model):
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/models/base.py", line 143, in __new__
    new_class.add_to_class("_meta", Options(meta, app_label))
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/models/base.py", line 371, in add_to_class
    value.contribute_to_class(cls, name)
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/models/options.py", line 243, in contribute_to_class
    self.db_table, connection.ops.max_name_length()
                   ^^^^^^^^^^^^^^
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/utils/connection.py", line 15, in __getattr__
    return getattr(self._connections[self._alias], item)
                   ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/utils/connection.py", line 62, in __getitem__
    conn = self.create_connection(alias)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/utils.py", line 193, in create_connection
    backend = load_backend(db["ENGINE"])
              ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/utils.py", line 113, in load_backend
    return import_module("%s.base" % backend_name)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Library/Frameworks/Python.framework/Versions/3.11/lib/python3.11/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/maryafaivisovich/Desktop/django/hw4_Django/shop/.venv/lib/python3.11/site-packages/django/db/backends/mysql/base.py", line 17, in <module>
    raise ImproperlyConfigured(
django.core.exceptions.ImproperlyConfigured: Error loading MySQLdb module.
Did you install mysqlclient?

<!-- asgiref==3.7.2
Django==4.2.2
load-dotenv==0.1.0
python-dotenv==1.0.0
sqlparse==0.4.4
typing_extensions==4.9.0
tzdata==2023.4
python-dotenv
mysqlclient -->