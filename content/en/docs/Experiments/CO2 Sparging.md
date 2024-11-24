---
title: CO2 Sparging
description: A simple CO2 sparging protocol by Gerrit Niezen
weight: 10
---

Describes how to get started with CO2 sparging on the Pioreactor.

## Kit List
1. [Pioreactor 20 mL](https://pioreactor.com/products/pioreactor-20ml?variant=46559156469816) (or via [LabCrafter](https://labcrafter.co.uk/products/pioreactor) if you're in the UK/EU)
1. [Raspberry Pi Zero 2 W with header](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/)
1. [Raspberry Pi Micro USB Power Supply](https://www.raspberrypi.com/products/micro-usb-power-supply/) (or via [LabCrafter][(https://labcrafter.co.uk/products/raspberry-pi-micro-usb-power-supply) if you're in the UK/EU)
1. [Micro SD card](https://docs.pioreactor.com/user-guide/common-questions#what-microsd-cards-do-you-recommend)
1. Another computer on the same network as the Raspberry Pi with a web browser

### CO2 sparging
1. Sodastream cylinder (classic blue, not quick connect pink)
1. [Sodastream-to-regulator adapter](https://www.aliexpress.com/item/4001089851288.html) (TR21-4 thread size in most of the world, CGA 320 in North America)
1. CO2 regulator with solenoid, e.g. [FZONE](https://fzaqua.com/collections/co2-system/products/fzone-dual-big-gauge-co2-regulator-1)
1. [Barrel power cord with 2.1mm DC plug](https://uk.farnell.com/pro-elec/pelb2059/lead-2-1mm-dc-plug-to-bare-end/dp/4160342)
1. Connector to connect barrel power cord to PWM output, e.g. TE Connectivity AMP connector ([housing](https://www.digikey.co.uk/en/products/detail/te-connectivity-amp-connectors/487526-1/469847) and [socket contacts](https://www.digikey.co.uk/en/products/detail/te-connectivity-amp-connectors/1-104479-0/1125892)), or solder Dupont female square head wires to barrel power cord
1. ~20cm 4mm PU tubing
1. Check valve
1. 3/16" barb female Luer lock connector
1. 2 x 1/16" barb male Luer lock connector
1. ~20cm 1/16" silicone tubing
1. [Pioreactor vial cap for electrolysis and CO2 sparging](https://www.printables.com/model/974845-pioreactor-vial-cap-with-hole-for-6mm-electrode)

### Tools required
1. Crimping pliers, if you're going to use the TE Connectivity AMP connectors with the barrel power cord, or a soldering iron if you're going to solder Dupont cables to the barrel power cord
1. Wrench for attaching adapter to Sodastream cylinder and regulator

### Optional
1. [Dovetail platform for Pioreactor](https://www.printables.com/model/298240-pioreactor-platform-with-dovetails-for-a-zero-mode)
1. [Dovetail platform for Sodastream cylinder holder](https://www.printables.com/model/855700-sodastream-holder-for-pioreactor)

TODO

## Setup

### Hardware
1. Connect the CO2 regulator to the Sodastream cylinder using the adapter.
1. TODO

### Software
1. [Install](https://docs.pioreactor.com/user-guide/using-community-plugins#installing-plugins) the `pioreactor-relay-plugin` plugin
1. Create a new [experiment profile](https://docs.pioreactor.com/user-guide/experiment-profiles) and copy and paste the following into the profile:

```yaml
experiment_profile_name: CO2 sparging every hour

metadata:
  author: Gerrit Niezen
  description: Turns on the relay for 10 seconds every hour

common:
  jobs:
    relay:
      actions:
        - type: repeat
          hours_elapsed: 1.0
          repeat_every_hours: 1.0
          actions:
            - type: log
              hours_elapsed: 0.0  # relative to the repeat loop, 1h
              options:
                message: "Sparging CO2 for 10 seconds"
                level: info
            - type: start
              hours_elapsed: 0.0
              options:
                start_on: True
            - type: stop
              hours_elapsed: 0.00278
```

## Protocol

### Running the experiment

1. TODO

## Results

TODO

