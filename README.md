# Firefox to transmission-daemon
Just a little script to use in conjuntion with transmission-cli and firefox to add new torrents on those sites which download button is a php function and you can't use any firefox extension like [Torrent to Web](https://github.com/DASPRiD/Torrent-to-Web) and forces you to download the torrent file and then upload to your transmission-daemon.

**IMPORTANT** 

This script is intended to use in computers where you DON'T have Transmission installed, but you want to send it to your REMOTE Transmission instance.

# Prerequisites
- Bash
- Transmission-cli
- GNU/Linux desktop. (Other OSes with bash and transmission-cli should work as well)

# Usage
Once downloaded the script you'll need to modify the credentials and the URL of your transmission-daemon accordingly. If your daemon doesn't use crendentials, remove the `-n username:password` parameter.

**IMPORTANT** 

If you have credentials, as those will be in clear text, change the persmission so anyone can't look then content of the script
```
chmod 0600 add2transmission 
```
Copy this script into a executables PATH (i.e.: `/usr/bin` or `/usr/local/bin`)

# Configure Firefox to use the script for open .torrent files and magnet 
Addin a new file extension handler in Firefox can be tricky, here official documentation [explains how to do it](https://support.mozilla.org/en-US/kb/change-firefox-behavior-when-open-file#w_adding-download-actions).
Basically, when Firefox ask for an application to open the .torrent file, you assign whatever application (like kate or gedit) and the reassign to add2transmission.
Next time you click on a torrent button on the web, it will be sent to your transmission-daemon remote server.

# Commits are welcome
I did this because I'm lazy to download torrents and upload to my transmission-daemon. If you feel this can be improved (as I feel), please do a PR. Changes like improved security, ask for confirmation to upload or anything interesting are welcome.

Enjoy!
