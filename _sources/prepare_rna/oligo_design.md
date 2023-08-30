# Oligo design

Materials:

- Target sequence(s)
- Access to primerize (online or downloaded)
- $ on IDT or other synthesizers

Resources:

- [Primerize-design tool](https://primerize.stanford.edu/design_1d/) 

- [Primerize-design](https://primerize.stanford.edu/protocol/#temp_design) 

- [Primerize-IDT ordering](https://primerize.stanford.edu/protocol/#idt_bulk) 

Sequences

```
> T7
TTCTAATACGACTCACTATA

> Phi2_5
TTCTAATACGACTCACTATT

> T7C
TTCTAATACCACTCACTATA

> Phi2_5C
TTCTAATACCACTCACTATT

> MlyI primer
GCATTGACTCTATTCAATAC

> BsaI_primer
GCATTGAGACCATTCAATAC
```

1. Add a promoter for T7 polymerase to the 5’ end of your sequences

2. 1. Note having a target sequence that starts with GG makes transcription much more efficient, but T7 will transcribe it all!
   2. If sequence starts with G: T7
   3. Otherwise: Phi2.5

3. *If you are likely going to be determining the secondary structure of the RNA in addition to cryo-EM add to the 3’ end one of our designed epPCR primers which can be digested off*

4. 1. *BsaI_epPCR primer*

   2. 1. *Check if your promoter+sequence+G contains ["GGTCTC","GAGACC"], note if you use U or T!*
      2. *If it doesn’t you can add on the BsaI primer to the 3’ end of your sequence.*

   3. *MlyI_epPCR primer*

   4. 1. *The promoters have the MlyI cut-site so change promoters to T7C or Phi2.5C*
      2. *Check if your promoter+sequence+G contains ["GAGTC","GACTC"] note if you use U or T!*
      3. *If it doesn’t you can add on the MlyI primer to the 3’ end of your sequence.*

5. The dsDNA you want to create is promoter+sequence(+epPCR primer if applicable).

6. Use primerize to find a set of oligos for PCRassembly.

7. 1. Input the sequence (can be rna, dna or mix), and name sequence (eg P4P6_T7_MlyI)
   2. Uncheck T7 promoter check if using online primerize
   3. Start with minimum Tm 60 and maximum length 60.
   4. If you receive a warning try again increasing length to 90 and then 100 (for IDT these are the price boundaries for other services this may differ).
   5. If still no luck, you can vary Tm.

8. Download the successful primerize run. Copy from the bottom of the file the bulk order of the oligos. (Note min Tm from output as well).

9. On IDT go to custom DNA orders in tubes (if large amounts can do plate)

10. Input the copied oligos into “bulk input”, it will automatically fill in a lot but you must still check for each oligo:

11. 1. Formulation: LabReady
    2. Purification: Standard desalting
    3. In general we want the smallest amount of oligo that they allow (<60nt 25nmol, <90nt 100nmol, <100nt 250nM, hence the price increase)

12. Add it to order, order on whichever card is applicable, keep track of your ordered oligos in a spreadsheet.