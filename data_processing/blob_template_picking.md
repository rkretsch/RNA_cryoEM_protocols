# Blob and Template Picking

### Cryosparc Blob Picking

Blob picking simply selects for a region of high signal with a specified radius and shape. Below are listed parameters which are not the default and should be adjusted according to evaluation of outputs:

- Minimum particle diameter
  - Use 20 A, as this is a good approximation for a head-on view of a helix
- Maximum particle diameter
  - Must estimate according to size of the RNA particle viewing
  - For a sample with <200 nt, can probably estimate a larger diameter of 150-250 A
  - This parameter is a good one to adjust after viewing the outputs in order to find the optimal value according to your sample
- Use circular blob AND elliptical blob
  - Elliptical blob for the helices
- Lowpass filter to apply (A)
  - Start with 5 and adjust visually
- Min separation dist (diameters)
  - 2.5 → will calculate for a minimum separation of 50 A between particles
  - This value is based off the min diameter

### Cryosparc Template Picking

First, create the “Template Picker” job. The templates are taken from a round of 2D classification you have already performed, so this job must be done after using another picker, such as the blob picker. Below are the relevant parameters:

- Particle diameter (A)
  - Estimated diameter in angstroms
- Lowpass filter to apply (A)
  - Start with 5, adjust visually
- Min. separation dist (diameters)
  - Recommend to have a separation distance of at least 50 A, so calculate what that fraction is (e.g. for a 150 A diameter, min sep distance is 0.33)
  - Can adjust visually

### Cryosparc Inpsect Picks

Create an “Inspect Picks” job to view the picker’s choices. Clicking into the interactive part of the job, can adjust the NCC threshold and the upper and lower limits for the power using sliders. Click through multiple micrographs and try to adjust this to minimize the selected noise and maximize selected particles. Click “Done” when satisfied with the thresholds.
