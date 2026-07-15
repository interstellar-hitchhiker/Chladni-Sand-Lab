CHLADNI SAND LAB
================

Files
-----
index.html            Main app (all interface, simulation, audio and controls)
manifest.webmanifest  PWA installation metadata
sw.js                 Offline application shell
icon-192.png          App icon
icon-512.png          App icon

Quick test
----------
The classic patterns and tone generator can be tested by opening index.html.
Microphone access, tab-audio capture and PWA installation generally require HTTPS or localhost.

Recommended publishing route
----------------------------
1. Upload every file in this folder to one GitHub repository.
2. In the repository, open Settings > Pages.
3. Publish from the main branch/root folder.
4. Open the resulting HTTPS GitHub Pages URL.
5. Approve microphone permission when using live voice mode.

Local test with Python
----------------------
Open a terminal in this folder and run:

python -m http.server 8000

Then visit:
http://localhost:8000

How the simulation works
------------------------
The app calculates idealised square-plate vibration modes. Virtual grains are agitated more strongly away from nodal lines and migrate down the calculated vibration-energy gradient toward those nodes. Microphone and audio modes estimate a dominant frequency and blend between nearby virtual modes.

Important scientific limitation
-------------------------------
This is a physics-informed visual simulation, not a calibrated model of one particular metal plate. Real Chladni figures depend on geometry, thickness, material, mounting, excitation point and boundary conditions.
