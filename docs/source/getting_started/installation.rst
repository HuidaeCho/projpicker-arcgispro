Installation
============

Requirements
------------

If installed with pip, ProjPicker uses the following standard modules:

- `collections <https://docs.python.org/3/library/collections.html>`_
- `argparse <https://docs.python.org/3/library/argparse.html>`_
- `os <https://docs.python.org/3/library/os.html>`_
- `sys <https://docs.python.org/3/library/sys.html>`_
- `sqlite3 <https://docs.python.org/3/library/sqlite3.html>`_
- `re <https://docs.python.org/3/library/re.html>`_
- `math <https://docs.python.org/3/library/math.html>`_
- `json <https://docs.python.org/3/library/json.html>`_
- `pprint <https://docs.python.org/3/library/pprint.html>`_
- `tkinter <https://docs.python.org/3/library/tkinter.html>`_
- `textwrap <https://docs.python.org/3/library/textwrap.html>`_

The ProjPicker `SQLite <https://sqlite.org/>`_ database (``projpicker.db``) will come packaged when installed with pip.
However, if any problems should arise and the ``projpicker.db`` should need to be recreated, the additional dependency of `pyproj <https://pypi.org/project/pyproj/>`_ will be needed.
For more information about ``projpicker.db``, see :doc:`here </program_references/database>`.

`pyproj <https://pypi.org/project/pyproj/>`_ is also needed for ``match`` operations.
To learn more about the ``match`` operator, refer to the :doc:`query syntax <query_syntax>`.

Using pip
---------

`Python package <https://pypi.org/project/projpicker/>`_

Installation with pip is the recommended way to install both the CLI appliction and the Python module.

.. code-block:: shell

    pip3 install projpicker

    # or if you're not a root
    pip3 install --user projpicker

    # to install development versions
    pip3 install --pre projpicker

    # or if you're not a root
    pip3 install --pre --user projpicker

From source
-----------

The current development version of ProjPicker can be downloaded and installed from source `here <https://github.com/HuidaeCho/projpicker>`_.
Use pip to install ProjPicker from the source directory.

.. code-block:: shell

    git clone https://github.com/HuidaeCho/projpicker.git
    cd projpicker
    pip3 install -e .
