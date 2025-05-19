# LineageOS 18.1 local_manifests
Lineage OS 18.1 manifest for Samsung S6, S6 edge, S6 edge+ and Note 5

Steps to build
1. Setup a Lineage 18.1 build environment according to official LineageOS documentation
2. Clone 7420_patches (lineage-18.1 branch) and follow the instructions to apply them. This isn't required, but you should probably apply them
3. Copy universal7420.xml to {ANDROID_ROOT}/.repo/local_manifests/roomservice.xml - create the folder if it doesnt exist
4. Return to {ANDROID_ROOT} and repo sync
5. source build/envsetup.sh
6. lunch lineage_[codename]-userdebug
7. make bacon -j[cpucorecount]

Replace codename with the device you are trying to build. Valid codenames:

- zeroflte: the FLAT version of the S6 (G920)
- zerolte: the EDGE version of the S6 (G925)
- zenlte: the EDGE PLUS (EDGE+) version of the S6 (G928)
- noblelte: for the Note 5 (N920)
  
Replace core count with the number of CPU cores you have.

## Supported Devices:  
- G920 F/S/K/I/L/W8/T
- G925 F/S/K/I/L/W8/T
- G928 F/S/K/C/I/L/G/W8/T
- N920 C/S/K/I/L/W8/T
