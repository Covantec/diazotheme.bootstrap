====================
diazotheme.bootstrap
====================


Introduction
============

``diazotheme.bootstrap`` package provides diazo themes based on the `Twitter Bootstrap CSS framework`_ 
using the **theming** and **packaging** features available for create Diazo_ theme
using `plone.app.theming`_.

``diazotheme.bootstrap`` package contains the following diazo implementations: 

- **Twitter Bootstrap Marketing Narrow Theme**, is the Twitter Bootstrap Marketing Narrow theme on diazo based.
- **Twitter Bootstrap Starter Theme**, is the Twitter Bootstrap starter theme on diazo based.
- **Twitter Bootstrap Hero Theme**, a diazo theme based for Twitter Bootstrap.


How to create a child theme
---------------------------

Any of the three theme folders can be used to create your own child theme, 
based on `diazoframework.bootstrap`_. You can either wrap the theme up in a package 
or you can create a zip file of the folder and upload that to the theme panel.

There are two ways of creating a child theme.


The package way
^^^^^^^^^^^^^^^

For this example, lets assume we are creating a package called
``diazotheme.newtheme`` and we will copy the ``starter`` theme in this 
package.

1. Created the ``diazotheme.newtheme`` package (for instance through ``paster`` script).

2. Copy ``diazotheme.bootstrap/diazotheme/bootstrap/starter`` to
   ``diazotheme.newtheme/diazotheme/newtheme/starter``.

3. Rename ``diazotheme.newtheme/diazotheme/newtheme/starter``
   to ``diazotheme.newtheme/diazotheme/newtheme/static`` (arbitrary
   name).

4. Add `<plone:static directory="static" name="newtheme" type="theme"/>`
   to ``diazotheme.newtheme/diazotheme/newtheme/configure.zcml``.

5. Change ``diazotheme.newtheme/diazotheme/newtheme/static/manifest.cfg``
   to reflect the changes, so: ::

        [theme]
        title = New theme
        description = Describe the new theme
        rules = /++theme++newtheme/rules.xml
        prefix = /++theme++newtheme
        doctype = <!DOCTYPE html>
        preview = preview.png


The zip file way
^^^^^^^^^^^^^^^^

Again, lets assume we use the ``theme`` theme and we want to end up
with the ``newtheme`` name.

1. Copy ``diazotheme.bootstrap/diazotheme/bootstrap/theme`` to your file system.

2. Rename ``theme`` to ``newtheme`` (the folder name will become the
   theme name in the theme panel)

3. Change ``newtheme/manifest.cfg``
   to reflect the changes, so: ::

        [theme]
        title = New theme
        description = Describe the new theme
        rules = /++theme++newtheme/rules.xml
        prefix = /++theme++newtheme
        doctype = <!DOCTYPE html>
        preview = preview.png

4. Customize your theme.

5. When you are finished customizing, create a zip archive of the 
   ``newtheme`` folder.

6. Upload the ``newtheme.zip`` in the plone theme panel.


Screenshots
===========


Twitter Bootstrap Marketing Narrow Theme
----------------------------------------

Layout of the site when viewed in a computer resolution:

.. image:: https://github.com/TH-code/diazotheme.bootstrap/raw/master/diazotheme/bootstrap/marketing-narrow/preview.png
  :alt: Twitter Bootstrap Marketing Narrow Theme
  :align: center


Twitter Bootstrap Starter Theme
-------------------------------

Layout of the site when viewed in a computer resolution:

.. image:: https://github.com/TH-code/diazoframework.bootstrap/raw/master/diazoframework/bootstrap/framework/preview.png
  :alt: Twitter Bootstrap Starter Theme
  :align: center


Twitter Bootstrap Hero Theme
----------------------------

Layout of the site when viewed in a computer resolution:

.. image:: https://github.com/TH-code/diazotheme.bootstrap/raw/master/diazotheme/bootstrap/theme/preview.png
  :alt: Twitter Bootstrap Hero Theme
  :align: center


Requirements
============

- From the Plone 4.1.x To the Plone 4.3 latest version (https://plone.org/download)
- The ``plone.app.theming`` package (*You will need enable it to use this package*)


Features
========

- Provides the diazo rules for *Twitter Bootstrap Marketing Narrow* theme.
- Provides the diazo rules for *Twitter Bootstrap Starter* theme.
- Provides the diazo rules for *Twitter Bootstrap Hero* theme.


Installation
============


Buildout
--------

If you are a developer, you might enjoy installing it via buildout.

For install ``diazotheme.bootstrap`` package add it to your ``buildout`` section's 
*eggs* parameter e.g.: ::

   [buildout]
    ...
    eggs =
        ...
        diazotheme.bootstrap


and then running ``bin/buildout``.

Or, you can add it as a dependency on your own product ``setup.py`` file: ::

    install_requires=[
        ...
        'diazotheme.bootstrap',
    ],


Resources
=========

This package is the parent of all Plone diazo themes and 
provides rule that are practical to use in other diazo themes.


Twitter Bootstrap Marketing Narrow Theme
----------------------------------------

The resources of this theme can be reached through

    ``/++theme++bootstrap-marketing-narrow``

There are placed at ``diazotheme.bootstrap/diazotheme/bootstrap/marketing-narrow`` 
directory with following resources files:

::

    _ marketing-narrow
      Provides the resources from "Twitter Bootstrap Marketing Narrow Theme".
      _ manifest.cfg
      _ preview.png
      _ rules.xml


Twitter Bootstrap Starter Theme
-------------------------------

The resources of this theme can be reached through

    ``/++theme++bootstrap-starter``

There are placed at ``diazotheme.bootstrap/diazotheme/bootstrap/starter`` 
directory with following resources files:

::

    _ starter
      Provides the resources from "Twitter Bootstrap Starter Theme".
      _ manifest.cfg
      _ rules.xml


Twitter Bootstrap Hero Theme
----------------------------

The resources of this theme can be reached through

    ``/++theme++bootstrap``

There are placed at ``diazotheme.bootstrap/diazotheme/bootstrap/theme`` 
directory with following resources files:

::

    _ theme
      Provides the resources from "Twitter Bootstrap Hero Theme".
      _ manifest.cfg
      _ preview.png
      _ rules.xml

Contribute
==========

- Issue Tracker: https://github.com/TH-code/diazotheme.bootstrap/issues
- Source Code: https://github.com/TH-code/diazotheme.bootstrap


License
=======

The project is licensed under the GPLv2.


Credits
-------

- Thijs Jonkman (t.jonkman at gmail dot com).


Amazing contributions
---------------------

- Leonardo J. Caballero G. aka macagua (leonardocaballero at gmail dot com).

You can find an updated list of package contributors on https://github.com/TH-code/diazotheme.bootstrap/contributors

.. _`Twitter Bootstrap CSS framework`: http://twitter.github.io/
.. _`diazoframework.bootstrap`: https://github.com/TH-code/diazoframework.bootstrap
.. _`diazotheme.bootstrap`: https://github.com/TH-code/diazotheme.bootstrap
.. _`Diazo`: http://diazo.org
.. _`plone.app.theming`: https://pypi.org/project/plone.app.theming/
