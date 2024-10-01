# LineageOS 20 local_manifests
This is the current Exynos 7420 manifest for LineageOS 20 (Android 13). These repos are only validated to build lineage ROMs. Any other custom ROM is unsupported and contacting me is likely to result in no support conisdering the sheer amount of custom ROMs there are.

## Steps to build  
1) Clone Lineage 20 repo and setup your build environment according to the lineage documentation  
2) Clone 7420_patches (lineage-20 branch) and follow the instructions to apply them. **THIS IS REQUIRED FOR WORKING BUILDS AND IS MANDATORY**  
3) Copy universal7420.xml to {ANDROID_ROOT}/.repo/local_manifests/roomservice.xml - create the folder if it doesnt exist 
4) Return to {ANDROID_ROOT} and repo sync
5) source build/envsetup.sh  
6) lunch lineage_[codename]-userdebug  
7) make bacon -j[cpucorecount]  

Replace codename with the device you are trying to build.
Valid codenames:
- zerofltexx : for the FLAT version of the S6 (G920F/I/S/K)
- zeroltexx: for the EDGE version of the S6 (G925F/I/S/K)

Replace core count with the number of CPU cores you have.
