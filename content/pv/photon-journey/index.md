+++
title = "A Photon's Journey Through a Solar Simulation"
date = 2026-09-04
description = "An interactive tour through a pvlib-based solar simulation."
weight = 50
+++

# A Photon's Journey Through a Solar Simulation

A virtual photon's journey from the sun through a photovoltaic simulation to
the grid.  

This simulation uses [pvlib](https://pvlib-python.readthedocs.io/) to follow
that journey from sunlight to grid-delivered electricity.  It uses sensible
values for each model choice.  It is also a reasonably simple simulation.
We could make even more steps by introducting 3D shading, terrain aware backtracktracking,
diffuse irradaince optimization, etc.

{{ photon_journey() }}

## The three sections

The journey is divided into three physical sections:

1. **Atmosphere:** solar position, air mass, water vapor, and the separation of
   measured sunlight into direct and diffuse components.
2. **DC:** rack geometry, irradiance on the module, shading, reflection,
   spectral response, cell temperature, diode behavior, degradation, and
   direct-current wiring. Use the rack-type toggle to select the tracker or
   fixed-tilt modeling path.
3. **AC:** inverter conversion, alternating-current wiring, transformer loss,
   and the final grid export limit.

Use the timeline, controls, or arrow keys to inspect individual calculations,
or let the complete journey play automatically.
