auto_transition.py
====================

Define the transition between two waveguide type.

In **IOPTEE SiN TFLN** an taper will be added between two same type of waveguides with different width.

For the connection between two waveguide types, fixed black box transitions have been configured by default. These transitions are provided by **IOPTEE**, and will be added automatically when auto-routing is called for different waveguide types.

Users are allowed to define the taper and set ``DEFAULT`` to their own specific transition policy. Please see ``gpdk > components > transition`` for more examples.

