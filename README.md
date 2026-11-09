Optical Link Budget Calculator

This calculator checks whether a fibre-optic link has enough power to work. You give it transmit power, fibre loss, distance, and a few other loss sources. It tells you the received power, how much safety margin you have, and the maximum distance the link can reach before the signal drops below what the receiver needs. It also compares the two standard fibre wavelengths (1310 nm and 1550 nm) and shows why 1550 nm reaches almost twice as far.

Why I built this

I'm an RF satellite engineer. Link budgets are part of my day job — C/Ku-band satellite links. This project takes that same skill into optical fibre, as I build toward RF-optical satellite systems.

The equation
P_rx (dBm) = P_tx (dBm) − L_fibre (dB) − L_connectors (dB) − L_splices (dB) − M_margin (dB)
L_fibre (dB) = alpha (dB/km) × distance (km)

Unlike an RF free-space link, there's no path-loss term that grows with distance squared. Fibre guides the light instead of letting it spread, so loss is linear in distance.

Results

With a 0 dBm transmitter and −24 dBm receiver sensitivity: the link reaches about 56 km at 1310 nm, and about 98 km at 1550 nm. That gap comes from the trade-off between Rayleigh scattering and infrared absorption — 1550 nm sits near the minimum of the two.

See OpticaLinkBudget.ipynb for the full code and plots.
