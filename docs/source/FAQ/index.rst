Frequently Asked Questions (FAQ)
========================================

This section summarizes common issues and adjustment suggestions regarding project management, PDK import, and code compatibility between **PhotoCAD V1.7.5** and **PhotoCAD V1.7.6**.

* **Project Creation and PDK Import**

    * After upgrading to **PhotoCAD V1.7.6**, it is recommended to create a new project and import the previous PDK package for migration. This approach helps ensure better functional compatibility and file integrity.


* **Code Variable Naming Optimization**

    * PhotoCAD V1.7.6 introduces standardized variable naming for ``LayerStyle`` definitions in the ``display.py`` file under the ``technology`` folder. The previously used ``pattern`` variable must now be updated to ``stipple`` to match the new syntax. This adjustment helps developers avoid errors and compatibility issues after upgrading.

::

    # Old syntax ( PhotoCAD V1.7.5 )
    LayerStyle(fill=LayerFill(color=NamedColor.PINK, pattern=FillStipple.BACK_DIAGONAL))
    # New syntax ( PhotoCAD V1.7.6 )
    LayerStyle(fill=LayerFill(color=NamedColor.PINK, stipple=FillStipple.BACK_DIAGONAL))  # New syntax

* **Enhanced Flexibility in GDS Export Parameters**

    * In **PhotoCAD V1.7.5**, setting the ``auto_flatten=False`` parameter in the ``fp.export_gds`` function globally prevents changes in the original PDK device coordinates caused by device rotation. However, this method applies to all devices simultaneously and does not support flexible adjustment for individual devices, which may not satisfy certain specific layout requirements.
    * In **PhotoCAD V1.7.6**, the ``auto_flatten`` parameter in ``fp.export_gds`` can be configured individually for each device, allowing for flexible control of layout flattening for different devices as required. This approach provides better support for complex projects and customized device layout requirements. (Note: Device names should not be enclosed in parentheses)

::

    # Old syntax ( PhotoCAD V1.7.5 )
    fp.export_gds(library, file=gds_file, auto_flatten=False)
    # New syntax ( PhotoCAD V1.7.6 )
    fp.export_gds(library, file=gds_file, auto_flatten={pdk.ppln_wg_BB: False,pdk.edge_coupler_3p5um_y_BB: False})

*  It is recommended to consult the latest Latitudeda PDK developer manual for more practical examples and detailed instructions.




