#  *in vitro* Transcription (IVT) 

__Goal__: Create the RNA of interest from the DNA template.

__Time__: ~0.5hrs - 4-overnight wait - ~1.5hrs

#### Introduction

T7 polymerase catalyzes the formation of RNA from DNA in the 5’-->3’ direction. It will read the 5’-->3’ strand of our DNA template and use NTPs to create the complementary RNA strand. T7 is extremely specific for its promoter which we inserted at the start of our construct, so most of our product should be the length of our dsDNA we put in minus the promoter region which T7 does not transcribe. We then clean up our IVT reaction using Zymo RCC columns and quantify how much RNA we have at this stage.

#### Materials:

- [dsDNA]
- Heat blocks
- TranscriptAid kit
- Zymo RNA Clean & Concentrator 25
- ddH2O
- NanoDrop
- 100% EtOH

### Method

:::{dropdown} {material-regular}`format_list_numbered` 1. IVT with TranscriptAid

1. You want to aim for 2000ng/reaction, and for cryo-EM often want 3 reactions total. For each reaction you have:
    * 8µL NTPs (25mM)
    * 4µL 5x buffer
    * 2000ng DNA or less
    * 2µL T7 mix *add last
    * ddH2O to bring to 20µL
1. Incubate at 37&deg;C for minimum 4 hours, especially if you have a mutant promoter do this overnight, if PAGE-purifying it is safe to run all overnight (off-products from running too long are generally a different length). Note down time incubated for.
2. Add 2µL DNase I per reaction. Incubate 15min at 37&deg;C to digest any left over DNA.

:::

:::{dropdown} {material-regular}`format_list_numbered` 2. RNA Column Purification

1. Move to IVT solution to 1.5mL tube. Add 2xIVT volume binding buffer and 3xIVT volume 100% EtOH to sample and mix well.
    * Note - for RNAs < 200 nt, add 4.5xIVT volume of 100% ethanol (e.g. for an IVT with a volume of 66 uL, add 132 uL binding buffer and 297 uL 100% EtOH). 

2. Add into the zymo RCC column, 700µL at a time. Wait 5min. Spin at 13,000g for 1min. Discard flow-through. Repeat until all the solution is added to the column.

3. Add 400µL of Prep-Buffer to the column. Spin at 13,000g for 1min. Discard flow-through.

4. Add 700µL of Wash Buffer to the column. Spin at 13,000g for 30sec. Discard flow-through.

5. Add 400µL of Wash Buffer to column. Spin at 13,000g for 30sec. Discard flow-through.

6. Spin at 13,000g for 2min.

7. *Optional:* Move column to well labeled 1.5mL tube. Dry 15min with cap open.

8. Add 30µL of ddH2O to elute. Wait 5 min. Spin at 13,000g for 30sec.

9. Immediately in -80&deg;C!

    :::

    :::{dropdown} {material-regular}`format_list_numbered` 3. RNA Quantification

    1. Dilute RNA [5x and/or 25x dilution recommended: 2µL ddH2O and 0.5µL sample in PCR tube] If you bring your own pipette to the non-RNAse free nanodrop, wipe it off with RNAse zap before using again.
    2. Wipe down the NanoDrop. Calibrate with 1µL ddH20. Set to RNA. 
    3. Blank and zero with 1µL ddH2O. 
    4. Load 1µL of sample, take measurement.
    5. Check for contaminants. Expect A260/A280~2.1. Do not want a 230 shoulder.  Generally, if A260 above 70 needs to dilute further. 
    6. Write down: A260, A280, and Reported ng/µL. 
    7. Calculate concentration: RNA (μM) = [A260 x 40,000] / [330 x length (bp)]

    :::
