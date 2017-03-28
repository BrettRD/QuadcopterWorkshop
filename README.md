# QuadcopterWorkshop
An intro to quadcopters workshop developed with Protospace


This repo contains a frame designed for laser-cutting from 4mm ply.

## Assembly
This frame only has four bolts to hold it together, and various parts are held in place by the frame geometry.
Once assembled, the frame is reasonably sturdy, but you may need an additional pair of arms to assemble it.

### Prep the parts
Some of the components need soldering before they can be used
* The motors need 3.5mm bullet connectors soldered to their fly-leads. Apply 10mm of 4.5mm heat-shrink.
* The flight controller needs headers soldered in place, and case screwed together.
* The ESCs and battery connector need to be soldered to the PDB - ESCs come off the PDB diagonals, positive leads front and rear, negative leads out the sides. One negative lead will share a place with the battery connector.
* The Props are designed to suit any motor shaft diameter up to 8mm and come with 8mm retainers, but require drilling out beyond 6mm.  Use a dull drill bit in a cordless drill to allow the bit to self-centre. (using a drill press requires extremely careful alignment)

### Order of assembly
I encourage you to skip ahead where possible, change things, refer to the example copy for details, and do your own thing.
This assembly order only applies for the frame design as supplied, and serves as notes for things that get hard when you do them the other way around.\
* Loop the battery strap through the base plate before fastening the PDB
* Fasten the PDB (with ESCs) to the the base plate with two layers of foam tape either side of the battery strap.
  Bolt holes are marked, but using foam tape leaves less hard points for the battery to snag on in a rough landing.
* Place the ESCs inside the arms. (Two outputs toward the straighter edge of the arm)
* Bolt the frame together with 4x M4 bolts (four to six hands recommended).
* Bolt the motors to the arms, paying attention to the direction of rotation (left and right hand thread on the prop adapter), cables draping over the straighter edge of the arms
* Fasten the flight controller using soft foam tape.
* Fasten the RC receiver to the base plate using foam tape.
* Plug the Naze32 RC lead into the receiver. Only pins 1-6 are important on this build.
* Plug the ESCs and receiver cable into the Naze32.
* Plug the flight controller into your laptop and configure it.
* Plug the motors into the ESCs. (if a motor spins the wrong way, swap two of its cables)
* Get someone to sanity-check your work before connecting the battery.

## Configuration
The flight controller and radio gear requires some basic set up.
### Receiver
Set the transmitter trim tabs to their mid points, and the throttle trim to minimum. (mid throttle trim is too high and prevents arming the copter.)
### Radio Binding
Modern radios permit multiple devices on the same frequency.  Plug the bind loop into the receiver and apply power, hold the bind button on the transmitter as you turn it on. The two devices should associate with each other. Power down everything and remove the bind loop. (make sure only one person tries this process at a time.)
### Axis inversions
The transmitter has four switches that allow you to invert any of its four axes. This build needs all but the Ailerons reversed.
### Flight Controller
The flight controller here is the NAZE32 Acro.  This controller runs the [Cleanflight](http://cleanflight.com/) software, which has its roots in the MultiWii code base. It is very popular as a reliable, no-nonsense racing controller.
You change the settings with the [Cleanflight Configurator](https://chrome.google.com/webstore/detail/cleanflight-configurator/enacoimjcgeinfnnnpajinjgmkahmfgb) Chromium App.
#### Flight modes
An auxiliary channel can be used to change flight behaviours. We lack such an auxiliary channel, so set all modes the same.  There are a few options to choose from, so I'll go over the important ones here:
* Rate gives you control over how quickly the copter rotates on its axes.  This is great for racing because it gives you a lot of control over the flight dynamics.  This mode requires the most attention
* Angle gives you control of the angle of the body. It won't let you flip over, but still offers good control.
* Horizon is a friendly mixed mode that will keep your copter level, but still allows you to roll all the way over when you really mean it.
* Baro takes control of the throttle, using the barometer as an altitude reference, and you tell it how fast to climb or descend.  This can lead to problems when you want to come down in a hurry, or the copter bounces endlessly on landing.

### Arming test
Move the throttle stick into the arming position (minimum throttle, full right yaw), and watch the read LED in the Naze32. if it goes from blinking to solid, you're ready to fly.
Move the throttle stick into the disarm position (minimum throttle, full left yaw), and the red LED shoud stark blinking again.

## Taking it further
These parts were chosen as a solid starting point for a hobby in RC aircraft.\
The flight controller is designed for racing copters, while the motors and ESCs are capable of lifting sensor packs and cameras.\
The transmitter was chosen to be appropriate as a "buddy box" or trainer handset alongside a more capable transmitter.\
To get into racing, you'll want to recude the total size, motor mass, and prop diameter.\
To get into autonomous platforms with advanced sensor packs, you'll want to swap the flight controller for something more advanced like the Pixhawk or Pixracer running the Ardupilot firmware.

## Glossary
* ESC: electrically switched commutator / electronic speed controller
* PDB: power distribution board



