---
template: main.html
---

![Setup-Banner](https://raw.githubusercontent.com/ExpressLRS/ExpressLRS-hardware/master/img/quick-start.png)

## Flashing via Passthrough

Target: `HappyModel_PP_2400_RX_via_BetaflightPassthrough`

Device Category: `Happymodel 2.4 GHz`

Device: `HappyModel PP 2400 RX`

![via Passthrough](../../assets/images/Method_RX_Passthrough-stm.png)

The PP receivers do not have Wifi, and so, it can only be updated via Passthrough or STLink(see below).

Follow the same wiring as that of the EP receivers shown [here](rx-fcprep.md#happymodel-ep1-ep2-pp). The PP has a silkscreened "RT5G" on one of its side indicating the order of the pads, with R = Rx, T = Tx, 5 = 5v and G = Gnd,  respectively. Connect the Rx pad to a Tx pad on the FC, and the Tx pad to an RX pad on the FC, with 5v and Gnd to their usual connections.

The PP **doesn't** have a `Boot` pad either so there's no need to bridge any pads.

Once wired, power up your FC by connecting a LiPo or, if the receiver is getting powered via USB, connect your USB cable to a vacant port.

Using the ExpressLRS Configurator, with the correct Target selected and [Firmware Options] set, hit **Build & Flash**. Wait a bit for the process to finish and you should see a "Success" banner. 

![Build & Flash](../../assets/images/BuildFlash.png)

Power-cycle the FC and verify receiver connects to the Tx module (power up the Tx first, then the Receiver).

## Flashing via STLink

Target: `HappyModel_PP_2400_RX_via_STLINK`

Device Category: `Happymodel 2.4 GHz`

Device: `HappyModel PP 2400 RX`

![via STLink](../../assets/images/Method_RX_STLink-stm.png)

![PP STLink](../../assets/images/ppSTLink.png)

This will require connecting a ST Link to CLK, DIO, 5V and GND.

Then with the correct Target selected and [Firmware Options] set, click **Build & Flash** in the ExpressLRS Configurator. Wait for the process to finish and you should see the "Success" banner.

![Build & Flash](../../assets/images/BuildFlash.png)

[Connect](rx-fcprep.md#happymodel-ep1-ep2-pp) your receiver to your FC and you should be ready for the next steps.

[Firmware Options]: ../firmware-options.md