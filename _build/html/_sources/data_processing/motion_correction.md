# Motion Correction

## Introduction

Next, the movies are motion corrected to combine them into a single micrograph. This includes correcting for the motion of the sample as it is hit by the electron beam, as well as weighing micrographs according to the amount of radiation damage (later frames weighed less). 

````{tab-set}
```{tab-item} Cryosparc Patch Motion
For this, you can use the job “Patch motion correction (multi)” on cryosparc. In most cases, all parameters can be kept as defaults for this job.

:::{warning}

For cryosparc patch-motion with falcon 4 camera, you will need to exclude final frame (e.g. with 40 frames, put 39 as it counts from 0).

:::
```
```{tab-item} Motioncor2
TODO
```
````



