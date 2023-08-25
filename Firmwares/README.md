# Release notes

(Learn [here](https://github.com/bzzrs/gpio-6i6o/wiki/Upgrade-Firmware) how to upgrade the firmware)

## 6.2.0 - 25 aug 2023
- Add support for OSC Type Tag Strings.
Example: /press/bank/{bank}/{index} ,ifsTTusFs 123 3.14 "Hello world!" -8 yes test
   outputs: /press/bank/{bank}/{index} Tags: ,ifsTTusFs Arguments: [123, 3.14, Hello world!, true, true, -8 yes, false, test]

## 6.1.0 - 3 aug 2023
- Custom outgoing messages 

## 6.0.1 - 4 feb 2023
- Lights out when starting firmware upgrade.

## 6.0.0 - 2 feb 2023
- Outgoing OSC are no longer bundles, but simple OSC ,essages. This increases the compatibility with other systems that not always have suport for OSC bundles. This breaks backward compatibility and forces a major version increase.

## 5.2.0 - 1 feb 2023
- Added body to http /press/bank to permanently set the state of a contact

## 5.1.0 - 25 Jan 2023
- Added links to the landing page when requesting json response
- Added Conformance path /conformance

## 5.0.0 - 23 Jan 2023
- Major rewrite of the http handler.
- Added /ident path (flashes the light for 1 second, to identify a device amongst many)
- New UI on the front screen
- Fixed Ethernet bug causing occasional delays of 200ms

## 4.7.7 - Dec 2022
- Bug fix for http /press/bank
- Added display
