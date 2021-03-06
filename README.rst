.. image:: https://cdn.rawgit.com/ergoithz/netflix-penguin/master/icons/128/netflix-penguin.png
   :align: right

Netflix Penguin
===============

Site-specific browser for Netflix.

This app requires a Pipelight Silverlight installation.

Rationale
---------
The reason behind another browser, in this case specially tailored for Netflix, is Mozilla Firefox dropping Silverlight NPAPI support, along with some browser hacks needed to bypass Netflix anti-linux filters (which only were possible on Firefox).

Without Pipelight, Silverlight and NPAPi, the only remaining Netflix option is Google Chrome, with playback crippled at 720p.

As last resort, this webkit-based browser were developed, including those hacks required to bypass Netflix linux-blocking mechanisms while supporting NPAPI and therefore: silverlight.

Requirements
------------

* PyGObject (python-gobject)
* Gtk3
* Gtk WebKit2 (webkit2gtk)
* Pipelight

System-wide installation
------------------------

Official distribution methods are always preferred.

You can install Netflix Penguin system-wide, using pip, and a corresponding menu entry will be created.

.. code-block:: sh

  sudo pip install netflix-penguin

And can be uninstalled via:

.. code-block:: sh

  sudo pip uninstall netflix-penguin

Virtualenv/venv considerations
------------------------------

This app, because of PyGobject, will only install on virtualenvs created with **--system-site-packages** flag, ie:

.. code-block:: sh

  python -m venv env --system-site-packages
  env/bin/pip install netflix-penguin
