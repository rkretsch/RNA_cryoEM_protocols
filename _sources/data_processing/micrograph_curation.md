# Micrograph Curation



### Cryosparc

Now that all micrographs are processed, you can manually reject those with bad ice or CTF correction.

1. First, using the job “Exposure Tools”, split micrographs into groups of about 1000.

2. Use the job “Curate Exposures” to manually look through each set of a thousand and find micrographs that are unusable.

   - Check “Accept All” to accept all micrographs within the set.

     ![accept_all_exposures](accept_all_exposures.png) **Figure 1. “Accept all” in Curate Exposures job.**

   - Click the header of each column (e.g. “CTF Fit”) to show all micrographs arranged in order of that value.

   - Click through micrographs to find the threshold within each parameter in which the micrographs appear usable.

   - Click “Overview” and scroll down to the desired parameter.

   - Use the sliding bars to select those micrographs which fall outside the given threshold of usability, and check “Reject Selection”.

     ![reject_exposures](reject_exposures.png) **Figure 2. “Reject selection” on Curate Exposures job.**

   - When satisfied with all remaining micrographs, check “Done”. This will output the accepted exposures.

     ![done_curating_exposures](done_curating_exposures.png) **Figure 3. “Done” in Curate Exposures job.**

3. Finally, use a second “Exposure Tools” job to combine all accepted micrographs into a single set.
