# 3D reconstruction

## Potential problems

### Mask artifacts

If you see an FSC curve with jumps such as this: 

![fsc_mask_artifact](fsc_mask_artifact.png)

Then it is possible that there are issues with the mask size fitting too tightly, in which case it is recommended to try to increase the mask size. To do this, change the following parameters: 



### Cryosparc Non-Uniform Refinement

After performing Ab Initio and any additional necessary refinement jobs, you should then perform non-uniform refinement on your final particle stack and volume in order to obtain a high resolution final model with a gold standard resolution estimate in Angstroms and an FSC curve. This job we typically run with default parameters, although it is best to evaluate the FSC curve after the job has been completed. 
