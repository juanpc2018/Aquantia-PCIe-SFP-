# Aquantia PCIe SFP+ 10G </br>
### FW Upgrade procedure </br>

There are different Brands of PCIe cards with Aqtion controller IC

SFP+ 10G </br>
[ASUS XG-C100F SFP+](https://www.asus.com/Networking-IoT-Servers/Wired-Networking/All-series/XG-C100F/) </br>
[Sonnet Solo 10G SFP+](https://www.sonnettech.com/product/solo10g-sfp-pcie-card.html) </br>
[Trendnet 10G v1 o v2 "Untested"](https://www.trendnet.com/products/10g-sfp-pcie-adapter/10-gigabit-pcie-sfp-network-adapter-TEG-10GECSFP-v2) </br>

RJ45 10GbE Cat6A: </br>
[ASUS XG-C100C](https://www.asus.com/networking-iot-servers/wired-networking/all-series/xg-c100c/) </br>
[Sonnet Solo 10G](https://www.sonnettech.com/product/solo10g-pcie-card.html) </br>

Intel IC´s Non Aquantia: </br>
[Sonnet Presto SFP+](https://www.sonnettech.com/product/presto10gbesfp.html) </br>
[Sonnet Twin10G](https://www.sonnettech.com/product/presto10gbaset.html) </br>

Sonnet also has Dual SFP+ with Intel IC, compatible with older OSX. </br>

Marvell / Aquantia requires OSX High Sierra. </br>

Asus & Sonnet have same Aquantia IC, </br>
but only Sonnet does Not require OSX Drivers. </br>

to make work the Asus .kext must be modified to include the Asus PID. </br>

Aquantia was purchased by Marvell. </br>
there is a Repo here in Github, </br>
has drivers for FreeBSD, ESXi https://github.com/Aquantia/AQtion </br>

There are drivers in the ASUS website, </br>
Sonnet Website. </br>
[Marvell / Aquantia AQC](https://www.marvell.com/support/downloads.html) Website</br>
[Station Drivers](https://www.station-drivers.com/index.php/en-us/component/remository/Drivers/Marvell/LAN/AQC-107-108-100-113-114-115-...--and--AQN-107-108-100-.../lang,en-us/) Archive. </br>

Linux driver installs and works Ok in Kubuntu 20.10 Groovy Gorilla </br>
but GroovyGorilla is Not LTS. </br>
better install 20.04 LTS </br>

Windows8.1 also work OK, </br>
same Driver & same FW works for Both: </br>
ASUS XG-C100F PCIe & Sonnet Solo 10G SFP+ PCIe </br>
Trendnet v1 or v2 PCIe "Unknown / Untested" </br>

Asus has No drivers for OSX, </br>
Marvell AQC100 has No drivers for OSX, </br>
but Sonnet with same IC works since OSX HighSierra without drivers, </br>
because a partnership between Apple & Sonnet to develop HW for Apple. </br>
OSX detects Sonnet PID HID and loads the drivers.
but still needs tweaking, see Sonnet FAQ.

WARNING #1: </br>
FW upgrade does Not Jump from very old to latest. </br>
you need to download the Sonnet Firmware if you have a very old FW installed on Asus XG-C100F, </br>
Upgrade with Sonnet FW then upgrade to latest .121 from Marvell.  </br>
FW upgrade utility can also Downgrade, but i dont see the point. </br>
FW Upgrade utility gives an error, but PCIe card works Ok after Reboot. </br>
Requires real Windows10, Not Virtual. </br>
AQC100 are SFP+ </br>
the AQC107 seem are for RJ45. "Untested". </br>
FW upgrade utility can detect without Upgrade. </br>
type /? or /help </br>
in cmd as Administrator. </br>
install drivers Before doing the Upgrade, and reboot to see if card is Working ok before & after the FW Upgrade. </br>

i have W8.1x64 & Linux, dont like W10, or w11 </br>
W10 can be installed without Keys, will work Ok for 10minutes, enough to Upgrade the FW. </br>
W10 Requires a 120GB or Bigger SSD. </br>
a laptop with W10 does Not work, you need a PCIe slot. </br>

https://www.microsoft.com/en-us/software-download/windows10 </br>

WARNING #2. </br>
Do Not install W10x64 on a MacPro5,1 directly, will damage the UEFI. </br>
Windows10 will overwrite the Mac UEFI. </br>
you need a Real PC, </br>
or install Windows10 in MacPro 2010 with [twocanoes Winclone](https://twocanoes.com/products/mac/winclone/) </br>

Reboot to test if the New FW was detected Ok by the tool. </br>
Then W10 is No longer needed. </br>

Asus XG-C100* requires: 1500rpm fan or more, depending on Ambient °C. </br>
Heatsink is Big, Pretty, but is too far from Marvell / Aquantia IC with a foam. </br>

Will shutdown IF over heats. <---- </br>
Over heats easy with 800rpm case fan. </br>

Asus has a Dumb ass working in heatsink design, </br>
this happens since Asus Rampage III Extreme X58 era "since 2010", absolute worse heatsink design Award. </br>

SFP+ is a bit more $$ than RJ45 CAT6a, but is much better. </br>
for short distances "Short-Range modules" with 850nm laser, require OM1 or OM2 or OM3 MMF cable. </br>
LC-LC Fiber Optic cables are color coded "Orage". </br>
higher quality Fiver is very thin, for long distances. </br>

The cheapest 16x SFP+ Switch / Router is the MikroTik CRS317 16S+ </br>
there is also a smaller 8x SFP+ version with better CPU, and a smaller 4x SFP+ version with same CPU. </br>

The Step-Up is the CCR2004 12S+ has less SFP+ cages but faster Quad-Core ARM CPU. </br>
CCR1072 was previous Top of the Line, 72-core Amazon CPU, has 4x fans that Never Turn-Off, very $$$. </br>
has No CPU bottleneck. </br>
CRS317 has 2x fans and 2-Cores, Fans Turn-Off, temps are around 40°C with 20°C ambient. </br>

CPU bottle neck: </br>
CRS317 can give file transfers of large .iso files 3TB at 500MB/s, if your SSD M.2 is faster or using a RAM Drive. </br>
but 10G should give 1200MB/s </br>

