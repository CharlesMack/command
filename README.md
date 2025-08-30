# central-command
The P.O.P.S. Command Center is the central hub for the Professional Production Mobile (P.O.P.S.) ecosystem, hosting the official AppDrop catalog at https://charlesmack.github.io/command/appdrops/index.html. Designed to support the P.O.P.S. interface (OnePagerMiniOS).

P.O.P.S. Command Center
The P.O.P.S. Command Center is the central hub for the Professional Production Mobile (P.O.P.S.) ecosystem, hosting the official AppDrop catalog at https://charlesmack.github.io/command/appdrops/index.html. Designed to support the P.O.P.S. interface (OnePagerMiniOS), the Command Center provides a curated list of production-focused AppDrops that users can sync to their P.O.P.S. interface for offline-first, user-sovereign productivity. The Command Center ensures seamless distribution of tools for professionals, maintaining a lightweight, reliable, and extensible platform.
Features

AppDrop Catalog: Hosts a comprehensive list of 33+ AppDrops, accessible via /command/appdrops/index.html, for syncing with the P.O.P.S. interface.
Sync Integration: Enables the P.O.P.S. interface to fetch new AppDrops when online, with local caching for offline use.
Minimalist Design: Static HTML with a glassmorphic UI, consistent with the P.O.P.S. aesthetic, for fast loading and easy maintenance.
Extensible: Easily updated to include new AppDrops, supporting the evolving needs of production professionals.
Open Source: Built for community contributions to enhance the AppDrop ecosystem.

Installation
Prerequisites

A GitHub account and repository access (e.g., charlesmack/command or charlesmack/OnePagerMiniOS).
GitHub Pages enabled for hosting the Command Center.
A modern web browser (Chrome, Safari, Firefox, or Edge).

Setup

Clone the Repository:
git clone https://github.com/charlesmack/command.git
cd command

Note: If the Command Center is a subdirectory of OnePagerMiniOS, adjust the path accordingly:
git clone https://github.com/charlesmack/OnePagerMiniOS.git
cd OnePagerMiniOS/command


Verify Directory Structure:Ensure the following files are present:

index.html: The Command Center landing page.
appdrops/index.html: The AppDrop catalog.


Enable GitHub Pages:

Go to the repository’s Settings > Pages on GitHub.
Set the source to the main branch (or gh-pages if used).
Confirm the site is live at https://charlesmack.github.io/command/ and the AppDrop catalog at https://charlesmack.github.io/command/appdrops/index.html.


Deploy Updates:

Make changes to index.html or appdrops/index.html.
Commit and push to the repository:git add .
git commit -m "Update Command Center and AppDrop catalog"
git push origin main





Usage

Access the Command Center:

Open https://charlesmack.github.io/command/ in a web browser to view the landing page.
Navigate to https://charlesmack.github.io/command/appdrops/index.html to see the AppDrop catalog.


Sync with P.O.P.S.:

Open the P.O.P.S. interface at https://charlesmack.github.io/OnePagerMiniOS/.
Go to the Settings panel (⚙️ icon in the dock).
Click Sync AppDrops when online to fetch the latest apps from the Command Center’s catalog.
Check the sync log for status updates (e.g., “Sync complete: 3 new AppDrops added”).
New AppDrops will appear in the P.O.P.S. home grid, cached in localStorage for offline use.


Browse AppDrops:

The catalog at /command/appdrops/index.html lists all available AppDrops with links to their respective pages.
Use the catalog to explore or manually access AppDrops, though syncing via P.O.P.S. is recommended for integration.



AppDrop Catalog
The Command Center hosts the following 33 AppDrops, designed for professional production tasks:

Atlas (🌍): Geospatial visualization tool for mapping and navigation.
Aurora (🌌): Creative design suite for visual storytelling.
Bryce Holograms (😇): 3D holographic production app for immersive visuals.
Camera Shop (🎥🏪): Camera equipment management and inventory tool.
Charles5 M (🎬): Video production tool for media workflows.
Charles5 P (📽️): Professional post-production editing suite.
Charles5 S (🎥): Streamlined video shooting and scripting app.
Charles5 SF (🎞️): Special effects editor for cinematic visuals.
Charles5 W (📺): Web-based video production and streaming tool.
Dev Editor (💻): Code editor for developers and technical workflows.
DJ Drop (🎧): Audio mixing and DJ tool for live performances.
Encyclopedia (📚): Knowledge base and reference tool for quick access.
First Aid QuickRef (🩺): Quick-reference medical guide for emergencies.
First Aid (🚑): Comprehensive first aid toolkit with detailed protocols.
FiveSeconds Cine (🎬): Short-form video editing for cinematic content.
FiveSeconds Lite (🎥): Lightweight video editor for quick cuts.
Hearsay (🗣️): Audio storytelling and podcasting tool.
Hearsay Cinema (🎭): Cinematic audio-visual narrative editor.
Magifico Room (🏠): Virtual room design and production planning tool.
Magifico Stage (🎤): Stage performance and event management app.
MPC Drop (🎮): Music production controller for beat-making.
OnePagerMiniOS (💻): Mini OS interface for lightweight workflows.
Planner Gemini (📅): Advanced event and task planning tool.
Planner Lite (🗓️): Simple, streamlined task planner.
POPS (🌟): Core P.O.P.S. app for system integration.
Retreat (🏕️): Wellness and productivity app for balanced workflows.
Scratchpad (📝): Quick note-taking tool for ideas and tasks.
Strobe (✨): Lighting control app for production environments.
Strobe HUD (💡): Heads-up display for real-time lighting adjustments.
Survivors Compass (🧭): Navigation and survival guide for field operations.
Tap Talk (💬): Real-time communication tool for team collaboration.
Media World (🗺🕹): 3D media player and interactive world explorer.
Viewria (👀): Visual media browser for asset management.

To add new AppDrops, update appdrops/index.html with new <a> tags in the format <a href="/path/to/appdrop/index.html">App Name</a>.
Contributing
We welcome contributions to expand the Command Center and AppDrop catalog! To contribute:

Fork the Repository:
git clone https://github.com/charlesmack/command.git
cd command


Create a Branch:
git checkout -b feature/your-feature-name


Make Changes:

Add new AppDrops to appdrops/index.html with proper <a> tags.
Enhance the Command Center landing page (index.html) with new features or UI improvements.
Ensure compatibility with the P.O.P.S. sync mechanism (parsing <a> tags with /appdrops/ paths).


Test Locally:

Use a local server (e.g., npx serve) to test changes.
Verify sync functionality by pointing the P.O.P.S. interface to your local or staged appdrops/index.html.
Example:npx serve

Then update the P.O.P.S. sync URL to http://localhost:5000/command/appdrops/index.html for testing.


Submit a Pull Request:

Push your branch:git push origin feature/your-feature-name


Open a pull request on GitHub with a clear description of your changes.



Development Notes

Tech Stack: Static HTML, CSS, and minimal JavaScript for the landing page and catalog.
Sync Mechanism: The P.O.P.S. interface fetches AppDrops from appdrops/index.html, parsing <a> tags with href attributes containing /appdrops/ and using text content as app names.
Design: Glassmorphic UI with a customizable accent color (default: #00ff7f), matching the P.O.P.S. interface.
P.O.P.S. Integration: The Command Center is designed to work with the P.O.P.S. interface at https://charlesmack.github.io/OnePagerMiniOS/, which caches AppDrops for offline use.
Security: AppDrop links are served as static HTML, with no server-side logic, ensuring minimal attack surface.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or support, contact the maintainer via GitHub Issues or the P.O.P.S. community at charlesmack.github.io.
