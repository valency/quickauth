=========
QuickAuth
=========

A quick user-password authentication for Python.

Installation
------------

.. code:: bash

    pip install quickauth

Usage
-----

.. code:: python

    from quickauth.core import QuickAuth
    authenticator = QuickAuth()
    print(authenticator.register())
    print(authenticator.authorize(key='fbdca934-34c0-11e9-8bb3-685b35d08286',value='579d0f25-aed1-40c4-afa8-61e11254f47e'))
    print(authenticator.update(key='fbdca934-34c0-11e9-8bb3-685b35d08286'))

Outputs:

.. code:: json

    {'key': 'fbdca934-34c0-11e9-8bb3-685b35d08286', 'secret': '579d0f25-aed1-40c4-afa8-61e11254f47e'}
    True
    {'key': 'fbdca934-34c0-11e9-8bb3-685b35d08286', 'secret': '974bc9bb-8839-4f0c-83b7-adc78cc3247d'}


Run from terminal:

.. code:: bash

    python3 -m quickauth.core [-h] [--db DB] [-k KEY] [-s SECRET] OPERATION


Positional arguments:

`OPERATION` register, authorize, or update

Optional arguments:

-h, --help                  show this help message and exit
--db DB                     database file, default: auth.db
-k KEY, --key KEY           key
-s SECRET, --secret SECRET  secret
