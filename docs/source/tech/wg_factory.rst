factory.py
===============


Define the straight and bend waveguide factories for auto-routing function in **PhotoCAD**.

#. ``StraightFactory`` : Import the straight waveguide to use it for straight connection.

#. ``CircularBendFactory`` : Import ``BendCircular`` from ``bend_circular`` and assigned each component to different situations.

    * Note that the default bend radius for every 90-degree bend used for auto-routing is set to a recommended value of 80 um / 50 um, depending on the waveguide type. However, users should define the bend radius themselves to meet the design requirements.

#. ``EulerBendFactory`` : Import ``BendEuler`` from ``bend_euler`` and assigned each component to different situations.

    * Note that the default bend radius for every 90-degree bend used for auto-routing is set to a recommended value of 80 um / 50 um, depending on the waveguide type. However, users should define the bend radius themselves to meet the design requirements.

