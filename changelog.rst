Changelog
=========

Last change: 22-OCT-2023 MTS

0.6.3 - 0.6.5
-------------
- Dependencies updated
- Bug fixes due to Python 3.10 and PyQt5 (listed below)
- Fix RCC error for Render GUI (one click installer) (remove tqdm from GUI)
- Fix save pick properties bug in Picasso Render GUI (one click installer)
- Fix render render properties bug in Picasso Render GUI (one click installer)
- Fix animation building in Picasso Render GUI (one click installer)
- Fix test clusterer HDBSCAN bug
- Fix .nd2 localized files info loading (full loader changed to unsafe loader)
- Fix rare bug with pick similar zero division error

0.6.2
-----
- Picasso runs on Python 3.10 (jump from Python 3.7-3.8)
- New installation instructions
- Dependencies updated, meaning that M1 should have no problems with old versions of SciPy, etc.
- Localize: arbitrary number of sensitivity categories
- Picasso Render legend displays larger font
- Picasso Render Test Clusterer displays info when no clusters found instead of throwing an error
- Calling clustering functions from ``picasso.clusterer`` does not require camera pixel size. Same applies for the corresponding functions in CMD. *Only if 3D localizations are used, the pixel size must be provided.*
- HDBSCAN is installed by default since it is distributed within the new version of ``scikit-learn 1.3.0``
- Screenshot ``.yaml`` file contains the list of colors used in the current rendering
- Render scale bar allows only integer values (i.e., no decimals)
- Localize .ims file fitting bug solve

0.6.1
-----
- **Measuring in the 3D window (Measure and Scalebar) fixed (previous versions did not convert the value correctly)**
- Localize GUI allows for numerical ROI input in the Parameters Dialog
- Allow loading individual .tif files as in Picasso v0.4.11``
- RESI localizations have the new column ``cluster_id``
- Building animation shows progress (Render 3D)
- Export current view in Render saves metadata; An extra image is saved with a scalebar if the user did not set it
- (**Not applicable in 0.6.2**) Clustering in command window requires camera pixel size to be input (instead of inserting one after calling the function)
- Bug fixes

0.6.0
-----
- New RESI (Resolution Enhancement by Sequential Imaging) dialog in Picasso Render allowing for a substantial resolution boost, (*Reinhardt, et al., Nature, 2023.* DOI: 10.1038/s41586-023-05925-9)
- **Remove quantum efficiency when converting raw data into photons in Picasso Localize**
- Input ROI using command-line ``picasso localize``, see `here <https://picassosr.readthedocs.io/en/latest/cmd.html>`_.

0.5.7
-----
- Updated installation instructions
- (H)DBSCAN available from cmd (bug fix)
- Render group information is faster (e.g., clustered data)
- Test Clusterer window (Render) has multiple updates, e.g., different projections, cluster centers display
- Cluster centers contain info about std in x,y and z
- If localization precision in z-axis is provided, it will be rendered when using ``Individual localization precision`` and ``Individual localization precision (iso)``. **NOTE:** the column must be named ``lpz`` and have the same units as ``lpx`` and ``lpy``.
- Number of CPU cores used in multiprocessing limited at 60
- Updated 3D rendering and clustering documentation
- Bug fixes

0.5.5-6
-------
- Cluster info is saved in ``_cluster_centers.hdf5`` files which are created when ``Save cluster centers`` box is ticked
- Cluster centers contain info about group, mean frame (saved as ``frame``), standard deviation frame, area/volume and convex hull
- ``gist_rainbow`` is used for rendering properties
- NeNA can be calculated many times
- Bug fixes

0.5.1-4
-------
- Sensitivity is a float number in Server: Watcher
- One-click-installer available
- Bug fixes

0.5.0
-----
- 3D rendering rotation window
- Multiple .hdf5 files can be loaded when using File->Open
- Localizations can be combined when saving
- Render window restart (Remove all localizations)
- Multiple pyplot colormaps available in Render
- View->Files in Render substantially changed (many new colors, close button works, etc)
- Changing Render's FOV with W, A, S and D
- Render's FOV can be numerically changed, saved and loaded in View->Info
- Pick similar is much faster
- Remove localization in picks
- Fast rendering (display a fraction of localizations)
- .txt file with drift can be applied to localizations in Render
- New clustering algorithm (SMLM clusterer)
- Test clusterer window in Render
- Option to calculate cluster centers
- Nearest neighbor analysis in Render
- Numerical filter in Filter
- New file format in Localize - .nd2 
- Localize can read NDTiffStack.tif files
- Docstrings for Render
- `Plugins <https://picassosr.readthedocs.io/en/latest/plugins.html>`_ can be added to all Picasso modules
- Many other improvements, bug fixes, etc.


0.4.6-10
--------
- Logging for Watcher of Picasso Server
- Mode for multiple parameter groups for Watcher
- Fix for installation on Mac systems
- Various bugfixes


0.4.2-5
-------
- Added more docstrings / documentation for Picasso Server
- Import and export for handling IMS (Imaris) files
- Fixed a bug where GPUFit was greyed out, added better installation instructions for GPUfit
- More documentation
- Added dockerfile


0.4.1
-----
- Fixed a bug in installation


0.4.0
-----
-  Added new module "Picasso Server"