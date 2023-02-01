# gpio-6i6o
Control GPIO contacts using OSC and HTTP 

![IMG_9504 (1)](https://user-images.githubusercontent.com/4082369/216039710-d4e9fe6b-587a-4e89-9845-d255ac66a2d5.png)

![IMG_9501](https://user-images.githubusercontent.com/4082369/216042669-64576b54-bfaf-493e-8c04-f25c57fcc1af.png)

## Usage

Detailed usage is provided in the [Wiki section](https://github.com/bzzrs/gpio-6i6o/wiki) of this repo.

### Powering the device and provide ethernet access
- Wall-power and RJ45 UTP cable
- RJ45 UTP cable with PoE

## Front panel display and light

The front panel can be divided in 4 sections:

### Display
The display will provided you with a wealth of information to quickly understand how the device is configured and what features are available.

### 2 leds with Ethernet activity
The 2 leds provide a quick way to see incoming and outgoing OSC message as a result of GPI and/or GPO activity.

When the device receives an OSC message, the led `In` will light up briefly. When an OSC message is sent to a target, the `out` led will lkight up briefly.

### Ethernet to GPO
6 leds and 6 buttons provide a quick way to monitor activity (leds) and close contact manually (buttons). Factory setting set the receiving port to `12321` and the Ethernet to GPO section is active (6 orange light are on). Send the device an OSC message and 1) the Net Act led will come ip briefly (received OSC message) and 2) led will light up briefly indicating the contact has been close/opended. (so both ends of the protocol have a visual indication of success). Pushing the butto will close the outgoing contact - no visual indicating is given, as the activty is upstream on the target device.

The GPO contact are fully galvanically seperated from the device circuitery and eachother (GND and 3.3V, 5V and 9V). The GPO's are controlled by MosFETs (secure and fast).

### GPI to Ethernet
6 leds and 6 buttons provide a quick way to monitor GPI activity. After initial startup this section will not light up, as mo target host and port are provided. Use the web interface to set the target host and port and the leds will light up. Now puish a button and see that the led comes on (for as long as you keep the button pressed) and that the Net Act led flashes quickly (OSC message sent). The buttons are a quick way to send an OSC message during the development phase as well as during abnormal situations in the workflow (controlling computer not in the right mode/sequence).

## Back panel 

The back panel also has 4 sections:

### Power
A C13 cable fits in the C14 connector on the device. Input voltage ranges from 100V to 240V - 50 or 60Hz.
This cable is optional is you provide PoE.

### Ethernet
An Ethernet cable that is connected to a switch or router.
The device accepts IEEE 802.3 PoE (Power cable not needed when providing PoE)

Note: Both PoE and power cable can be attached to the machine at the same time.

### Ethernet to GPO

### GPI to Ethernet
