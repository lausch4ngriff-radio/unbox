# unbox - rekordbox / Serato / Traktor / VirtualDJ / Denon "Now Playing" overlays for Twitch / OBS

Display your current or recent rekordbox / serato / traktor / virtualdj / denon tracks to your viewers on Twitch. Inspired by PRACT OBS and ASOT.
<p align="center">
 <img src="https://cdn.discordapp.com/attachments/780172543771410452/783904760880562176/Screen_Shot_2020-12-02_at_7.56.55_PM.png" />
</p>

**Please back up your library before using this as corruption could occur, we're not responsible for any issues, or corruption that this software may cause to your library.**

If unbox is useful to you and you'd like to support future development, please feel free to [donate](https://paypal.me/erikrichardlarson?locale.x=en_US). Your support is much appreciated! Please send me your Twitch channel if you've supported and I'll post it here. 

**Our supporters**

<p float="left">
 <a href="https://www.twitch.tv/dj_frankwillard"><img src="https://static-cdn.jtvnw.net/jtv_user_pictures/654c4e52-c532-435e-8641-969666ce348f-profile_image-300x300.png" data-canonical-src="https://static-cdn.jtvnw.net/jtv_user_pictures/654c4e52-c532-435e-8641-969666ce348f-profile_image-300x300.png" width="80" height="80" /></a>
<a href="https://www.twitch.tv/djaramistv"> <img src="https://static-cdn.jtvnw.net/jtv_user_pictures/93f54a41-ec11-459a-885f-bb5ce4550aa9-profile_image-300x300.png" data-canonical-src="https://static-cdn.jtvnw.net/jtv_user_pictures/93f54a41-ec11-459a-885f-bb5ce4550aa9-profile_image-300x300.png" width="80" height="80" /></a>
<a href="https://www.twitch.tv/djtaylornorris"> <img src="https://static-cdn.jtvnw.net/jtv_user_pictures/d533704e-55a7-4912-b744-82e0c63e93b9-profile_image-300x300.png" data-canonical-src="https://static-cdn.jtvnw.net/jtv_user_pictures/d533704e-55a7-4912-b744-82e0c63e93b9-profile_image-300x300.png" width="80" height="80" /></a>
 <a href="https://www.twitch.tv/geoffbutler"> <img src="https://static-cdn.jtvnw.net/jtv_user_pictures/1021dfce-899d-4567-a08a-f9ea9b282770-profile_image-70x70.png" data-canonical-src="https://static-cdn.jtvnw.net/jtv_user_pictures/1021dfce-899d-4567-a08a-f9ea9b282770-profile_image-70x70.png" width="80" height="80" /></a>
  <a href="https://www.twitch.tv/reorderdj"> <img src="https://static-cdn.jtvnw.net/jtv_user_pictures/7716d257-49e5-41ec-8404-2a4883507b2a-profile_image-70x70.png" data-canonical-src="https://static-cdn.jtvnw.net/jtv_user_pictures/7716d257-49e5-41ec-8404-2a4883507b2a-profile_image-70x70.png" width="80" height="80" /></a>
</p>

## How to use
1. **Download the unbox desktop app.** Here's the mac version: [Mac Download](https://github.com/erikrichardlarson/unbox/releases/download/8.1/unbox-mac.zip) and here's the windows version: [Windows Download](https://github.com/erikrichardlarson/unbox/releases/download/8.1/unbox-windows.zip) Currently there is support for rekordbox 5 / 6, Traktor, Serato, and VirtualDJ. 

**Extra step for Traktor users only: If you're on Traktor, you also need to download this [D2 file](https://github.com/erikrichardlarson/unbox/releases/download/7.0/D2.zip), unzip and just place it in your CSI folder located at C:\Program Files\Native Instruments\Traktor Pro 3\Resources64\qml\CSI on Windows or /Applications/Native Instruments/Traktor Pro 3/Traktor.app/Contents/Resources/qml/CSI on Mac. There is a D2 folder already in this CSI directory so it's best to make a backup of that. And if you don't own a Kontrol D2, go to Controller Manager in your preferences, click Add beneath the device dropdown, and add Traktor then select Kontrol D2. I would automate this for you but permissioning makes it tricky, sorry Traktor users.**

**Denon users: Please make sure your player is online before selecting the Denon mode.**

2. **Open the unbox zip file you downloaded above, and open the unbox app, on Windows you'll want to click the unbox.exe file. When it's open just select your mode. If you select real-time rekordbox on Windows another launcher will come up, select the version of rekordbox you're on in the dropdown and click launch, please leave all other settings intact.** If Windows or Mac asks you to trust unbox, you'll need to do that. The source code is in this repo if you're concerned about security. When the app is open you'll see this window:  
<p align="center">
<img src="https://media.discordapp.net/attachments/790269915444805656/818679548815474708/Screen_Shot_2021-03-08_at_6.59.52_PM.png?width=876&height=614" data-canonical-src="https://media.discordapp.net/attachments/790269915444805656/818679548815474708/Screen_Shot_2021-03-08_at_6.59.52_PM.png?width=876&height=614" />
</p>

3. **Just keep unbox open when you're playing.** Now that unbox is open, you have access to a few things:  

*  Browser sources. The browser sources are just web pages that unbox automatically updates when it's open. The dropdown on the second step of the app gives you all available sources, on the third step of the app you can copy the link to your clipboard. For example you can add: http://localhost:8080/history.html or http://localhost:8080/asot.html. Below you can see what these browser sources look like. If rekordbox / Serato / Traktor is on a different computer than you're streaming OBS on, you can grab the IP address of the computer running unbox / rekordbox / Serato / Traktor and use that in place of localhost for your browser source urls. You'll need to have both machines on the same network to make this work. The now playing overlay could look something like this: http://192.168.0.1:8080/asot.html
 
*  Three txt files. You also have access to a "rekordbox_stream.txt" file in your home directory in a folder called unbox_output. You can add this as a text source in OBS, it updates in real time so you can display a plain text view of the current playing track. The other two files are artist.txt and track.txt which are just the artist and track separated. 

*  To use KUVO live playlists. Just paste in your user id, click get playlist, and we'll find your latest playlist.

<p align="center">
 <img src="https://media.discordapp.net/attachments/790269915444805656/802319468609011712/Screen_Shot_2021-01-22_at_3.30.39_PM.png" />
</p>
