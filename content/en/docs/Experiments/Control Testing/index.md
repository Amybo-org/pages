---
title: Control Testing
description: A simple control test evaluating results between Pioreactors by Gerrit Niezen
weight: 10
---

To ensure that the Pioreactors we're using are working as expected, we ran an experiment where we used the exact same experimental conditions with two Pioreactors, with the hope to produce the same results.

The original experiment is described on the [Pioreactor website](https://docs.pioreactor.com/experiments/control-testing).


{{% imgproc equipment Fit "600x500" %}}
A bunsen burner, small weight scale, three vials and a dropper. Two of the vials contain YPD broth and are covered with aluminium foil. The other vial contains stock solution.
{{% /imgproc %}}


## Kit List
1. 2 x [Pioreactor 20 ml](https://pioreactor.com/products/pioreactor-20ml?variant=46559156469816) - [see our thoughts on Pioreactors](https://AMYBO.org/docs/equipment/bioreactors/#pioreactorhttpspioreactorcom)
1. 2 x [Raspberry Pi Zero 2 W with header](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/)
1. 2 x [Raspberry Pi 15W USB-C Power Supply](https://www.raspberrypi.com/products/type-c-power-supply/)
1. 2 x [Micro SD cards](https://docs.pioreactor.com/user-guide/common-questions#what-microsd-cards-do-you-recommend)
1. 3 x 20mL vials
1. Another computer on the same network as the Raspberry Pi with a web browser
1. [Pressure cooker](https://www.prestige.co.uk/products/high-dome-iconic-aluminium-pressure-cooker) to ['autoclave'](../../equipment/autoclaves/)
1. [Aluminium foil](https://www.sainsburys.co.uk/gol-ui/product/sainsburys-kitchen-foil-10m-x-300mm) to cover the vessel ports
1. [Distilled water](https://www.sainsburys.co.uk/gol-ui/product/carplan-de-ionised-water-25ltr)
1. [Baker's yeast](https://www.sainsburys.co.uk/gol-ui/product/allinson-easy-bake-yeast-100g)
1. [Digital pocket scale](https://www.ebay.co.uk/itm/353643617581?hash=item5256cd5d2d:g:-uUAAOSw8SthJx1f)
1. [YPD broth](https://formedium.com/product/ypd-broth/)
1. Measuring cup
1. Dropper/pipette


## Protocol

### Preparing and sterilizing the media

1. [Prepare YPD broth media](https://www.tiktok.com/@pioreactor/video/7130702807656697093) for three 15mL vials.
1. Pour 300mL tap water into the pressure cooker, place the three vials on the metal trivet in the pressure cooker and turn to a high setting.
1. Once the water in the cooker starts to boil, steam will come out of the open valve. Put the heaviest weight (15lb) weight on top of the valve.
1. The steam will lift the weight and start to escape. As soon as the steam starts to escape, start timing the sterilization and turn down the heat so that the steam is only just escaping and not rushing out. Aim to maintain a gentle hissing.
1. After 20 minutes turn off the heat and leave to cool.
1. Wait until pressure is completely reduced then lift the weight off the valve allowing any remaining steam to escape. **Never open the pressure cooker until the steam
valve has been opened to release the pressure.**

{{% imgproc autoclaving Fit "600x500" %}}
Using a pressure cooker on a gas stove as an autoclave
{{% /imgproc %}}

### Running the experiment

1. Dilute a small amount of baker's yeast in 15mL of YPD broth media
1. Innoculate the three sterile vials with the same amount (just a drop) of culture from the stock solution.
1. Wipe the vials and place them in the Pioreactors.
1. Start a new experiment on your Pioreactor dashboard.
1. Select *Manage all Pioreactors*
1. Start *Stirring* activity
1. Start *Temperature automation* activity and set to 30°C
1. Start *OD reading activity*
1. Go back to the graphs and check that an Optical Density (OD) signal is being received.
1. Select *Manage all Pioreators* again and start *Growth rate*.

{{% imgproc pioreactors Fit "600x500" %}}
Two Pioreactors standing side by side, with the one on the right connected to a Raspberry Pi 400
{{% /imgproc %}}

## Results

The raw results from the experiment are [available as CSV files on GitHub](https://github.com/AMYBO-org/results/tree/main/Control%20Testing).

{{% imgproc results Fit "600x1500" %}}
A screenshot of the Pioreactor results
{{% /imgproc %}}

## Report

{{< card header="Watch Gerrit's report his results" >}}
{{< youtube gIxau_YtKr0 >}}
{{< /card >}}

<br>
