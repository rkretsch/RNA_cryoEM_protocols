# Pre-processing

__Goal__: to generate a set of micrographs from a given set of movies collected on a CryoEM microscope, including motion correction and CTF estimation.

## Introduction

Data is collected by the microscope in movies with the given number of frames specified by the user. The purpose of motion correction is to combine all the frames in the movie into a single micrograph. As the sample is hit with the electron beam, it tends to bend and move, so this job must include some correction to the image due to the motion of the sample throughout the movie. Motion correction also weighs the earlier frames more heavily than the later ones as the later frames have greater radiation damage. Then, the contrast transfer function (CTF) of each micrograph is calculated, which is the sinusoidal wave function representing the uneven transfer of information content as a function of spatial frequency. The CTF provides useful information about the quality of the micrograph.
