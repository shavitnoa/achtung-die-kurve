# Achtung, die Kurve!

Revived HTML5 and Javascript version of the Flash game "Achtung, die Kurve!" (beware, (of) the curve!). Hope you enjoy!

## About this version

**The Problem:** Players with the `g_robot` powerup (square head, 90° turns) died "randomly."

This version fixes the robot powerup's random self-kills. The front collision probe sat only a fraction of a pixel beyond the player's own head cap, which is drawn each frame before the collision check — so sub-pixel rounding and antialiased pixels could make the probe read the player's own head as a collision, killing robots while turning or even driving straight. The fix uses a 1.5× front probe in robot mode (and during a few grace frames after the powerup expires) so the probe always clears the head; walls and other trails behave exactly as before.

Play it here: [https://shavitnoa.github.io/achtung-die-kurve/](https://shavitnoa.github.io/achtung-die-kurve/)

Based on the original project at [https://achtung.life](https://achtung.life)

Licence: MIT
