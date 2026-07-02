auto_link.py
=============

Define the auto link policies between two waveguide type.

For example:

``(type(WG.RIB1.C.WIRE) >> type(WG.RIB1.C.WIRE), fpt.StraightPrefer(WG.RIB1.C.WIRE), fpt.BendURIB1g(WG.RIB1.C.WIRE.BEND_EULER))``

It means that when the start and end waveguide are both ``WG.RIB1.C.WIRE``, the automated waveguide type for routing will be ``WG.RIB1.C.WIRE`` and an automated bend ``WG.RIB1.C.WIRE.BEND_EULER`` will be added.


Users are allowed to define and set ``DEFAULT`` to their own specific linking policy.

