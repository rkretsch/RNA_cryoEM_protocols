# Ab Initio 3D reconstruction

__Goal__: To create an initial three-dimensional model from the stack of 2D particle views.

## Introduction

After creating and curating your particle stack by evaluating the 2D views, it is time to move into three-dimensional space. The task of the algorithm is to generate a rough, initial model (or multiple models) for how all the 2D views might align together with their various relative orientations (i.e. what is the top view, what is a view from the right side, the bottom, etc.). Later on, this model can be further refined and the resolution greatly improved by further particle classification and refinement steps. 

## Expected results

After running this job, you can view the initial models. Look for RNA-like features, especially major and minor helical grooves. Running this job with multiple classes will allow you to identify “junk” classes and “good” classes. The “junk” classes can be used as a sink for “junk” or noise particles. 

### Cryosparc

Create an **“Ab-Initio Reconstruction”** job. Below are the adjustable parameters: 

- Number of Ab-Initio classes

- - The number of initial models the job will create for you 
  - Default is 1, but you can increase this to at least 2 or 3 in order to identify junk classes - try to play around with this number and see what produces the best initial models 

- Maximum resolution (Angstroms)

- - The max resolution should be 8A, as helical features cannot be seen until at least 10A

- Initial resolution (Angstroms)

- - Increase to 15A or 25A (can do 2 jobs with each and see which is better)

- Number of initial iterations

- - Increase this to at least 400

- Number of final iterations

- - Increase this to at least 600

- Initial minibatch size

- - Increase this to at least 300

- Final minibatch size

- - Increase this to at least 1000

- Class similarity

- - How similar the initial models are that the algorithm creates - default is 0.1, but you can try changing this number to see if you get better results 
