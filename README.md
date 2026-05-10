# AudioDeck

## What is an AudioDeck? 
A desktop audio controller for Windows computers - allowing users to modify various sound and microphone settings on the fly without havng to stop what they are doing on their PC. 

## Directory Guide
```text
/ *** The directory/ organization setup will likely change often and I will try to keep this guide updated as such
├── docs/                     
│   ├── guides/               # Setup, usage, building, troubleshooting guides 
│   ├── references/           # Datasheets, pinouts, protocols, layouts, wiring schematics (image) 
│   └── development/          # Changelog, todo, design notes
├── hardware/                 # Schematics, PCB files, wiring
│   ├── enclosure/            # All CAD files related to enclosure (case) parts
│   └── electronics/          # Wiring Schematics
|       └── PCB/              # PCB gerber files
│
├── software/            
│   ├── firmware/             # RP2040 firmware
│   └── pc-app/               # Desktop host application
│
└── README.md
```

## Plans for the AudioDeck
The AudioDeck will initially be made as a handwired version, with a PCB version eventually being released.
### Planned Features
- Control system audio volume using a slider
- Mute system audio using a key
- Mute/ unmute system microphone using a key
- Assign up to 5 customs macro keys for any purpose
- Next, Previus, Play/ Pause function keys that will control your active media session (youtube, spotify, VLC etc)
- Using the built in menu: 
  - View and modify per app audio volume of all active audio sessions (spotify, discord, chrome etc)
  - Select and update both input and output audio devices
  - Pin your favorite audio apps for quick access
  - Modify AudioDeck settings like screen brightness, encoder sensitivity and more
- Idle screen when not actively using the menu which may display things like the current time and date, and possibly even PC component status (GPU temp, CPU temp and load etc)
- A PC home app that will allow the board to communicate with your PC to allow viewing and mofications of audio sessions and devices
- Using the PC home app, you will have access to further AudioDeck preferences/ settings like:
  - Enabling/ Disabling audio apps you want to be able to see and modify on the AudioDeck
  - Setting up your custom macro keys
  - Potentionally being able to change AudioDeck screen layout/ colors/ design
  - Potentially being able to upload GIFs to be used in the idle menu
  - MORE IDEAS COMING SOON!!!
