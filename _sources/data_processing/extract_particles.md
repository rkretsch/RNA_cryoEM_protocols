# Extract Boxed Particles

### Cryosparc Extract From Micrographs

Create the job “Extract From Micrographs” using the outputs from Inspect Picks. This will generate your particle stack which can then be used for 2D classification. Below are the adjusted parameters.

- Extraction box size (pix)
  - Calculate this by using the estimated maximum diameter of the particle and the raw pixel size of the data
  - Overestimate box size by about 1.5-2x the max diameter of the particle
  - Round your calculated box size to the closest of the following values:
    - 16, 20, 24, 28, 32, 36, 40, 48, 56, 60, 64, 72, 80, 84, 96, 100, 108, 112, 120, 128, 140, 144, 160, 168, 180, 192, 196, 200, 216, 224, 240, 252, 256, 280, 288, 300, 320, 324, 336, 360, 384, 392, 400, 420, 432, 448, 480, 500, 504, 512, 540, 560, 576, 588, 600, 640, 648, 672, 700, 720, 756, 768, 784, 800, 840, 864, 896, 900, 960, 972, 980, 1000, 1008, 1024, 1080, 1120, 1152, 1176, 1200, 1260, 1280, 1296, 1344, 1372, 1400, 1440, 1500, 1512, 1536, 1568, 1600, 1620, 1680, 1728, 1764, 1792, 1800, 1920, 1944, 1960, 2000
- Fourier crop to box size (pix)
  - Change this parameter if your extraction box size is above 200 pixels
  - Choose a value of 200 pixels or smaller, but make sure you are choosing a value from the above list