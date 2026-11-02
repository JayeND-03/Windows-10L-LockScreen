
# Prerequisites
  - The device you're testing this on is NOT your main. I won't be responsible for bricking your device or any related issues as you've been warned.
 - Your system is running Windows 11 21H2 (22000.194) or above. (Older builds including leaked ones already had the OG lock screen)
 - Windows Update is recommended to be paused/stopped completely to prevent tweaks from breaking.
 - Widgets should be turned off for original look and feel.
# Installation
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

12. Copy this YAML code:
`theme: Windows 10L
disableNewStartMenuLayout: ''
styleConstants:
  - ''
controlStyles:
  - target: StackPanel#TimeAndDatePanel
    styles:
      - Orientation=Vertical
      - VerticalAlignment=Bottom
      - HorizontalAlignment=Left
      - Margin=48,0,32,64
  - target: StackPanel#TimePanel
    styles:
      - HorizontalAlignment=Left
      - Margin=0
      - Padding=0
  - target: StackPanel#TimePanel > TextBlock#Time
    styles:
      - FontSize=130
      - FontFamily=Segoe UI Light
      - FontWeight=Normal
      - CharacterSpacing=0
      - Foreground=#FFFFFF
      - HorizontalAlignment=Left
      - VerticalAlignment=Center
      - TextAlignment=Left
      - Margin=0
      - Padding=0
  - target: StackPanel#TimeAndDatePanel > TextBlock#Date
    styles:
      - FontSize=56
      - FontFamily=Segoe UI SemiLight
      - FontWeight=Normal
      - CharacterSpacing=-15
      - Foreground=#FFFFFF
      - HorizontalAlignment=Left
      - TextAlignment=Left
      - Margin=0,-10,0,30
      - Padding=0
      - TextWrapping=Wrap
  - target: Grid#NetworkAndBatteryIcon > Border
    styles:
      - Background:=<WindhawkBlur BlurAmount="35" TintColor="#70242424"/>
      - BorderBrush=#50242424
      - BorderThickness=0
      - CornerRadius=8
      - HorizontalAlignment=Right
      - Margin=11,0,11,11
      - Padding=10,10,10,10
  - target: Grid#MediaTransportControls
    styles:
      - Background:=<WindhawkBlur BlurAmount="35" TintColor="#90242424"/>
      - BorderBrush=#50242424
      - BorderThickness=0
      - CornerRadius=8
      - Width=380
      - Height=110
      - MinWidth=0
      - MinHeight=0
      - Padding=10,10,10,10
      - Margin=0,0,0,0
  - target: Grid#MediaControlsContainer
    styles:
      - HorizontalAlignment=Right
      - Margin=0,0,11,63
      - MinWidth=0
  - target: Grid#MediaTransportControls > StackPanel
    styles:
      - VerticalAlignment=Right
      - Margin=0
      - Padding=0
  - target: Grid#ThumbnailImageArea
    styles:
      - Width=90
      - Height=90
      - VerticalAlignment=Center
      - HorizontalAlignment=Left
      - Margin=0,0,12,0
      - RenderTransformOrigin=0.5,0.5
      - RenderTransform:=<ScaleTransform ScaleX="1.0" ScaleY="1.0" />
  - target: Grid#MediaTransportControls > StackPanel > TextBlock
    styles:
      - FontWeight=Semib
      - CharacterSpacing=0
      - TextAlignment=Left
      - Height=Auto
      - Padding=0,0,0,0
  - target: Grid#MediaTransportControls > StackPanel > TextBlock[1]
    styles:
      - FontSize=18
      - Foreground=#FFFFFF
      - TextWrapping=Wrap
      - MaxLines=2
      - TextTrimming=CharacterEllipsis
      - Margin=0
  - target: Grid#MediaTransportControls > StackPanel > TextBlock[2]
    styles:
      - FontSize=13
      - Foreground=#C5E3C5
      - Margin=0,0,0,0
      - TextWrapping=NoWrap
      - TextTrimming=CharacterEllipsis
  - target: Button#PlayPauseButton
    styles:
      - Width=36
      - Height=36
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#PreviousButton
    styles:
      - Width=36
      - Height=36
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#NextButton
    styles:
      - Width=36
      - Height=36
  - target: StackPanel#DefaultTitleStackPanel > TextBlock
    styles:
      - FontFamily=Segoe UI Light
      - FontSize=16
      - FontWeight=Normal
      - CharacterSpacing=0
      - Foreground=#FFFFFF
themeResourceVariables:
  - ''
webContentStyles:
  - target: ''
    styles:
      - ''
webContentCustomJs: ''
`
