.. _commands:

Management commands
===================

django-reversion includes a number of ``django-admin.py`` management commands.


.. _createinitialrevisions:

createinitialrevisions
----------------------

Creates an initial revision for all registered models in your project. It should be run after installing django-reversion, or registering a new model with django-reversion.

.. code:: bash

    ./manage.py createinitialrevisions
    ./manage.py createinitialrevisions your_app.YourModel --comment="Initial revision."

Run ``./manage.py createinitialrevisions --help`` for more information.

.. Warning::
    For large databases, this command can take a long time to run.


deleterevisions
---------------

Deletes old revisions. It can be run regularly to keep revision history manageable.

.. code:: bash

    ./manage.py deleterevisions
    ./manage.py deleterevisions your_app.YourModel --days=30

Run ``./manage.py deleterevisions --help`` for more information.

.. Warning::
    With no arguments, this command will delete your entire revision history! Read the command help for ways to limit which revisions should be deleted.
