Filtering results
=================

Shell
-----

.. code-block:: shell

    # projected CRSs only
    projpicker 34.2348,-83.8677 33.7490,-84.3880 | grep "^projected_crs"

    # CRSs in meter only
    projpicker 34.2348,-83.8677 33.7490,-84.3880 | grep "|meter|"

Python
------

.. code-block:: python

    import projpicker as ppik

    # sorted by area to find the most local CRS first
    bbox = ppik.query_points([[34.2348, -83.8677], [33.7490, -84.3880]])

    # projected CRSs only
    bbox_proj = list(filter(lambda x: x.proj_table=="projected_crs", bbox))
    ppik.print_bbox(bbox_proj)

    # CRSs in meter only
    bbox_meter = list(filter(lambda x: x.unit=="meter", bbox))
    ppik.print_bbox(bbox_meter)

GUI
---

.. figure:: projpicker_gui.png
   :align: center
   :alt: GUI for selecting a subset of queried results

   GUI for selecting a subset of queried results

Shell
^^^^^

The ``-g`` (``--gui``) option launches a tkinter-based GUI for selecting a subset of queried results.
Geometries and other options still need to be passed from the command line:

.. code-block:: shell

    # projected CRSs only
    projpicker -g 34.2348,-83.8677 33.7490,-84.3880

Python
^^^^^^

.. code-block:: python

    import projpicker as ppik

    bbox = ppik.query_points([[34.2348, -83.8677], [33.7490, -84.3880]])

    # start GUI
    bbox = ppik.gui.select_bbox(bbox)
