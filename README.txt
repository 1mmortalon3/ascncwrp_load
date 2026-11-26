ASCENDANCY NETWORKS — REPUBLIC UPLINK
Animated Garry's Mod loading screen

INSTALL
1. Extract this ZIP. Upload index.html to a public static web host, for example
   https://your-domain.example/loading/index.html (replace with your real URL).
   The image, styles, and JavaScript are embedded; no other files are required.
2. In your GMod server's garrysmod/cfg/autoexec.cfg, add or replace:
   sv_loadingurl "https://your-domain.example/loading/index.html"
3. Restart the server or run the same command in its server console. Join to test.
   The page must be accessible by connecting clients; a game server directory
   alone is not a web host. Keep FastDL settings separate.

PREVIEW
Open index.html locally in a browser for a clearly labeled simulated session.
To preview a hosted copy append ?demo=1. Do not include this in sv_loadingurl.
Real GMod callbacks automatically stop the preview simulation.

CUSTOMIZE
Open index.html in a plain-text editor. Search for EDITABLE SETTINGS near the
bottom of the file. CONFIG contains the brand, operation name, rain toggle and
rotating tips. The HTML above it contains headings and interface labels. The
background is the original supplied image embedded as a JPEG data URL.
The page contains no music, external requests, analytics, or dependencies.
The emblem is Republic-inspired; the branding is editable.

PROGRESS
The loading bar represents file synchronization, not overall game startup.
It displays an indeterminate animation until both file counts are received.
GameDetails, SetFilesTotal, SetFilesNeeded, DownloadingFile and SetStatusChanged
are implemented as global functions. No Steam ID is displayed or stored.

TESTING
Tested with desktop Chromium, simulated callbacks, several screen resolutions,
and animated rain frame changes. Not tested inside an actual GMod client.
Official setup/callback documentation: https://wiki.facepunch.com/gmod/Loading_URL

UPDATE: Original supplied Republic SVG embedded in index.html. Lower 16% of viewport (minimum 120px on normal displays, 96px on shorter displays, 76px on very short displays) reserved for native GMod loading UI. Actual engine overlay placement must be checked in game.

V3: Explicit top/left/right/bottom offsets for GMod browser compatibility.
Larger logo, headings, deployment manifest and progress panel. Main UI spans
92% of viewport width. Bottom 13% (105px for displays 780px high or less;
76px for 550px high or less) remains clear for engine loading UI.
Re-test in the actual GMod client after replacing the hosted file.
