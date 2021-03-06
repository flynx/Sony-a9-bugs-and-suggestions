# Sony a9: Bugs and suggestions

These bugs and suggestions are for *Sony a9 firmware version 2.00 to
version 6.00*.


## Philosophy and motivation

- I shoot lots of fast moving subjects and fast changing situations
- I react to the situation — thinking in this workflow makes things slow
- I separate actions and make them as independent as possible
- I prefer the interface to be as simple as possible, i.e. to do one thing
I have to perform only one action, e.g. when waiting for the moment the
index finger only shoots, thumb only starts/stops AF, etc.
- The target is for the camera to be an extension of what I do not
requiring any mental attention during the shoot as all the attention
is drawn to the situation at hand and any interruptions break the flow
and concentration.


---

## Critical bugs

Most of the bugs in this sections are connected in one way or the other
to the *"Recall Custom hold #"* function.



### Focus peaking stops working after activating *"Recall Custom hold #"* with AF-ON set

#### To reproduce (setup):
  1. Set *Peaking Display* to *On*
  2. Set focus mode to *MF*
  3. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)


#### To reproduce (operation):
  1. Press *"AF-ON"* (*"Recall Custom hold #"*) — **Focus peaking disappears**

Focus peaking display disappears untill either:
  1. Camera power is turned off then on,
  2. focus mode is switched to AF-C / AF-S and back to MF,
  3. Menu is displayed for more than several seconds

Turning *Peaking Display* off then back on has no effect.


### Stateful functions (Example: *"AEL Toggle"*) dropped when activating *"Recall Custom hold #"*

#### To reproduce (setup):
  1. Set *"AEL Toggle"* to a custom button (*C2*)
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)


#### To reproduce (operation):
  1. Press *C2* (*"AEL Toggle"*) — to lock exposure
  2. Recompose
  3. Press *"AF-ON"* (*"Recall Custom hold #"*) — **Exposure unlocked and changed**

This seems to drop all settings that can be toggled including:
  - *"AEL Toggle"*
  - *"Spot AEL Toggle"*
  - *"AF/MF Ctrl Toggle"*
  - ...


#### Expected behavior:
Togglable settings are reset only by toggling them off or by switching
the camera off


#### Motivation and situations this affects:
This simply makes it pointless and impossible to use *"AEL Toggle"*
with any of the *"Recall Custom hold #"* functions.



### Activating *"Recall Custom hold #"* then half pressing the Shutter button will hold the "Recall Custom hold #" function even if the original button is released, until the Shutter button is fully released

#### To reproduce (setup):
  1. Set in *"Recall Custom hold #"*:
     1. *AF-ON* to On
     1. *Focus mode* to Continuous AF
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)
  3. Set *"AF w/ shutter"* to Off
  4. Set AF mode to *AF-C*


#### To reproduce (operation):
  1. Press and hold *AF-ON* — AF tracking starts
  2. Half press and hold shutter button
  3. Release *AF-ON* — **AF tracking does not stop** while shutter button is pressed
  4. Release shutter button — **AF tracking stops**


#### Expected behavior:
*"Recall Custom hold #"* effect should be activated and stopped ONLY by 
the assigned and pressed button.

Shutter button and *"Recall Custom hold #"* should be independent and
not affect each other.


#### Motivation and situations this affects:
This makes focusing and recomposing in fast moving situations without
fully releasing the shutter button impossible. Fully releasing the shutter
button increases the reaction time and makes it harder to capture the
exact moment.

This affects situations when the subject is just out of the current
focusing zone and it is faster and more practical to move the whole camera
to the subject, focusing and moving back, than moving the focusing zone
(requiring changing the grip and losing concentration).

A good flow would be:
  1. Set an approximate focusing zone and if possible roughly pre-focus in advance
  2. Roughly compose and get ready (half-pressing the shutter button)
  3. if focus is off, move the camera slightly and focus on the subject
  4. compose and wait for the moment
  5. repeat #3 and #4 as the situation changes

This is usually done in one fluid movement, progressively composing and
focusing closer and closer to the target, in a more and more accurate
manner, always ready to take the shot if the situation changes. This
is effective as capturing the perfect situation when it happens is more
critical than getting perfect focus or prefect framing. If time permits
this approach also helps achieve all (composition, focus, framing),
if not I get a good composition with some compromises.

This issue makes this approach very hard or even impossible as between
steps #3 and #4 the camera will not stop tracking focus, as the shutter
button still half-pressed in anticipation of the shot, and as a result
the camera will focus on the background/foreground when recomposing. To
work around this it is needed to fully release the shutter button between
steps #3 and #4 breaking the flow and concentration.

With this issue it is more practical to focus manually in such situations.



### Half pressing the Shutter button will prevent any "Recall Custom hold #" from activating

#### To reproduce (setup):
  1. Set in *"Recall Custom hold #"*:
     1. *AF-ON* to On
     1. *Focus mode* to Continuous AF
  2. Set *"Recall Custom hold #"* to a custom button (*AF-ON*)
  3. Set *"AF w/ shutter"* to Off
  4. Set AF mode to *AF-C*


#### To reproduce (operation):
  1. Half press and hold shutter button
  2. Press and hold *AF-ON* — **No effect** while the shutter button is pressed


#### Expected behavior:
Shutter button should have no effect on other button function, especially
when half pressed.

Shutter button and *"Recall Custom hold #"* should be independent and
not affect each other.


#### Motivation and situations this affects:
This makes it impossible to refocus while the shutter button is half pressed.

This is related to the previous issue.

Consider the same flow as above in a dynamic situation:
  1. Set an approximate focusing zone and if possible roughly pre-focus in advance
  2. Roughly compose and get ready (half-pressing the shutter button)
  3. if focus is off, move the camera slightly and focus on the subject
  4. compose and wait for the moment
  5. repeat #3 and #4 as the situation changes

This issue prevents starting focus tracking in step #3 without fully
releasing the shutter button as when the shutter is half pressed *"Recall
Custom hold #"* functions can not be activated.

This breaks the flow and concentration hindering reaction to the changing
situation.

With this issue it is also more practical to focus manually in such
situations.


### Screen briefly turns on when turning camera on in EVF mode (v3.00 only)

#### To reproduce (setup):
  1. Set *"FINDER/MONITOR"* to *Monitor (Manual)* via Menu
  2. Set custom button to *"Finder/Monitor sel."* (*Down Button*)
  3. Press *Down button* to switch to EVF mode.

#### To reproduce (operation):
  1. Turn camera off (for a few seconds)
  2. Turn camera on -- **screen turns on momentarily**

#### Expected behavior:
In EVF mode the screen is always off.

*NOTE: when *"FINDER/MONITOR"* is set to *Viewfinder (Manual)* via Menu
the screen does not blink on startup regardless of how it was switched 
afterwards.*



---

## Critical suggestions

This section describes missing features that either hinder camera use
or make it near impossible in common situations.


### Save all settings to card / Load all settings from card

*Enable saving and loading full camera state to/from memory card.*

When using multiple cameras it is critical to be able to predictably and
repeatably save/load settings to each camera. Such cases include when
using backup cameras, rented cameras or agency gear, having this feature
would enable the photographer to load his setup into the camera in one
simple step and then for the agency or renting house to return the camera
to its specific defaults.

Currently saving/loading a subset of settings is possible but this still
requires to additionally setup features that are not staved, like IPTC
data, control/button setup and other settings.


### Memory card overflow mode (IMPLEMENTED in v5)

*Enable writing to next card automatically when current card is full.*

A common use case is to use two cards in two slots and when one fills
up to write data the second. Currently when one card fills up it is
necessary to manually switch to the other card.


### Add *Face detect* option to *"Recall Custom hold #"* (IMPLEMENTED in v5)

In some situations face detect prevents from focusing on an area close
to a face (Example: tow faces partially covering each other and focus
must be on the farther face), adding this feature would make dealing
with such situations very simple by activating a *"Recall Custom hold #"*
set to a button (*AF-ON* with *Face detect* disabled). Currently dealing
with this requires going into the menu and disabling face detect manually
and enabling it after the shot is made.


### *"Auto-shutter"* to change from e-shutter to mechanical when setting shutter speed longer than 1/8sec

Currently to set a shutter speed longer than 1/8 sec requires to change
to M or S mode, then changing the shutter to mechanical and then setting
the correct speed. A way around this is to set M or S to one of the
1/2/3 custom modes and change shutter speed accordingly.

Enabling switching shutter mode with the selected shutter speed would
make this seamless, by simply changing the shutter speed manually (or
via P/A modes).

To avoid confusion this can also be done by adding an option like
*"Extended shutter range in auto-shutter"* to enable or disable this
feature.


### Option to manually change H, M and L speeds for each shutter mode
Currently H, M and L cont. drive modes are set to different speeds in
different shutter modes, e.g. L is set to 5 fps in e-shutter and 2.5 fps
in mechanical shutter, effectively one setting that has two different
behaviors, this makes changing shutter type require additionally resetting
the drive mode to M and then back, if the situation requires a specific
frame rate.

Situations where it may be required to change the shutter type quickly
may include:
- Screens in frame (some sports events, etc.)
- Specific lighting situations (oscillating lights, like some PWM LEDs 
and Sodium vapor lamps)
- Using flash

Adding an option to change the speeds (within obvious limits) for each shutter
type would enable setting L and M to same values for such situations. This
would also simplify setting specific fps values more appropriate for
specific events independent of shutter type.


### Option to overwrite drive modes and focus modes via custom settings (1/2/3)
It is not possible to overwrite the left dial state in custom modes, this
makes it impossible to setup the camera for specific tasks that require
specific frame rates and focusing modes in a way that would enable the
user to switch modes using just one control (Mode dial). Currently one
needs to both change the Mode dial to a custom mode and also change the
drive mode and focus mode separately.

This can either be done either by adding an option to save/load the dial
states per custom mode or as is done for *"Recall Custom hold #"*.


### AF tracking better hold point (IMPLEMENTED in v5)
Currently AF tracking is very erratic unless a face or a very distinct
subject is tracked even if the focus is locked on and camera is static.

It is hard to elaborate here without speculating but it seems that
unless the AF system can isolate a specific object it does not account
for camera movement and scene depth at all. This does not appear to be 
the case on older Alpha models.



---

## Suggestions

This section describes non-critical features that would make the camera
more convenient in everyday use.


### Menu and playback buttons turn screen on if eye sensor not activated until shutter button half press (return to shooting)
It is a common use case to quickly check an image or to set something in
the menu while not shooting. Currently this would require to switch the
camera from EVF to Screen and then back manually (set to a custom button).

Adding the option in EVF mode to turn on the screen if the Menu or Play
buttons are pressed and the Eye sensor / EVF is not active and switch
back to EVF mode as soon as the shutter button is half pressed would
make the above used case very convenient.

*NOTE: I'm not using the eye sensor to switch between the EVF and the
Screen because it is not fast enough for what I do, the 1/3 to 1/2
second EVF blackout is large enough for me to miss the first shot in a
fast changing situation.*


### E-shutter sound volume
There are situations where the current e-shutter sound is either too loud
(concert hall during a piano concert for example) and situations when
it is too quiet (a crowd or a loud event).

It would be very useful to add an option to change the volume of the
e-shutter sound.

*NOTE: for future cameras, it would be very good to add a tactile feedback
for shutter, for example silently vibrate the shutter button the moment
the shutter is opened and the moment it is closed (for long exposures),
this would eliminate the need for e-shutter sound and make the operation
very intuitive. This can be accomplished via a piezo element built
into the shutter button itself, which would also isolate any vibrations
transferred to the camera body.*


### Option to change the mode (P/A/S/M) from within one of the custom modes.
Currently this would require to fully reset the camera and overwrite
the current custom mode. It would be more convenient to be able to to
this via the *"Shoot mode"* option in the *"Function Menu St."*.


### Touchpad mode (from a7III) (IMPREMENTED in v5)
Add the touchscreen touchpad mode as implemented in *a7III*.


---

## Contacts:

  **Alex A. Naanou**  
  alex.nanou@gmail.com  
  http://flic.kr/f_lynx/  
  https://www.facebook.com/alex.naanou  
  https://docs.google.com/document/d/1ejk_vb9hYwQZ6DR1PzW0T7TLMBD_OQ4oHRrc_NeUPdA/edit?usp=sharing  

<!-- vim:set sw=4 ts=4 spell : -->
