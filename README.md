# Disable auto update

###### Source: https://www.youtube.com/watch?v=lPUFzDes_Eg

Works for version 1.1.62 [LINK TO DOWNLOAD](https://spotify.en.uptodown.com/windows/download/3764443) from uptodown.com

1. Uninstall Spotify
2. Delete Spotify folder from `%appdata%` locations:
    * AppData\Roaming
    * AppData\Local
    * AppData\Local\Packages (if applicable, if not, move to next step)
3. Download and Install 1.1.62 version
4. Start Spotify but **DO NOT LOG IN**
5. Create and make **READ ONLY** a `Spotify_new.exe` file in `AppData\Roaming\Spotify` directory
6. Create and **DENY all permissions** from *all users* to `Update` folder in `AppData\Local\Spotify` directory
7. Log in with Remember me checked.

### How to undo
1. Navigate to `AppData\Local\Spotify` directory
2. Undo permissions changes to `Update` folder

<br>

# Remove banner ad

###### Source: https://github.com/mrpond/BlockTheSpot/issues/150#issuecomment-826379721


1. Navigate to `%appdata%\Spotify\Apps`. Here you will find xpui.spa, make a copy of this file so that you have a backup.
2. Rename xpui.spa to xpui.zip and open the zip. Within the zip, there will be xpui.css, extract this file.
3. Open the extracted file with a text editor and search for `.b2731cdeb97c1f6a4cf5caa44e943acb-scss`. This is the css selector of the ad banner div.
4. For this selector, change the `display:flex` to `display:none`, save the file, drop it back in the zip to replace the original xpui.css.
5. Change the extension from xpui.zip to xpui.spa

The div selector did not change even after I reinstalled, so I'm guessing it should be the same for everybody.
