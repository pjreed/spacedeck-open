# Spacedeck Open

This is the free and open source version of Spacedeck, a web based, real time, collaborative whiteboard application with rich media support. Spacedeck was developed in 6 major releases during Autumn 2011 until the end of 2016 and was originally a commercial SaaS. The developers were Lukas F. Hartmann (mntmn) and Martin Güther (magegu). All icons and large parts of the CSS were designed by Thomas Helbig (dergraph).

As we plan to retire the subscription based service at spacedeck.com in May 2018, we decided to open-source Spacedeck to allow educational and other organizations who currently rely on Spacedeck to migrate to a self-hosted or local version.

We appreciate filed issues, pull requests and general discussion.

# Features

- Create virtual whiteboards called *Spaces* with virtually unlimited size
- Drag & drop images, videos and audio from your computer or the web
- Write and format text with full control over fonts, colors and style
- Draw, annotate and highlight with included graphical shapes
- Turn your Space into a zooming presentation
- Collaborate and chat in realtime with teammates, students or friends
- Share Spaces on the web or via email
- Export your work as printable PDF or ZIP

# Data Import from Spacedeck.com

Spacedeck Open has a data import feature that you can use to migrate your ZIP export from Spacedeck.com.

1. To import, first drop your downloaded ZIP file in the spacedeck root folder.
2. Navigate to *Account / Profile* in your local Spacedeck Open application (person icon in the top right corner).
3. On the bottom of the page, click the *Import* button next to the ZIP file name.
4. Wait until console output has finished.

# Requirements, Installation

Spacedeck uses the following major building blocks:

- Node.js 9.x: Web Server / API. Download: https://nodejs.org
- Vue.js: Frontend UI Framework, included
- SQLite, included

It also has some optional binary dependencies for advanced media conversion:

- ffmpeg and ffprobe for video/audio conversion. Download: https://www.ffmpeg.org/download.html
- audiowaveform for audio waveform rendering. Download: https://github.com/bbcrd/audiowaveform
- ghostscript for PDF import. Download: https://www.ghostscript.com/download/gsdnld.html

By default, media files are uploaded to the ```storage``` folder.
The database is stored in ```database.sqlite``` by default.

To use Spacedeck, you only need Node.JS 9.x.

Then, to install all node dependencies, run

    npm install

To rebuild the frontend CSS styles (you need to do this at least once):

    gulp styles

# Configuration

See [config/default.json](config/default.json)

# Run (web server)

    node spacedeck.js

Then open http://localhost:9666 in a web browser.

# Run (desktop app with integrated web server)

    electron .

# License

The Spacedeck logo and brand assets are registered trademarks of Spacedeck GmbH. All rights reserved.

Spacedeck Open source code is released under the GNU Affero General Public License Version 3 (GNU AGPLv3).

    Spacedeck Open - Web-based Collaborative Whiteboard For Rich Media
    Copyright (C) 2011-2018 Lukas F. Hartmann, Martin Güther
    Icons and original CSS design copyright by Thomas Helbig
    
    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU Affero General Public License as
    published by the Free Software Foundation, either version 3 of the
    License, or (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU Affero General Public License for more details.

    You should have received a copy of the GNU Affero General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
