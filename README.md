# Remove banner ad

###### Source: https://github.com/mrpond/BlockTheSpot/issues/150#issuecomment-826379721


1. Navigate to `%APPDATA%/Spotify/Apps`. Here you will find xpui.spa, make a copy of this file so that you have a backup.
2. Rename xpui.spa to xpui.zip and open the zip. Within the zip, there will be xpui.css, extract this file.
3. Open the extracted file with a text editor and search for `.b2731cdeb97c1f6a4cf5caa44e943acb-scss`. This is the css selector of the ad banner div.
4. For this selector, change the `display:flex` to `display:none`, save the file, drop it back in the zip to replace the original xpui.css.
5. Change the extension from xpui.zip to xpui.spa

The div selector did not change even after I reinstalled, so I'm guessing it should be the same for everybody.

