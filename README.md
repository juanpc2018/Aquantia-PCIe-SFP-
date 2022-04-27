# Aquantia-PCIe-SFP-
FW Upgrade procedure

There are different Brands of PCIe cards with Aqtion controller IC
ASUS XG-C100F SFP+
ASUS XG-C100C RJ45 CAT6A
Sonnet Tech Solo 10G SFP+
Trendnet 10G v1 o v2 "Untested"

Sonnet also has Dual SFP+ with Intel IC
compatiblw with older OSX,
Aquantia requires OSX High Sierra.

Asus & Sonnet have same Aquantia IC,
but only Sonnet does Not require OSX Drivers.

to make work the Asus .kext must be modified to include the Asus PID.

Aquantia was purchased by Marvell.
there is a Repo here in Github,
has dricers for FreeBSD, ESXi
https://github.com/Aquantia/AQtion

There are drivers also in the ASUS website,
and Sonnet Website.

Latest Drivers % FW from Marvell / AQC:
https://www.marvell.com/support/downloads.html

Linux driver installs and works well in Kubuntu 20.10 Groovy
but Groovy is Not LTS.
better install 20.04 LTS

Windows also work OK,
same Driver & same FW works for Both:
ASUS XG-C100F or Sonnet Solo 10G SFP+ PCIe
Trendnet "untested"

SFP+
https://www.asus.com/Networking-IoT-Servers/Wired-Networking/All-series/XG-C100F/
https://www.sonnettech.com/product/solo10g-sfp-pcie-card.html
https://www.sonnettech.com/product/presto10gbesfp.html
https://www.trendnet.com/products/10g-sfp-pcie-adapter/10-gigabit-pcie-sfp-network-adapter-TEG-10GECSFP-v2

RJ45 10G CAT6A
https://www.sonnettech.com/product/solo10g-pcie-card.html
https://www.sonnettech.com/product/presto10gbaset.html

Asus XG-C100* requires: 1500rpm fan or more, depending on Ambient °C.
Heatsink is Big, Pretty, but is too far from Marvell / Aquantia IC with a foam.

Will shutdown IF over heats.
an over heats very easy with 800rpm case fan.

Asus has a Dumb ass working in heatsink design.
this happens since Asus Rampage III Extreme X58 era "since 2010".
