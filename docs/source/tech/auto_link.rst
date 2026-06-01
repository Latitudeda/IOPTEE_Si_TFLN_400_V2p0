auto_link.py
=============

Define the auto link policies between two waveguide type.

For example:

``(type(WG.SIN.C.WIRE) >> type(WG.SIN.C.WIRE), fpt.StraightPrefer(WG.SIN.C.WIRE), fpt.BendUsing(WG.SIN.C.WIRE.BEND_EULER))``

It means that when the start and end waveguide are both ``WG.SIN.C.WIRE``, the automated waveguide type for routing will be ``WG.SIN.C.WIRE`` and an automated bend ``WG.SIN.C.WIRE.BEND_EULER`` will be added.


Users are allowed to define and set ``DEFAULT`` to their own specific linking policy.

