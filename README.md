This repository documents my learning journey in Luau security, focusing on client-server trust boundaries and game logic vulnerabilities. Inside are proof-of-concept scripts demonstrating flaws discovered during live analysis.

⚠️ Disclaimer: Created strictly for educational and security research purposes.

🛠️ Tools Used
Analysis: Dex Explorer (DataModel inspection) & Remote Spies (rspy/sspy for network sniffing)

Execution: Runtime executors to test server-side validation

🔍 Vulnerability Index
1. Level & Requirement Bypass
The Flaw: The server trusts the client's position or map access rules. Players can bypass level gates, teleport directly to the final map, and loop the sequence for infinite wins.

Fix: The server must independently verify a player's actual level and prerequisites before awarding wins or updating their location.

2. Item Duplication (Unsecured RemoteEvents)
The Flaw: Server-side listeners blindly process network requests (like item spawning or asset updates) without verifying if the player actually owns the item.

Fix: Never trust client network arguments. Enforce strict server-side inventory verification and rate limits on all events.
