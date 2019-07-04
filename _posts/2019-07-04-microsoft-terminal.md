---
layout: post
title:  "The New Windows Terminal"
categories: system, setup, windows, terminal, bash, wsl, linux
---

So, the Microsoft Store now finally has the Preview version of the much hyped Windows Terminal, and having used it for some time now, I have come to like this single-window multi-tabbed terminal. I have been using ConEmu for some time now, and although it also has the multi-tab feature, it kind of gets slow at times. The Windows Terminal feels really snappy and uses lower memory overall. The Terminal also seems to have a better UI, but I feels it lacks the feature of glass-slab like transparency. Windows Terminal has the acrylic transparency feature which blotches out the background for most part and this is a feature that I strongly feel should be incorporated in the final version. 


Another highlight for this Terminal Application is its display configurability using a JSON file called "profile.json". A shortcut (Ctrl+,) or the options drop down on the App can land you here, after which you can adjust your settings accordingly. I am sharing my json file here for your reference. 

```json
{
    "globals" : 
    {
        "alwaysShowTabs" : true,
        "defaultProfile" : "{09dc5eef-6840-4050-ae69-21e55e6a2e62}",
        "initialCols" : 120,
        "initialRows" : 30,
        "keybindings" : 
        [
            {
                "command" : "closeTab",
                "keys" : 
                [
                    "ctrl+w"
                ]
            },
            {
                "command" : "newTab",
                "keys" : 
                [
                    "ctrl+t"
                ]
            },
            {
                "command" : "newTabProfile0",
                "keys" : 
                [
                    "ctrl+shift+1"
                ]
            },
            {
                "command" : "newTabProfile1",
                "keys" : 
                [
                    "ctrl+shift+2"
                ]
            },
            {
                "command" : "newTabProfile2",
                "keys" : 
                [
                    "ctrl+shift+3"
                ]
            },
            {
                "command" : "newTabProfile3",
                "keys" : 
                [
                    "ctrl+shift+4"
                ]
            },
            {
                "command" : "newTabProfile4",
                "keys" : 
                [
                    "ctrl+shift+5"
                ]
            },
            {
                "command" : "newTabProfile5",
                "keys" : 
                [
                    "ctrl+shift+6"
                ]
            },
            {
                "command" : "newTabProfile6",
                "keys" : 
                [
                    "ctrl+shift+7"
                ]
            },
            {
                "command" : "newTabProfile7",
                "keys" : 
                [
                    "ctrl+shift+8"
                ]
            },
            {
                "command" : "newTabProfile8",
                "keys" : 
                [
                    "ctrl+shift+9"
                ]
            },
            {
                "command" : "nextTab",
                "keys" : 
                [
                    "ctrl+tab"
                ]
            },
            {
                "command" : "openSettings",
                "keys" : 
                [
                    "ctrl+,"
                ]
            },
            {
                "command" : "prevTab",
                "keys" : 
                [
                    "ctrl+shift+tab"
                ]
            },
            {
                "command" : "scrollDown",
                "keys" : 
                [
                    "ctrl+shift+down"
                ]
            },
            {
                "command" : "scrollDownPage",
                "keys" : 
                [
                    "ctrl+shift+pgdn"
                ]
            },
            {
                "command" : "scrollUp",
                "keys" : 
                [
                    "ctrl+shift+up"
                ]
            },
            {
                "command" : "scrollUpPage",
                "keys" : 
                [
                    "ctrl+shift+pgup"
                ]
            },
            {
                "command" : "switchToTab0",
                "keys" : 
                [
                    "alt+1"
                ]
            },
            {
                "command" : "switchToTab1",
                "keys" : 
                [
                    "alt+2"
                ]
            },
            {
                "command" : "switchToTab2",
                "keys" : 
                [
                    "alt+3"
                ]
            },
            {
                "command" : "switchToTab3",
                "keys" : 
                [
                    "alt+4"
                ]
            },
            {
                "command" : "switchToTab4",
                "keys" : 
                [
                    "alt+5"
                ]
            },
            {
                "command" : "switchToTab5",
                "keys" : 
                [
                    "alt+6"
                ]
            },
            {
                "command" : "switchToTab6",
                "keys" : 
                [
                    "alt+7"
                ]
            },
            {
                "command" : "switchToTab7",
                "keys" : 
                [
                    "alt+8"
                ]
            },
            {
                "command" : "switchToTab8",
                "keys" : 
                [
                    "alt+9"
                ]
            }
        ],
        "requestedTheme" : "system",
        "showTabsInTitlebar" : true,
        "showTerminalTitleInTitlebar" : true
    },
    "profiles" : 
    [
        {
            "acrylicOpacity" : 0.20000000298023224,
            "background" : "#2C001E",
            "backgroundOpacity" : 0.9,
            "closeOnExit" : true,
            "colorScheme" : "Campbell",
            "commandline" : "wsl.exe  -d Ubuntu-18.04",
            "cursorColor" : "#FFFFFF",
            "cursorShape" : "bar",
            "fontFace" : "Consolas",
            "fontSize" : 12,
            "guid" : "{09dc5eef-6840-4050-ae69-21e55e6a2e62}",
            "historySize" : 9001,
            "icon" : "ms-appdata:///roaming/ubuntu-32.png",
            "name" : "Ubuntu",
            "padding" : "0, 0, 0, 10",
            "snapOnInput" : true,
            "useAcrylic" : false
        },
        {
            "acrylicOpacity" : 0.20000000298023224,
            "background" : "#012456",
            "backgroundImage" : "ms-appdata:///roaming/esa.gif",
            "backgroundImageOpacity" : 0.25,
            "closeOnExit" : true,
            "colorScheme" : "Campbell",
            "commandline" : "powershell.exe",
            "cursorColor" : "#FFFFFF",
            "cursorShape" : "bar",
            "fontFace" : "Consolas",
            "fontSize" : 12,
            "guid" : "{565ed1db-1474-455e-9d62-cb9fc7eb3f59}",
            "historySize" : 9001,
            "icon" : "ms-appdata:///roaming/pwsh-32.png",
            "name" : "PowerShell",
            "padding" : "0, 0, 0, 0",
            "snapOnInput" : true,
            "startingDirectory" : "%USERPROFILE%",
            "useAcrylic" : false
        },
        {
            "acrylicOpacity" : 0.20000000298023224,
            "closeOnExit" : true,
            "colorScheme" : "Solarized Dark",
            "commandline" : "cmd.exe",
            "cursorColor" : "#FFFFFF",
            "cursorShape" : "bar",
            "fontFace" : "Consolas",
            "fontSize" : 12,
            "guid" : "{2c9fc8c8-d57d-4721-9319-47fe42fbb900}",
            "historySize" : 9001,
            "icon" : "ms-appdata:///roaming/cmd.ico",
            "name" : "CMD",
            "padding" : "0, 0, 0, 0",
            "snapOnInput" : true,
            "startingDirectory" : "%USERPROFILE%",
            "useAcrylic" : true
        }
    ],
    "schemes" : 
    [
        {
            "background" : "#0C0C0C",
            "black" : "#0C0C0C",
            "blue" : "#0037DA",
            "brightBlack" : "#767676",
            "brightBlue" : "#3B78FF",
            "brightCyan" : "#61D6D6",
            "brightGreen" : "#16C60C",
            "brightPurple" : "#B4009E",
            "brightRed" : "#E74856",
            "brightWhite" : "#F2F2F2",
            "brightYellow" : "#F9F1A5",
            "cyan" : "#3A96DD",
            "foreground" : "#F2F2F2",
            "green" : "#13A10E",
            "name" : "Campbell",
            "purple" : "#881798",
            "red" : "#C50F1F",
            "white" : "#CCCCCC",
            "yellow" : "#C19C00"
        },
        {
            "background" : "#073642",
            "black" : "#073642",
            "blue" : "#268BD2",
            "brightBlack" : "#002B36",
            "brightBlue" : "#839496",
            "brightCyan" : "#93A1A1",
            "brightGreen" : "#586E75",
            "brightPurple" : "#6C71C4",
            "brightRed" : "#CB4B16",
            "brightWhite" : "#FDF6E3",
            "brightYellow" : "#657B83",
            "cyan" : "#2AA198",
            "foreground" : "#FDF6E3",
            "green" : "#859900",
            "name" : "Solarized Dark",
            "purple" : "#D33682",
            "red" : "#D30102",
            "white" : "#EEE8D5",
            "yellow" : "#B58900"
        },
        {
            "background" : "#FDF6E3",
            "black" : "#073642",
            "blue" : "#268BD2",
            "brightBlack" : "#002B36",
            "brightBlue" : "#839496",
            "brightCyan" : "#93A1A1",
            "brightGreen" : "#586E75",
            "brightPurple" : "#6C71C4",
            "brightRed" : "#CB4B16",
            "brightWhite" : "#FDF6E3",
            "brightYellow" : "#657B83",
            "cyan" : "#2AA198",
            "foreground" : "#073642",
            "green" : "#859900",
            "name" : "Solarized Light",
            "purple" : "#D33682",
            "red" : "#D30102",
            "white" : "#EEE8D5",
            "yellow" : "#B58900"
        },
        {
            "background" : "#2C001E",
            "black" : "#EEEEEC",
            "blue" : "#268BD2",
            "brightBlack" : "#002B36",
            "brightBlue" : "#839496",
            "brightCyan" : "#93A1A1",
            "brightGreen" : "#586E75",
            "brightPurple" : "#6C71C4",
            "brightRed" : "#CB4B16",
            "brightWhite" : "#FDF6E3",
            "brightYellow" : "#657B83",
            "cyan" : "#2AA198",
            "foreground" : "#EEEEEC",
            "green" : "#729FCF",
            "name" : "Ubuntu",
            "purple" : "#D33682",
            "red" : "#16C60C",
            "white" : "#EEE8D5",
            "yellow" : "#B58900"
        },
        {
            "background" : "#2C001E",
            "black" : "#4E9A06",
            "blue" : "#3465A4",
            "brightBlack" : "#555753",
            "brightBlue" : "#729FCF",
            "brightCyan" : "#34E2E2",
            "brightGreen" : "#8AE234",
            "brightPurple" : "#AD7FA8",
            "brightRed" : "#EF2929",
            "brightWhite" : "#EEEEEE",
            "brightYellow" : "#FCE94F",
            "cyan" : "#06989A",
            "foreground" : "#EEEEEE",
            "green" : "#300A24",
            "name" : "UbuntuLegit",
            "purple" : "#75507B",
            "red" : "#CC0000",
            "white" : "#D3D7CF",
            "yellow" : "#C4A000"
        }
    ]
}
```


For some better reference, I am adding some screenshots of the App. For the Powershell window, I have added a gif for the background and the WSL has the classic Ubuntu look.

<img src="{{site.url}}/images/powershell.png" style="display: block; margin: auto;" />

<img src="{{site.url}}/images/ubuntu.png" style="display: block; margin: auto;" />


I hope they improve a bit on the transparency issue and the lag issues with closing the application, once all the windows are closed. 



