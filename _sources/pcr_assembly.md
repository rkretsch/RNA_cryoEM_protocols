# PCR assembly



#### Goal: Create the dsDNA that will be the template to create your RNA of interest. 



#### General notes: 

- If the assembly fails, first try another polymerase.

#### Introduction: 

We need to go from the cheap short ssDNA oligos we ordered to the dsDNA which will transcribe to create our RNA of interest. To do this we conduct an PCR assembly reaction. In short, our oligos overlap with each other so they can anneal to each other. This creates multiple primed sites for PCR reactions. The complete dsDNA will be completed in the extension steps. Using a construct designed by primerize this normally succeeds in making the dsDNA we want. Check the assembly with a gel confirming the expected length dsDNA is present and checking for side-products. If there are significant side-products you may want to gel-purify the correct sized products, however it may be ok to proceed if you will exclude these products in dPAGE purification of the RNA. Note, if you have a epPCR primer site at the end of your construct you will want to remove this before transcribing the RNA for cryo-EM, this requires a digest, another column purification, and checking on the gel to see the size has reduced by the expected amount. Finally, we need to quantify how much dsDNA we have in order to calculate the amount to use for the transcription step.

Note in future, if you have this complete dsDNA construct, you can amplify it using traditional PCR and the first forward primer and last reverse primer.

#### Material: 

- Oligos from IDT

- ddH2O

- dNTPs

- Polymerase and associated buffer (e.g. Phusion and 5x HF Buffer)

- ~1.5hr on thermocycler

- TBE 1x ~150mL

- SYBR Safe

- dsDNA ladder

- 6x Loading dye

- Agarose

- Gel doc

- QIAquick spin columns

- Buffer PB*

- Buffer PE* or 80% EtOH

- Centrifuge

- Nanodrop

  \* recipes available

### Method

#### 1a. Primer MasterMix

1. Check primer concentration (often ~100µM), label primers on cap.
2. Create a MM with 12.5µM first and last primer (eg 50µL), and 0.125µM others (eg 0.5µL) (eg in 400µL total). You can save MM for future reactions, store at -20°C. [**primer MM**].

#### 1b. Physion MasterMix and PCR preparation

3. Before starting, make sure there is a thermocycler available and reserve with tape.
4. Each standard reaction is 50µL, recommend 4 standard reactions per assembly. Label PCR tubes for each assembly. *Recognize the capacity of your thermocycler, if it is 100µL and you want 4 standard reactions per assembly, each assembly will need to be done in 2 PCR tubes (100µL each, 200µL total).*
5. For each assembly add 16µL of [**primer MM**] per standard reaction (eg 64µL for 4 standard reactions) directly to the PCR tubes.
6. Make a Phusion MM for 1.1x the number of reactions you need (number of assemblies x number of standard reactions per assembly). Per reaction you need:
   	22µL ddH2O
   	10µL HF-buffer
   	1µL dNTPs (10mM)
   	1µL Phusion polymerase **add last minute*
   Vortex and spin down.
7. Add 34µL of Phusion MM per standard reaction to each of your PCR tubes.
8. Vortex and spin down. Immediately place in thermocycler

#### 1c. PCR cycles

9. Set the following program on thermocycler (likely saved)
   98oC 30sec
   35x[98oC 10sec
       64oC 30sec *(check annealing temp of oligos, can go a few* *°C above min Tm)*
       72oC 30sec] *(may need to extend if longer construct, 15-30 per kb)*
   72oC 10min
   12oC inf

#### 1d. Agarose gel

#### 1e. dsDNA column purification



sub note is DNA gel purificaition

TODO different assembly enzymes
