# gpio-6i6o
Control GPIO contacts using OSC and HTTP.

Pricing and ordering via [bzzrs.tv](https://www.bzzrs.tv/product-page/bbzrbx-6i6o)

![IMG_9504 (1)](https://user-images.githubusercontent.com/4082369/216039710-d4e9fe6b-587a-4e89-9845-d255ac66a2d5.png)

![IMG_9501](https://user-images.githubusercontent.com/4082369/216042669-64576b54-bfaf-493e-8c04-f25c57fcc1af.png)

## Usage

Detailed usage is provided in the [Wiki section](https://github.com/bzzrs/gpio-6i6o/wiki) of this repo.

### Powering the device and provide ethernet access
- Wall-power and RJ45 UTP cable
- RJ45 UTP cable with PoE

## Front panel display and light

The front panel can be divided in 4 sections:

![Screenshot 2023-02-01 at 17 40 50](https://user-images.githubusercontent.com/4082369/216106594-a4b49f83-6bb7-4796-8993-b4a4a0fa1b8b.png)

### Display
The display will provided you with a wealth of information to quickly understand how the device is configured and what features are available.

![IMG_6E413CCD616D-1](https://user-images.githubusercontent.com/4082369/216108149-1dbafc11-4851-4e7d-a21b-c00084810167.jpeg)


### 2 leds with Ethernet activity
The 2 leds provide a quick way to see incoming and outgoing OSC message as a result of GPI and/or GPO activity.

![IMG_691FF929280B-1](https://user-images.githubusercontent.com/4082369/216108427-b779bebd-57a7-4292-a4c8-2b2641c827c2.jpeg)

When the device receives an OSC message, the led `In` will light up briefly. When an OSC message is sent to a target, the `out` led will lkight up briefly.

### Ethernet to GPO
6 leds and 6 buttons provide a quick way to monitor activity (leds) and close contact manually (buttons). Factory setting set the receiving port to `12321` and the Ethernet to GPO section is active (6 orange light are on). Send the device an OSC message and 1) the Net Act led will come ip briefly (received OSC message) and 2) led will light up briefly indicating the contact has been close/opended. (so both ends of the protocol have a visual indication of success). Pushing the butto will close the outgoing contact - no visual indicating is given, as the activty is upstream on the target device.

![IMG_9516](https://user-images.githubusercontent.com/4082369/216108985-221e52b0-58c7-4cb2-a214-756665b23f15.JPG)

The GPO contact are fully galvanically seperated from the device circuitery and eachother (GND and 3.3V, 5V and 9V). The GPO's are controlled by MosFETs (secure and fast).

### GPI to Ethernet
6 leds and 6 buttons provide a quick way to monitor GPI activity. After initial startup this section will not light up, as mo target host and port are provided. Use the web interface to set the target host and port and the leds will light up. Now puish a button and see that the led comes on (for as long as you keep the button pressed) and that the Net Act led flashes quickly (OSC message sent). The buttons are a quick way to send an OSC message during the development phase as well as during abnormal situations in the workflow (controlling computer not in the right mode/sequence).

![IMG_9517](https://user-images.githubusercontent.com/4082369/216109362-29bd4616-1ec3-4f1c-824f-809ac6792cf8.JPG)

## Back panel 

The back panel also has 4 sections:

![Screenshot 2023-02-01 at 17 40 20](https://user-images.githubusercontent.com/4082369/216106634-14be14a9-797d-4ff0-a67b-2ac117dc83bc.png)

### Power
A C13 cable fits in the C14 connector on the device. Input voltage ranges from 100V to 240V - 50 or 60Hz.
This cable is optional is you provide PoE.

![IMG_9518](https://user-images.githubusercontent.com/4082369/216110458-87012295-40a5-424b-94fd-496d2b91c68c.JPG)


### Ethernet
An Ethernet cable that is connected to a switch or router.
The device accepts IEEE 802.3 PoE (Power cable not needed when providing PoE)

![IMG_9518](https://user-images.githubusercontent.com/4082369/216110586-b283dcdc-c64b-42cd-9cf8-a4ae32816ca4.JPG)

Note: Both PoE and power cable can be attached to the machine at the same time.

Note: for studio environments, a XLR RJ45 connector (eg Neutrik) is prefered over standards UTP cable.

### Ethernet to GPO

6 3-pin male XLR are provided on the device to connect to. Pin 2 and 3 are connected (industry best practice).

![IMG_9519 2](https://user-images.githubusercontent.com/4082369/216111179-44d3d664-d3d2-4bf1-a114-0fad21acda75.JPG)

### GPI to Ethernet

6 3-pin female XLR are provided on the device to connect to. Pin 2 and 3 are connected (industry best practice).

![IMG_9520](https://user-images.githubusercontent.com/4082369/216111422-ae402dcf-7132-47ce-ac48-5df5235d9066.JPG)

