# Reticulum Development Roadmap
The development path for Reticulum is currently laid out in five distinct areas: *Comprehensibility*, *Universality*, *Functionality*, *Usability & Utility* and *Interfaceability*. Conceptualising the development of Reticulum into these areas serves to advance the implementation and work towards the Foundational Goals & Values of Reticulum.

## Comprehensibility
These efforts are aimed at improving the ease of which Reticulum is understood, and lowering the barrier to entry for people who wish to start building systems on Reticulum.

- Improving [the manual](https://markqvist.github.io/Reticulum/manual/) with tutorials specifically for beginners
- Updating the documentation to reflect recent changes and improvements
    - Update descriptions of protocol mechanics
        - Update announce description
        - Add in-depth explanation of the IFAC system
    - Software
        - Update Sideband screenshots
        - Update Sideband description
        - Update NomadNet screenshots
        - Update Sideband screenshots
    - Installation
        - Install docs for fedora, needs `python3-netifaces`
        - Add a *Reticulum On Raspberry Pi* section
        - Update *Reticulum On Android* section if necessary
        - Update Android install documentation.
    - Communications hardware section
        - Add information about RNode external displays.
        - Packet radio modems.
        - Possibly add other relevant types here as well.
    - Setup *Best Practices For...* / *Installation Examples* section.
        - Home or office (example)
        - Vehicles (example)
        - No-grid/solar/remote sites (example)

## Universality
These efforts seek to broaden the universality of the Reticulum software and hardware ecosystem by continously diversifying platform support, and by improving the overall availability and ease of deployment of the Reticulum stack.

- Improved roaming support on Android
- OpenWRT support
- Create a standalone RNS Daemon app for Android
- A lightweight and portable C implementation for microcontrollers, µRNS
- A portable, high-performance Reticulum implementation in C/C++, see [#21](https://github.com/markqvist/Reticulum/discussions/21)
- Performance and memory optimisations of the Python implementation
- Bindings for other programming languages

## Functionality
These efforts aim to expand and improve the core functionality and reliability of Reticulum.

- Improve storage persist call on local client connect/disconnect
- Faster path invalidation on physical topography changes
- Better path invalidation on roaming interfaces
- Network-wide path balancing
- Distributed Destination Naming System
- Globally routable multicast
- Destination proxying: Create a new random destination, and sign it with the original destination to create verifiable ephemeral destinations. This could actually be a very powerful feature for aggregating routes in the network, and it retains destination owners control over how they are routed
- [Metric-based path selection and multiple paths](https://github.com/markqvist/Reticulum/discussions/86)

## Usability & Utility
These effors seek to make Reticulum easier to use and operate, and to expand the utility of the stack on deployed systems.

- Add bluetooth pairing code output to rnodeconf
- Easy way to share interface configurations, see [#19](https://github.com/markqvist/Reticulum/discussions/19)
- Transit traffic display in rnstatus
- JSON output mode for rnstatus
- rnid utility
- rnsign utility
- rncrypt utility
- rnsconfig utility
- Expand rnx utility to true interactive remote shell

## Interfaceability
These efforts aim to expand the types of physical and virtual interfaces that Reticulum can natively use to transport data.

- Filesystem interface
- Plain ESP32 devices (ESP-Now, WiFi, Bluetooth, etc.)
- More LoRa transceivers
- AT-compatible modems
- Direct SDR Support
- Optical mediums
- IR Transceivers
- AWDL / OWL
- HF Modems
- GNU Radio
- CAN-bus
- Raw SPI
- Raw i²c
- MQTT
- XBee
- Tor

## Active Work Areas
For each release cycle of Reticulum, improvements and additions from the five areas are selected as active work areas, and can be expected to be included in the upcoming releases within that cycle. While not entirely set in stone for each release cycle, they serve as a pointer of what to expect in the near future.

- The current `0.4.x` release cycle aims at completing:
  - [x] Improve storage persist call on local client connect/disconnect
  - [x] Improved roaming support on Android
  - [ ] Updating the documentation to reflect recent changes and improvements
  - [ ] Add bluetooth pairing code output to rnodeconf
  - [ ] Improve storage persist call on every local client connect/disconnect
  - [ ] Transit traffic display in rnstatus
  - [ ] JSON output mode for rnstatus
  - [ ] Add `rnid` utility
  - [ ] Add `rnsign` utility
  - [ ] Add `rncrypt` utility
  - [ ] Create a standalone RNS Daemon app for Android
- Targets for related applications
  - [x] Add paper offline & paper message transport to LXMF
  - [x] Implement paper messaging in Nomad Network
  - [x] Implement paper messaging in Sideband
  - [x] Expand device support in Sideband to support older Android devices
