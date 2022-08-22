# *in vitro* transcription (IVT)



#### Goal: to create the RNA of interest from the DNA template

#### Introduction: 

T7 polymerase catalyzes the formation of RNA from DNA in the 5’-->3’ direction. It will read the 5’-->3’ strand of our DNA template and use NTPs to create the complementary RNA strand. T7 is extremely specific for its promoter which we inserted at the start of our construct, so most of our product should be the length of our dsDNA we put in minus the promoter region which T7 does not transcribe. We then clean up our IVT reaction using Zymo RCC columns and quantify how much RNA we have at this stage.
Materials:
[**dsDNA**]Heat blocksTranscriptAid kitZymo RNA Clean & Concentrator 25ddH2ONanoDrop100% EtOH

### Method

#### 2a. IVT with TranscriptAid

##### ~*4hours-overnight*

1. You want to aim for 2000ng/reaction, and for cryo-EM often want 3 reactions total. For each reaction you have:8µL NTPs (25mM)
   	4µL 5x buffer
   	2000ng DNA or less
   	2µL T7 mix **add last*
   	ddH2O to bring to 20µL**
2. Incubate a 37oC for minimum 4 hours, especially if you have a mutant promoter do this overnight, if PAGE-purifying it is safe to run all overnight (off-products from running too long are generally a different length). Note down time incubated for.
3. Add 2µL DNase I per reaction. Incubate 15min at 37oC to digest any left over DNA.

#### 2a. Column Purify RNA 

##### *~1hour*

Move to IVT solution to 1.5mL tube. Add 2xIVT volume binding buffer and 3xIVT volume 100% EtOH to sample and mix well.Add into the zymo RCC column, 700µL at a time. Wait 5min. Spin at 13,000g for 1min. Discard flow-through. Repeat until all the solution is added to the column.Add 400µL of Prep-Buffer to the column. Spin at 13,000g for 1min. Discard flow-through.Add 700µL of Wash Buffer to the column. Wait 1min. Spin at 13,000g for 30sec. Discard flow-through.Add 400µL of Wash Buffer to column. Wait 1min. Spin at 13,000g for 30sec. Discard flow-through.Spin at 13,000g for 2min.Move column to well labeled 1.5mL tube. Dry 15min with cap open.Add 15µL of ddH2O to elute. Wait 5min. Spin at 10,000g for 30sec.Add 15µL of ddH2O to elute. Wait 5min. Spin at 10,000g for 30sec.Immediately in -80oC!

#### 2c. RNA Quantification

~10min

*Dilute RNA [5x and/or 25x dilution recommended: 2µL ddH2O and 0.5µL sample in PCR tube] *If you bring your own pipette to the non-RNAse free nanodrop, wipe it off with RNAse zap before using again.*Wipe down the NanoDrop. Set to RNA. Blank and zero with 1µL ddH2O. Load 1µL of sample, take measurement.Check for contaminants. Expect A260/A280~2.1. Do not want a 230 shoulder. Generally, if A260 above 70 needs to dilute further. Write down: A260, A280, and Reported ng/µL. Calculate concentration: RNA (μM) = [A260 x 40,000] / [330 x length (bp)]
