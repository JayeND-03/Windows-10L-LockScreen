# Prerequisites
  - The device you're testing this on is NOT your main. I won't be responsible for bricking your device or any related issues as you've been warned.
 - Your system is running Windows 11 21H2 (22000.194) or above. (Older builds including leaked ones already had the OG lock screen)
 - Windows Update is recommended to be paused/stopped completely to prevent tweaks from breaking.
 - Widgets should be turned off for original look and feel.
# Installation
Last updated: November-2026
## General
 1. Install [Windhawk](https://windhawk.net/)
 2. Look for the mod "Windows 11 Start Menu Styler" BY **m417z**, it often appears in the ★Featured Mods section, or just look it up in the search box.
 3. Click on "**Details**" button
 4. **DON'T** click "Install" *unless* you want to customize your Windows further later, click "**Fork**" to enter Editing mode.
 5. mod.wh.cpp will show up, on **line 3** // @name , change "Windows 11 Start Menu Styler - Fork" to your desirable name, like "Custom LS".
 6. Click "**Compile Mod**" button and wait for it to compile the forked mod.
 7. After the mod is compiled successfully, click "**Exit Editing Mode**" to go back to the Home page. The mod *should now be* in the Installed Mods section as local.
 8. Click on "**Details**" once again.
 9. NOW, go to "**Advanced**" tab, scroll down to "Custom process **inclusion** list"
 10. Type in **LockApp.exe** (select to quickly copy), then "**Save**"
 11. Scroll down further and enable 2 options:
- **Ignore mod inclusion/exclusion lists**
- **Consider inclusion list patterns for critical system processes**

From Step 12, quickly check your Windows version by either go to Settings > System > About > Windows Info or Ctrl+R > winver, then choose the proper YAML codes for your system.
## For Windows 11 [KB5064093](https://blogs.windows.com/windows-insider/2025/08/22/announcing-windows-11-insider-preview-build-26120-5761-beta-channel/) (Dev 26200.5761 / Beta 26120.5761) and above
From this build, Microsoft redesigned battery icon with percentage on the lockscreen, and added a tray to the network icon and it. [[Reference image]](https://winblogs.thesourcemediaassets.com/sites/44/2025/08/lock-screen-battery-icon2.png)

12. Copy this YAML code within this file: [W10-LS.yaml](https://github.com/JayeND-03/Windows-10L-LockScreen/blob/main/YAML%20codes/For%20Windows%2011%20KB5064093%20&%20above/W10L-LS.yaml)
13. Back to Windhawk, go to "**Settings**" tab, click on the "**Textual mode**" button to switch to Textual mode
14. Paste the code in the box and click "**Save settings**"
## For Windows 11 21H2 to below KB5064093
On older build of Windows 11, lock screen didn't change much except the Date&Time, login screen. On build [22543](https://blogs.windows.com/windows-insider/2022/01/27/announcing-windows-11-insider-preview-build-22543/), Microsoft updated the media flyout with only new icons and rounded corners [[Reference image]](https://blogs.windows.com/wp-content/uploads/prod/sites/44/2022/01/mct-lock.png). From build [22635.4082](https://blogs.windows.com/windows-insider/2024/08/26/announcing-windows-11-insider-preview-build-22635-4082-beta-channel/), they redesigned the media flyout to match the WinUI3 design. [[Reference image]](https://blogs.windows.com/wp-content/uploads/prod/sites/44/2024/08/media-controls-lock-screen-content-1024x640.png)

12. Copy this YAML code within this file: [W10-LS-legacy.yaml](https://github.com/JayeND-03/Windows-10L-LockScreen/blob/main/YAML%20codes/For%20Windows%2021H2%20to%20below%20KB5064093/W10L-LS-legacy.yaml)
13. Back to Windhawk, go to "**Settings**" tab, click on the "**Textual mode**" button to switch to Textual mode
14. Paste the code in the box and click "**Save settings**"
## Done!
You can now behold the classic Lock Screen by pressing Windows+K, it's advisable to restart your computer for the tweaks to be fully applied.
