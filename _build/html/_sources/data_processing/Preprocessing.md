# Pre-processing

#### Goal: to generate a set of micrographs from a given set of movies collected on a CryoEM microscope, including motion correction and CTF estimation. 

#### Introduction

Data is collected by the microscope in movies with the given number of frames specified by the user. The purpose of motion correction is to combine all the frames in the movie into a single micrograph. As the sample is hit with the electron beam, it tends to bend and move, so this job must include some correction to the image due to the motion of the sample throughout the movie. Motion correction also weighs the earlier frames more heavily than the later ones as the later frames have greater radiation damage. Then, the contrast transfer function (CTF) of each micrograph is calculated, which is the sinusoidal wave function representing the uneven transfer of information content as a function of spatial frequency. The CTF provides useful information about the quality of the micrograph. 

### Method

#### Import Movies

First, the movies collected by the camera must be imported into Cryosparc for further operations to take place. This is done using the job “Import Movies”. Parameters for this job are listed below. Data paths are input as usual and the other parameters are calculated from the microscope settings that were used during data collection.

- Movies data path 
- Gain reference path 
- Raw pixel size (A)
- Accelerating voltage (kV)
- Spherical aberration (mm)
    * This value is usually 2.7 mm
- Total exposure dose (e/A^2)

#### Motion Correction 

Next, the movies are motion corrected to combine them into a single micrograph. This includes correcting for the motion of the sample as it is hit by the electron beam, as well as weighing micrographs according to the amount of radiation damage (later frames weighed less). For this, you can use the job “Patch motion correction (multi)” on cryosparc. In most cases, all parameters can be kept as defaults for this job.

   * Note: for cryosparc patch-motion with falcon camera, you will need to exclude final frame (e.g. with 40 frames, put 39 as it counts from 0).

#### CTF estimation

Next, the parameters of the contrast transfer function (CTF) of each micrograph can be estimated. This provides useful information about the quality of the micrograph. Some of the parameters of the CTF include the defocus of the micrograph, the wavelength of electrons, and the spherical aberration. Defocus is the only parameter which will vary for a given dataset, therefore, CTF estimation is really estimating the defocus of each micrograph. CTF correction occurs when the program fits the observed CTF to a theoretical model, which generates a cross-correlation score and a resolution limit for the micrograph. CTF estimation and correction is done using the job “Patch CTF (multi)” in which most parameters can be kept as default in most situations.

[Grant Jensen, CTF](https://www.youtube.com/watch?v=mPynoF2j6zc&t=2s) 

[Grant Jensen, CTF Correction](https://www.youtube.com/watch?v=GYDLhg49UQA)

#### Curate Micrographs

Now that all micrographs are processed, you can manually reject those with bad ice or CTF correction. 

1. First, using the job “Exposure Tools”, split micrographs into groups of about 1000. 
2. Use the job “Curate Exposures” to manually look through each set of a thousand and find micrographs that are unusable. 
    * Check “Accept All” to accept all micrographs within the set.

        ![accept_all_exposures](accept_all_exposures.png)
        **Figure 1. “Accept all” in Curate Exposures job.**
        
    * Click the header of each column (e.g. “CTF Fit”) to show all micrographs arranged in order of that value.
    * Click through micrographs to find the threshold within each parameter in which the micrographs appear usable.
    * Click “Overview” and scroll down to the desired parameter.
    * Use the sliding bars to select those micrographs which fall outside the given threshold of usability, and check “Reject Selection”.
        
        ![reject_exposures](reject_exposures.png)
        **Figure 2. “Reject selection” on Curate Exposures job.**
        
    * When satisfied with all remaining micrographs, check “Done”. This will output the accepted exposures. 
        
        ![done_curating_exposures](done_curating_exposures.png)
        **Figure 3. “Done” in Curate Exposures job.**
        
3. Finally, use a second “Exposure Tools” job to combine all accepted micrographs into a single set.


