# Oxipital Chataigne module

The [Chataigne](https://benjamin.kuperberg.fr/chataigne/en) module that controls the Oxipital engine over OSCQuery:
orb and force groups (base values and macro weights), camera link, and the sync with Unity.

It is used as a git submodule at `Chataigne/modules/Oxipital` (Chataigne loads the modules of the `modules` folder
next to a session) by:

- [Oxipital-Engine](https://github.com/Gamgie/Oxipital-Engine): light session to try the engine
- [Oxipital-Live](https://github.com/Gamgie/Oxipital-Live): the live performance session

Chataigne reloads `Oxipital.js` by itself when the file changes. The script engine is JUCE JavaScript: `var`,
`function` and plain loops only. See the "LINK WITH UNITY" comment in `Oxipital.js` before changing how syncs
are triggered: a sync is heavy on both sides and must never be started when "Is Connected" turns on.
