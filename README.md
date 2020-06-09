# i-sow
Seed Linux ISO torrents by adding new torrents soon after they're created (would probably also work for other torrents).

# Usage

Download torrents using:

    <install-path>/i-sow <URL>

For example:

    /home/user/Downloads/i-sow/i-sow https://archlinux.org/download/

This will look for magnet links first, then .torrent file.  If multiple are
found you can add an extra argument to specify a unique substring of the desired
URI that should be selected.

# Regularly Checking

Using `crontab -e` you can add the following line to check for an updated iso
torrent nightly at 1 AM:

    0 1 * * * <install-path>/i-sow <download-url>

# Dependencies

- lynx (https://lynx.browser.org/)

