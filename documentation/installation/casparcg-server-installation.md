---
description: Sofie specific fork of CasparCG Server 2.1
---

# Installing CasparCG Server for Sofie

This is a step-by-step-guide to install a fresh copy of CasparCG Server to be used together with Sofie.  
Sofie is compatible with [CasparCG Server 2.1 - NRK version](https://github.com/nrkno/tv-automation-casparcg-server/releases/) for playout.

## Hardware

**Decklink cards:** Install 1 piece of **Decklink Quad2** SDI I/O card per CasparCG Server at PCI slot 4. \(img 1\)  
Check the physical condition of the two cooling fans on the cards to make sure they are properly in place. \(img 2\)

| ![](http://confluence.nrk.no/download/attachments/70026806/IMG_0309.jpeg?version=1&modificationDate=1543924546000&api=v2) | ![](http://confluence.nrk.no/download/thumbnails/70026806/IMG_0306.jpeg?version=1&modificationDate=1543924541000&api=v2) |
| :--- | :--- |
| \(img 1\) Decklink Quad 2 in PCI slot 4 | \(img 2\) Make sure the fans are properly in place and all clips are locked. |

## PC and Windows installation

1. Wait for reboot.
2. Choose F8 to open command prompt and write `diskpart` 
   1. **Dell Precision 5820**  - "sel disk 0" → "clean"  - "sel disk 1" → "clean"  - "list disk" to check if everything is in order  - exit diskpart → exit command prompt → reboot  - Reboot
   2. **HP Z4 Workstation**  - "sel disk 0" → "clean"  - "sel disk 1" → "clean"  - "sel disk 2" → "clean"  - "list disk" to check if everything is in order  - exit diskpart → exit command prompt → reboot  - Reboot
3. BIOS
   1. **Dell Precision 5820** Flash BIOS: Boot to BIOS menu using F12 and choose "Flash BIOS". Choose the appropriate .exe-file
   2. **HP Z4 Workstation** Disable M2 disks
4. **Media Disk RAID1:** Boot to BOOT MENU using F12, select "Device Configuration".  - If the only action is "Delete" then delete the RAID0 volume.  - Select "Create RAID Volume". Set "media" as Volume Name, set RAID level to "RAID1" and select the two equal disks to create a RAID1 volume of 1TB.  - F4 to save and reboot.
5. Install Windows 10 64-bit.
6. **ClearType and rendering:**  
   Make sure ClearType is active. Make the following changes in the "Juster utseendet og ytelsen for Windows" window.

   * Set "_Adjust for best performance_” under “_Performance options_”.  
   * Enable "Font smoothing" under _"Performance options"._   \(img 1\)

   | ![](http://confluence.nrk.no/download/thumbnails/70026806/performance.png?version=1&modificationDate=1543998537000&api=v2) |
   | :--- |
   | \(img 1\) Windows appearance and performance settings |

## Windows and CasparCG configuration – common for both machine 01 and 02

1. **Disk management**  - Log on with the approriate Windows user.  - Assign `D:` as a Media disk. 
2. **nVidia:** Install latest nVidia Quadro P4000 drivers ODE, Express installation.
3. **Desktop Video** **installation:** Install Desktop video 10.8.3 \(Decklink drivers\).

   | 10.8.3 \(November 2016\) is used with Duo2 and Quad2 cards in combination with blackburst \(B/B\) reference signal. With tri-level sync or without external sync newer drivers will most likely work. Note: Not fully tested . |
   | :--- |

4. **CasparCG Server & Launcher**  
   Download latest **CasparCG Server** release from: [https://github.com/nrkno/tv-automation-casparcg-server/releases/](https://github.com/nrkno/tv-automation-casparcg-server/releases) to `C:\casparcg`  
   Extract `CasparCG\Server` to `C:\casparcg`

   i.e. `C:\casparcg\casparcg.exe`.

5. Download latest **CasparCG Launcher** release from: [https://github.com/nrkno/tv-automation-casparcg-launcher/releases](https://github.com/nrkno/tv-automation-casparcg-launcher/releases), rename it to `casparcg-launcher.exe` and add it to `C:\casparcg`.
6. **Open incoming TCP ports in the Windows firewall**  Open the following ports: 3250, 5250, 8000, 8005.
7. **Machine-specific** list of tasks as described below
8. **Run launcher**   Allow windows smart screen to run _casparcg-launcher_  _\(more info → run\)_
9. **Reboot**  Verify that everything starts and works as intended.

## Windows and CasparCG configuration – machine 01 \(Media Play-out\)

1. **Blackmagic Design Desktop Video setup** Un-pair BNC connectors for devices 1, 2, and 4. Pair the BNC connector for device 3 \(SDI5&6\). Select _1080i50_ for all 8 devices.
2. **CasparCG config** 
3. _**casparcg-launcher**_ **config**  
4. **Shortcuts** to _Caspar CG Launcher_ and TestMode, and prepare Startup Folder. Copy the _CasparCG Launcher_ shortcut to Windows' common startup folder \(Win+R, then `shell:common startup`\). 
5. **Create shared folder** Share the `D:\\media\` and give it the name `mamMediaScanner`.  
6. **Remove** _**MediaScanner**_ from _CasparCG Launcher_ in _Settings_. 
7. **FileZilla Server** Install _FileZilla Server_. Create the folder `D:\casparcg\media\mam`.  Start _FileZilla Server_, and make the following changes to settings:  - General -&gt; No Transfer timeout: 9999  - Security Settings -&gt; Disable IP check  - Miscellaneous -&gt; Start minimized  - Logging -&gt; Select "Enable logging to file", then change Logfile type to "Use a different logfile each day" and set "Delete old logfiles after XX days" to 32. And finally create the user based on user name and password in the list "FileZilla Server" in LastPass.  - Add the folder `D:\casparcg\media\mam` as the home folder.  - Give the user all rights to this folder. 

## Windows and CasparCG configuration – machine 02 \(Graphics Play-out\)

1. **media-scanner**  Latest release from [https://github.com/nrkno/tv-automation-media-scanner/releases](https://github.com/nrkno/tv-automation-media-scanner/releases) Copy over to `C:\casparcg`. 
2. **Blackmagic Design Desktop Video setup** Un-pair BNC connectors for devices 1, 3, and 4. Pair the BNC connector for device 2 \(SDI3&4\). Select _1080i50_ for all 8 devices. 
3. **CasparCG config** 
4. **casparcg-launcher config** 
5. **Batch file for mapping Z Drive** 
6. **Shortcuts** to _Caspar CG Launcher_ and TestMode, and prepare Startup Folder. Copy the _CasparCG Launcher_ shortcut to Windows' common startup folder \(Win+R, then `shell:common startup`\).
7. **Shortcuts** 

**Please note:**

* All machines must have a screen, mouse, and keyboard attached \(or a KVM or similar dummy load\). They cannot be run headless!

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>The <em>Netop</em> remote client will adversely affect the font rendering
          on CasparCG Server if not configured correctly on the client side.
          <br />It is important that this is done on each <em>Netop Guest</em> client before
          connecting to <em>CasparCG Server</em> machines.</p>
        <p>Click the connection settings icon to open settings window.
          <br />Change the follwing settings in &quot;Netop Guest&quot; application:</p>
        <ol>
          <li>Change Desktop setting &quot;Optimize screen transfer&quot; to &quot;Never&quot;.
            <br
            />
            <img src="http://confluence.nrk.no/download/thumbnails/70026806/Netop%20Guest%2006.12.2018%2013_50_57.png?version=1&amp;modificationDate=1544101992000&amp;api=v2"
            alt/>
          </li>
          <li>Change the &quot;Mouse&quot; setting to &quot;Local mouse&quot;.
            <br />
            <img src="http://confluence.nrk.no/download/thumbnails/70026806/Netop%20Guest%2006.12.2018%2013_51_12.png?version=1&amp;modificationDate=1544102043000&amp;api=v2"
            alt/>
          </li>
        </ol>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>