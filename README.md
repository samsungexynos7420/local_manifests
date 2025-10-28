# LineageOS 19.1 local_manifests
Lineage OS 19.1 manifest for Samsung S6, S6 edge, S6 edge+ and Note5.

## Steps to build  
1) Set up an initial lineage-19.1 build environment following official lineage instructions
2) Clone 7420_patches (lineage-19.1 branch) in your home folder
``
git clone https://github.com/samsungexynos7420/7420_patches --branch lineage-19.1
``

Follow instructions in that branch. **THIS STEP IS MANDATORY TO GET A FULLY WORKING DEVICE**   
3) Copy universal7420.xml to {ANDROID_ROOT}/.repo/local_manifests/roomservice.xml - create the folder if it doesnt exist 
4) Return to {ANDROID_ROOT} and repo sync
5) source build/envsetup.sh  
6) lunch lineage_[codename]-userdebug  
Replace codename with the device you are trying to build.
Valid codenames:
- zeroflte : for the FLAT version of the S6 (G920F/S/K/I/L/W8)
- zerolte: for the EDGE version of the S6 (G925F/S/K/I/L/W8)
- noblelte: for the Note 5 International (N920C/S/K/I/L/W8)
- zenlte: for the EDGE+ version of the S6 (G928F/C/S/K/I/L/W8)

7) make bacon -j[cpucorecount]  
Replace core count with the number of CPU cores you want to use for building.
