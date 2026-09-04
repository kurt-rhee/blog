+++
title = "A Photon's Journey Through a Solar Simulation"
date = 2026-09-04
description = "An interactive tour through a pvlib-based solar simulation."
weight = 50
+++

# A Photon's Journey Through a Solar Simulation

A photovoltaic performance model does much more than turn sunlight into an
energy estimate. It follows a chain of physical calculations from conditions
above the atmosphere to the power delivered at the grid connection.

This simulation uses [pvlib](https://pvlib-python.readthedocs.io/) to follow
that journey from sunlight to grid-delivered electricity.

{{ photon_journey() }}

## The three sections

The journey is divided into three physical sections:

1. **Atmosphere:** solar position, air mass, water vapor, and the separation of
   measured sunlight into direct and diffuse components.
2. **DC:** tracker geometry, irradiance on the module, shading, reflection,
   spectral response, cell temperature, diode behavior, degradation, and
   direct-current wiring.
3. **AC:** inverter conversion, alternating-current wiring, transformer loss,
   and the final grid export limit.

Use the timeline, controls, or arrow keys to inspect individual calculations,
or let the complete journey play automatically.
