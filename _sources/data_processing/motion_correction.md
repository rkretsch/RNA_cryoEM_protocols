# Motion Correction

### Cryosparc

Next, the movies are motion corrected to combine them into a single micrograph. This includes correcting for the motion of the sample as it is hit by the electron beam, as well as weighing micrographs according to the amount of radiation damage (later frames weighed less). For this, you can use the job “Patch motion correction (multi)” on cryosparc. In most cases, all parameters can be kept as defaults for this job.

- Note: for cryosparc patch-motion with falcon camera, you will need to exclude final frame (e.g. with 40 frames, put 39 as it counts from 0).
