# SaveNexus
A personal online save collection that supports multiple emulators

Runs on python 8.8

How It Works
Desktop App (PyQt5) runs on your computer with an embedded HTTP server (port 8765) that:

Scans your PSP saves and save states
Provides REST API endpoints
Launches PPSSPP with your selected game/save state

Web Dashboard (Flask) runs separately (port 5000) and:

Shows your game library in a browser
Works from any device on your network
Communicates with the desktop app via API calls

Both interfaces stay in sync and control the same PPSSPP installation.
Quick Start

Update your files with the code from the artifacts
Install dependencies: pip install Flask flask-cors
Run desktop app: python gui/app_gui.py (starts API server automatically)
Run web dashboard: python gui/web_app.py (in separate terminal)
Open browser: http://localhost:5000

The desktop app MUST be running for the web dashboard to work, since it provides the local agent API that actually launches games.
