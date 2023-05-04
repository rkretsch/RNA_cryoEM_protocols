# CTF Estimation



### Introduction

Next, the parameters of the contrast transfer function (CTF) of each micrograph can be estimated. This provides useful information about the quality of the micrograph. Some of the parameters of the CTF include the defocus of the micrograph, the wavelength of electrons, and the spherical aberration. Defocus is the only parameter which will vary for a given dataset, therefore, CTF estimation is really estimating the defocus of each micrograph. CTF correction occurs when the program fits the observed CTF to a theoretical model, which generates a cross-correlation score and a resolution limit for the micrograph. 

```{seealso}
[Grant Jensen, CTF](https://www.youtube.com/watch?v=mPynoF2j6zc&t=2s) 

[Grant Jensen, CTF Correction](https://www.youtube.com/watch?v=GYDLhg49UQA)
```



````{tab-set}
```{tab-item} Cryosparc Patch CTF
CTF estimation and correction is done using the job “Patch CTF (multi)” in which most parameters can be kept as default in most situations.

```
```{tab-item} CTFfind4
TODO
```
````
