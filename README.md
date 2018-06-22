# Sony a9: Bugs and suggestions

These bugs and suggestions are for *a9 firmware version 2.00*



## Bugs

Most of the bugs in this sections are connected in one way or the other to the *"Recall Custom hold #"* function.


### Stateful functions (Example: *"AEL Toggle"*) dropped when activating *"Recall Custom hold #"*

#### To reproduce (setup):
  1. Set *"AEL Toggle"* to a custom button (*C2*)
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)


#### To reproduce (operation):
  1. Press *C2* (*"AEL Toggle"*) -- to lock exposure
  2. Recompose
  3. Press *"AF-ON"* (*"Recall Custom hold #"*) -- **Exposure unlocked and changed**

This seems to drop all settings that can be toggled including:
  - *"AEL Toggle"*
  - *"Spot AEL Toggle"*
  - "AF/MF Ctrl Toggle"


#### Expected behavior:
Togglable settings are reset only by toggling them off or by switching the camera off



### Activating *"Recall Custom hold #"* then half pressing the Shutter button will hold the "Recall Custom hold #" function even if the original button is released, until the Shutter button is fully released.

XXX make the title shorted/clearer...

#### To reproduce (setup):
  1. Set in *"Recall Custom hold #"*:
     1. *AF-ON* to On
     1. *Focus mode* to Continuous AF
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)
  3. Set *"AF w/ shutter"* to Off
  4. Set AF mode to *AF-C*


#### To reproduce (operation):
  1. Press and hold *AF-ON* -- AF tracking starts
  2. Half press and hold shutter button
  3. Release *AF-ON* -- **AF tracking does not stop** while shutter button is pressed
  4. Release shutter button -- **AF tracking stops**


#### Expected behavior:
*"Recall Custom hold #"* effect should be activated and stopped ONLY by 
the assigned and pressed button.

Shutter button and *"Recall Custom hold #"* should be independent and not affect each other.



### Half pressing the Shutter button will prevent any "Recall Custom hold #" from activating.

#### To reproduce (setup):
  1. Set in *"Recall Custom hold #"*:
     1. *AF-ON* to On
     1. *Focus mode* to Continuous AF
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)
  3. Set *"AF w/ shutter"* to Off
  4. Set AF mode to *AF-C*


#### To reproduce (operation):
  1. Half press and hold shutter button
  2. Press and hold *AF-ON* -- **No effect** while the shutter button is pressed


#### Expected behavior:
Shutter button should have no effect on other button function, especially when half pressed.

Shutter button and *"Recall Custom hold #"* should be independent and not affect each other.



## Critical suggestions

This section describes missing features that either hinder camera use or make it near impossible in common situations.


### Save all settings to card / Load all settings from card

*Enable saving and loading full camera state to/from memory card.*

When using multiple cameras it is critical to be able to predictably and repeatably save/load settings to each camera. Such cases include when using backup cameras, rented cameras or agency gear, having this feature would enable the photographer to load his setup into the camera and then for the agency or renting house to return the camera to it's defaults.

Currently saving/loading a subset of settings is possible but this still requires to additionally setup features that are not stored, like IPCT data, control setup and other settings.


### Memory card overflow mode

*Enable writing to next card automatically when current card is full.*

A common use case is to use two cards in two slots and when one fills up to write data the second. Currently when one card fills up it is necessary to manually switch to the other card.


### Add face detect option to *"Recall Custom hold #"*

In some situations face detect prevents from focusing on an area close to a face, adding this feature would make dealing with such situations very simple by activating a *"Recall Custom hold #"* set to a button. Currently dealing with this requires going into the menu and disabling face detect manually and enabling it after the shot is made.


### *"Auto-shutter"* to change from e-shutter to mechanical when setting shutter speed longer than 1/8sec manually

Currently to set a shutter speed longer than 1/8 sec requires to change to M or S mode, then changing the shutter to mechanical and then setting the correct speed. A way around this is to set M or S to one of the 1/2/3 custom modes and change shutter speed accordingly.

Enabling switching shutter mode with the selected shutter speed would make this seamless, by simply chaning the shutter speed.

To avoid confusion this can also be done by adding an option like *"Extended shutter range in auto-shutter"* to enable or disable this feature.


### Option to manually change H, M and L speeds for each shutter mode

Currently H, M and L cont. drive modes are set to different speeds in different shutter modes, e.g. L is sert to 5 fps in e-shutter and 2.5 fps in mechanical shutter, this makes changing shutter type require additionally resetting the drive mode to M and then back.

Situations where it may be required to change the shutter type quickly may include:
- screens in frame (some sports events, etc.)
- specific lighting situations (oscillating lights, like LEDs and Sodium vapor lamps)

Adding an option to change the speeds (within limits) for each shutter mode would enable setting L and M to same values for such situations. This would also simplify setting specific fps values more appropriate for specific events independent of shutter type.


### Option to overwrite drive modes and focus modes via custom settings (1,2,3)



### AF tracking better hold point XXX



## Suggestions

This section describes non-critical features that would make the camera more convenient in every day use.

### e-shutter sound volume

### menu and playback buttons turn screen on if eye sensor not activated until shutter button half press (return to shooting)

### Touchpad mode (from a7III)



