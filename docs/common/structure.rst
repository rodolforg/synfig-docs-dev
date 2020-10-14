.. _structure:

Code structure
===============


Overview
--------

Synfig is divided into three components: ETL, synfig-core and synfig-studio.

* **ETL** is a template library that implements reference counting, portable threading and other low-level stuff. Every part of the Synfig project uses ETL in some way. It is like the C++ STL.
* **synfig-core** is Synfig's backend. It renders scenes and knows how to read and write Synfig XML files. This directory contains the Synfig library and the Synfig command-line tool. 
* **synfig-studio** is the graphical editor. It uses the GTK+ widget library. If you want to hack on the interface, this is what you should look at.

The structure of **synfig-core** is:

* ``synfig-core/src/synfig/`` - Code of **"libsynfig"** library. This is actually the main part of synfig-core. It contains code of render engine and routines for reading/writing Synfig's files. The **libsynfig** library is used by all other Synfig's components.
* ``synfig-core/src/modules/`` - Functionality of **libsynfig** can be extended with modules and this directory is a place for them. A module can do following things:
   * Add support for importing specific file format(s). Examples:
      * ``synfig-core/src/modules/mod_png/mptr_png.cpp``
      * ``synfig-core/src/modules/mod_bmp/mptr_bmp.cpp``
   * Add support for exporting (rendering) to specific file format(s). Examples:
      * ``synfig-core/src/modules/mod_png/trgt_png.cpp``
      * ``synfig-core/src/modules/mod_gif/trgt_gif.cpp``
   * Implement a layer type(s). Examples:
      *  ``synfig-core/src/modules/mod_geometry/circle.cpp`` - Circle Layer
      *  ``synfig-core/src/modules/lyr_freetype/lyr_freetype.cpp`` - Text Layer
      *  ``synfig-core/src/modules/mod_noise/distort.cpp`` - Noise Distort Layer	 
   * Implement a **valuenode** (see below on valuenodes). Example:
      * ``synfig-core/src/modules/mod_noise/valuenode_random.cpp``
* ``synfig-core/src/tool/`` - Code of synfig command-line tool (binary is simply called ``synfig``). It uses **libsynfig** to read Synfig files and render them in any supported format.

Main components of **synfig-studio**:

- ``synfig-studio/src/synfigapp/`` - Code of **libsynfigapp** library. This is a layer between GUI and **libsynfig** (from synfig-core). It contains code for **actions** - operations that transform loaded Synfig's file in some way. When user makes some change to Synfig file in GUI, then an *action* is called that does the actual modification.
- ``synfig-studio/src/gui/`` - Code of GUI written in GTKmm. This defines how application looks and behave.



So, we have following structure:

::

  gui ---> libsynfigapp -------> libsynfig
  
             synfig-cli -------> libsynfig


.. toctree::
   :maxdepth: 1
   :glob:

   structure/*
