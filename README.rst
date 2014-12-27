Timeout wrapper
===============

.. image:: https://badge.fury.io/py/timeout_wrapper.png
    :target: http://badge.fury.io/py/timeout_wrapper

.. image:: https://pypip.in/d/timeout_wrapper/badge.png
        :target: https://pypi.python.org/pypi/timeout_wrapper


Timeout decorator with defaults and exceptions.

Documentation
-------------

Usage of this decorator is really simple - to set the timeout, just add
``@timeout(time)`` decorator to your function definition::

    @timeout(3)  # 3 seconds
    def myfunc(..):
        ..

If the ``myfunc()`` call timeouts, ``TimeoutException`` is raised.

Optionally, you can also set your own message for exception::

    @timeout(3, exception_message="Oh noez")
    def myfunc(..):
        ..

or use default value, instead of exception::

    @timeout(3, False):
    def myfunc(..):
        ..

Thats all.


Installation
------------
Module is hosted at `PYPI <https://pypi.python.org/pypi/timeout_wrapper>`_,
and can be easily installed using
`PIP <http://en.wikipedia.org/wiki/Pip_%28package_manager%29>`_:

::

    sudo pip install timeout_wrapper