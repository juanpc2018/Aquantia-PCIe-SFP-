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
has drivers for FreeBSD, ESXi https://github.com/Aquantia/AQtion

There are drivers also in the ASUS website,
and Sonnet Website.

Latest Drivers % FW from Marvell / AQC: https://www.marvell.com/support/downloads.html

Linux driver installs and works Ok in Kubuntu 20.10 Groovy Gorilla
but GroovyGorilla is Not LTS.
better install 20.04 LTS

Windows8.1 also work OK,
same Driver & same FW works for Both:
ASUS XG-C100F PCIe & Sonnet Solo 10G SFP+ PCIe
Trendnet v1 or v2 PCIe "Unknown / Untested"

Asus has No drivers for OSX,
Marvell AQC100 has No drivers for OSX,
but Sonnet with same IC works since OSX HighSierra without drivers,
because a partnership between Apple & Sonnet to develop HW for Apple.
OSX detects Sonnet PID HID and loads the drivers.
but still needs tweaking, see Sonnet FAQ.

WARNING #1:
FW upgrade does Not Jump from very old to latest.
you need to download the Sonnet Firmware if you have a very old FW installed on Asus XG-C100F,
Upgrade with Sonnet FW then upgrade to latest .121 from Marvell
FW upgrade utility can also Downgrade, but i dont see the point.
FW Upgrade utility gives an error, but PCIe card works Ok after Reboot.
Requires real Windows10, Not Virtual.
AQC100 are SFP+
the other are for RJ45.
FW upgrade utility can detect without Upgrade.
type /? or /help
in cmd as Administrator.
install drivers Before doing the Upgrade, and reboot to see if card is Working ok before the FW Upgrade.

i have W8.1x64 & Linux, dont like W10, or w11
W10 can be installed without Keys, will work Ok for 10minutes, enough to Upgrade the FW.
W10 Requires a 120GB or Bigger SSD.
a laptop with W10 does Not work, you need a PCIe slot.

https://www.microsoft.com/en-us/software-download/windows10

WARNING #2.
Do Not install W10x64 on a MacPro5,1 directly, will damage the UEFI.
Windows10 will overwrite the Mac UEFI.
you also need a Real PC.
or install Windows10 with twocanoes Winclone.

REboot to test if the New FW was intealled,
if is detected by the tool in cmd.
if Ok, W10 is No longer needed.

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
