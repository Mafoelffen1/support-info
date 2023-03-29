## Ubuntu Forums system-info Script
The Ubuntu Forums "system-info" script queries the users computer and prepares a report, so that Ubuntu Forums Community Members can see what they are recommending solutions for. This is the 'TEST/DEV Repository for the STABLE Repository located at: https://github.com/UbuntuForums/system-info
## Details

- Creates the file `system-info.txt` at the base of the user's home directory.
- Masks all sensitive info, like IP addresses, MAC addresses, Full FQDN and Serial numbers, automatically in a meaningful way.
- The script displays the report results within the 'less' utility to review the results, one screen at a time. To navigate from there, press the space bar, left, right, up, down, page up or page down keys to navigate. If in a graphical terminal session, you can also use mouse navigation. Press the "q" key to exit "less" and continue. It will create/save the final report and offer to upload to a pastebin site.
- Offers to upload the results to the Ubuntu `pastebinit` provider if at least one-of-four programs are installed, and a sufficiently reliable internet connection is available. This is the easiest way to share the sanitized results with the Ubuntu Community for support. After successful upload to a pastebin, it will both display and log the URL of the uploaded report (`~/system-info-link.log`), for you to copy and paste in your post on the Ubuntu Forums. The user can optionally paste the results of the report to their post on Ubuntu Forum's, wrapped within 'Code' Tags.
- Future versions may have an option to create the archive `system-info.tar.gz` if the report exceeds 19.5 kB in size. (Not implemented yet.)


## Run from CLI

You can either run it from the command line (Console or Terminal Session) with these commands:

    wget -N -t 5 -T 10 https://github.com/Mafoelffen1/system-info/raw/main/system-info && \
    chmod +x system-info && \
    ./system-info

This will download the script, make it executable, and run it, all in a row.

## Run from GUI

Or, from a GUI Desktop, this way:

1. [Download][1] the script
2. In Nautilus or other file broswer, From File Properties, Permissions, Make it executable.
3. Run it from your file browser or a Run dialog from kdialog

## Install Script from Debian Package

The UbuntuForums 'system-info' Script is now available to install as a .deb package from it's PPA at:
https://launchpad.net/~mafoelffen/+archive/ubuntu/system-info

You can add this PPA to your system and install the package with:

    sudo add-apt-repository ppa:mafoelffen/system-info
    sudo apt update
    sudo apt install system-info

[1]: https://github.com/Mafoelffen1/system-info/raw/main/system-info
