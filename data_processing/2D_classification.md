# 2D Classification

**Goal**: to classify particles into groups representing various two dimensional views of the entire molecule. 

Once you have a stack of particles representing your molecule, you can classify each of those views into a 2D orientation of that molecule. Since there are thousands of particles suspended in the ice in different orientations, each particle must be classified with other particles that resemble it, so we have groups of particles in separate orientations. 

````{tip}
```{admonition} Selecting 2D classes
Parameters used to consider whether or not to select a class include: the clarity/resolution of the class, the number of particles in the class, if the full particle is visible. Additionally, try to select classes which represent all orientations. For RNA reconstruction, it is best to keep all particles that resemble RNA molecules at this stage. The goal is to strike a balance between keeping particle numbers high while removing “junk” or noise. 
```
````





````{tab-set}
```{tab-item} Cryosparc 

Create a “**2D Class”** job. The inputs for this job are the particles which have been extracted from a micrograph using the “Extract from Micrographs” job. 

The following parameters are helpful to modify for this job:

- Number of 2D classes

- - The default value is 50, but can try a range from 40, 80, 100, etc.

- Maximum resolution (A)

- - Default is 6, but can increase resolution at later stages 
  - Recommended to keep it at 6 after initial blob picking

- Initial classification uncertainty factor 

- - Controls the initial search for 2D references
  - A lower number (e.g. 2-3) will give more junk classes (this is useful in the first few rounds of 2D class to help eliminate noise)
  - A higher number (8-10) will result in a higher diversity of “better” or more refined classes (this is useful in the later steps of the process)
  - Recommended to stick with 2 at this stage in the process

- Circular mask diameter (A)

- - Estimate how large of a window is necessary to view the whole particle in angstroms

- Circular mask diameter outer (A)

- - Can have a larger gradient from visible to opaque to see outer edges of the particle 

- Number of online-EM iterations

- - Should increase this to at least 30-40 (helpful for smaller particles)

- Batchsize per class

- - Increase to at least 200-300 (better for smaller particles)

​	Again, might need to run a few rounds of this job trying out different parameters (esp diameter size) in order to determine optimal values. 

​	Finally, create the “**Select 2D classes”** job in order to interactively view the 2D classes created from the previous job. 
```
````