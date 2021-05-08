
# TWRP tree foe Infinix Hot 10 Play
# Infinix Hot 10 Play Specs Sheet

>Dual Sim, 3G, 4G, VoLTE, Wi-Fi
>Helio G35, Octa Core, 2.3 GHz Processor
>4 GB RAM, 64 GB inbuilt
>6000 mAh Battery
>6.82 inches, 720 x 1640 px Display with >Water Drop Notch
>13 MP Dual Rear & 8 MP Front Camera
>Memory Card Supported, upto 256 GB
>Android v10
released : January 21,2021

# How to build TWRP now?

Clone minimal TWRP environment
Follow the instruction in this page
https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni

Remember to clone the correct version of TWRP based on what Android version your phone have! If your phone have Android 8.0, clone twrp-8.0 branch

Move device tree to TWRP sources
Copy working/(brand)/(device) folder to device/(brand)/(device) folder in TWRP sources
Example:

brand name: Infinix 
device codename: X688C
Copy working/Infinix/X688C to device/xiaomi/whyred in TWRP sources
Building
Open a terminal with the current dir pointing to TWRP sources root
Then type
. build/envsetup.sh
to initialize the environment

After that, type
lunch omni_codename-eng
where codename is the codename of your phone

If that is successful, type
mka recoveryimage
to build the recovery

If also that is successful, congratulation!
Go to out/target/product/codename/ (codename is your device codename) and you will find your recovery.img
