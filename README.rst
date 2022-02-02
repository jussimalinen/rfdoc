RFDoc
=====

Introduction
------------

RFDoc is a web application for storing and searching `Robot Framework
<http://robotframework.org>` test library and resource file documentations.

RFDoc is implemented using `Django web framework <http://djangoproject.com>` version 4.0 or higher.

**Note:** This project is currently not actively maintained.

License
-------

RFDoc is licensed under Apache License 2.0.

See LICENSE.txt for details.

Running RFDoc
-------------

For getting RFDoc to run locally, see
https://github.com/robotframework/rfdoc/blob/wiki/DevelopmentEnvironment.md

**Note:** In section 'Set up the database' replace

```
python -m rfdoc.manage syncdb
```
with
```
python -m rfdoc.manage migrate --run-syncdb
```

For setting up a public production server, see
https://github.com/robotframework/rfdoc/blob/wiki/ProductionEnvironment.md

Directory Layout
----------------

atest/
    Acceptance tests. Naturally using Robot Framework.

src/
    RFDoc source code.

tools/
    Utilities to use as part of the CI pipeline or as SCM hooks.

Running the Acceptance Tests
----------------------------

Acceptance tests are run using ``atest/run_atests.py``.

Run the script without any arguments for help.

TL;DR
----------------------------
1. execute ``python setup.py install``
2. execute ``python -m rfdoc.rfdocsettings_defaults /your/path/here`` to create a **rfdocsettings.py**
3. edit **rfdocsettings.py** to your needs
4. add */your/path/here* to **PYTHONPATH** or use parameter **--pythonpath=/your/path/here** in the command below:
5. execute ``python -m rfdoc.manage migrate --run-syncdb``
6. execute ``python -m rfdoc.manage runserver``
