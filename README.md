My Luau Vulnerability Learning Journey

This folder serves as a personal documentation of my progress learning Luau security. The scripts here are proof-of-concept tools I built after analyzing different Roblox games for logic flaws.

Through active testing, these are the first major Luau vulnerabilities I've learned to spot and write scripts for:

Missing Checkpoint Validation: Bypassing sequential game loops by script-teleporting to the final pad.

Unsecure RemoteEvents: Exploiting open client-to-server endpoints to programmatically spam and duplicate items.

Hunting for these specific Luau vulnerabilities is now the first thing I do when testing a game. I am still learning, sharpening my skills, and documenting my findings here as I work to become a better security researcher.
