Flake8 Extension to enforce better comma placement.
===================================================

**Note:** Forked from PyCQA/flake8-commas to add support for Python 3.11, match statement, and other features. Support
for Python version below 3.7 has been dropped, as well as older (2.x.y) versions of flake8.

**Further Note:** The changes here have been merged back into PyCQA/flake8-commas and a new version has been released
so this repo is no longer needed and is now archived.

Usage
-----

If you are using flake8 it's as easy as:

.. code:: shell

    pip install https://github.com/karamanolev/flake8-commas.git

Now you can avoid those annoying merge conflicts on dictionary and list diffs.

Errors
------

Different versions of python require commas in different places. Ignore the
errors for languages you don't use in your flake8 config:

+------+-----------------------------------------+
| Code | message                                 |
+======+=========================================+
| C812 | missing trailing comma                  |
+------+-----------------------------------------+
| C813 | missing trailing comma in Python 3      |
+------+-----------------------------------------+
| C814 | missing trailing comma in Python 2      |
+------+-----------------------------------------+
| C815 | missing trailing comma in Python 3.5+   |
+------+-----------------------------------------+
| C816 | missing trailing comma in Python 3.6+   |
+------+-----------------------------------------+
| C818 | trailing comma on bare tuple prohibited |
+------+-----------------------------------------+
| C819 | trailing comma prohibited               |
+------+-----------------------------------------+

Examples
--------

.. code:: Python

    lookup_table = {
        'key1': 'value',
        'key2': 'something'  # <-- missing a trailing comma
    }

    json_data = json.dumps({
        "key": "value",
    }),                      # <-- incorrect trailing comma. json_data is now a tuple. Likely by accident.

