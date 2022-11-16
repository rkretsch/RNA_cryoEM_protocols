# Particle Picking

#### Goal:  to pick a stack of particles from a set of micrographs representing the molecule of interest.

### Introduction

The next step of the reconstruction process is to pick out the particles in the micrographs which are representative of your desired species and compile a stack of particles which are much smaller images of the molecule itself. There are multiple ways to achieve this; the first is blob picking, which simply selects for a region of high signal with a specified radius and shape. The second is template picking, which requires you to have already completed a 2D classification job and selected a set of views of the molecule. The algorithm then looks for particles which match the views or templates you have given it. Another method is deep picking, which uses a neural network to select particles. Using this method requires having hand-picked or curated a set of several thousand particles in order to train the model. After using a picker, which finds the locations of particles, you can inspect those picks and choose desired parameters of the cross correlation of the signal with the parameters of the picker, as well as the thresholds of the power of the signal. Finally, you must extract a stack of smaller views of the particles themselves from the micrographs, which can then be used for later jobs.

## Methods

#### Blob Picking

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

#### Template Picking

First, create the “Template Picker” job. The templates are taken from a round of 2D classification you have already performed, so this job must be done after using another picker, such as the blob picker. Below are the relevant parameters: 

- Particle diameter (A)
    - Estimated diameter in angstroms
- Lowpass filter to apply (A)
    - Start with 5, adjust visually 
- Min. separation dist (diameters)
    - Recommend to have a separation distance of at least 50 A, so calculate what that fraction is (e.g. for a 150 A diameter, min sep distance is 0.33)
    - Can adjust visually

    
#### Inspect Picks

Create an “Inspect Picks” job to view the picker’s choices. Clicking into the interactive part of the job, can adjust the NCC threshold and the upper and lower limits for the power using sliders. Click through multiple micrographs and try to adjust this to minimize the selected noise and maximize selected particles. Click “Done” when satisfied with the thresholds.

#### Extract From Micrographs

Create the job “Extract From Micrographs” using the outputs from Inspect Picks. This will generate your particle stack which can then be used for 2D classification. Below are the adjusted parameters. 

- Extraction box size (pix)
    - Calculate this by using the estimated maximum diameter of the particle and the raw pixel size of the data
    - Overestimate box size by about 1.5-2x the max diameter of the particle 
    - Round your calculated box size to the closest of the following values: 
        - 16, 20, 24, 28, 32, 36, 40, 48, 56, 60, 64, 72, 80, 84, 96, 100, 108, 112, 120, 128, 140, 144, 160, 168, 180, 192, 196, 200, 216, 224, 240, 252, 256, 280, 288, 300, 320, 324, 336, 360, 384, 392, 400, 420, 432, 448, 480, 500, 504, 512, 540, 560, 576, 588, 600, 640, 648, 672, 700, 720, 756, 768, 784, 800, 840, 864, 896, 900, 960, 972, 980, 1000, 1008, 1024, 1080, 1120, 1152, 1176, 1200, 1260, 1280, 1296, 1344, 1372, 1400, 1440, 1500, 1512, 1536, 1568, 1600, 1620, 1680, 1728, 1764, 1792, 1800, 1920, 1944, 1960, 2000
- Fourier crop to box size (pix)
    - Change this parameter if your extraction box size is above 200 pixels
    - Choose a value of 200 pixels or smaller, but make sure you are choosing a value from the above list



