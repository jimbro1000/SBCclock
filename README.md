# Clock Card for HD6309SBC #

This board provides a variety of divided clock signals
to the 6809SBC board.

Where the SBC board calls for a quadrature clock (for
the 6809E variants) the board also provides Q and E.

The design is intended to be swappable to permit
easy exchange of different clock rates or different
clock generator designs.

The intended target is a raw clock of 25.175MHz to
facilitate a VGA signal. The CPU then operates at
one eighth of that - 3.15MHz, slightly above the
expected clock maximum for a C-class processor but
well within tolerance.

By having a swappable clock card the target 
operating frequency can be halved again to allow
the use of B-class processors while retaining
the 25MHz VGA signal. Again this is slightly
above specification at 1.57MHz but within the
tolerance of the design.

## Outputs ##

The card must provide the raw clock on Clock24, this
can be any frequency (that the CPUs support) but 
changing from the VGA clock frequency will require a
different approach to video output.

Outputs are then expected for the clock divided by
2, 4, 8 and 16 (Clock12, Clock6, Clock3 and Clock1.5)

Where Q and E are used they are output along with the
inverse of each.