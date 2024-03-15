# PicoDiel

## Summary

Analyses of the diel responses of picocyanobacteria.

## Highly Qualified Personnel

- Douglas A. Campbell, Mount Allison University, dcampbel@mta.ca, ORCID 0000-0001-8996-5463

## Principle Investigators
- Mireille Savoie, Mount Allison University, msavoie@mta.ca, ORCID 0000-0003-3024-2687
- Sylwia Sliwinska-Wilczewska, Mount Allison University, University of Gdansk, ssliwinskawilczews@mta.ca, ORCID 0000-0002-3147-6605
- Marta Konik, University of Victoria, Institute of Oceanology, Polish Academy of Sciences, mk@iopan.gda.pl, ORCID 0000-0003-1145-9127
- Naaman Omar, Mount Allison University, nomar@mta.ca, ORCID 0000-0001-9583-2886
- Douglas A. Campbell, Mount Allison University, dcampbel@mta.ca, ORCID 0000-0001-8996-5463

## Primary Contact  

- Douglas A. Campbell, Mount Allison University, dcampbel@mta.ca, ORCID 0000-0001-8996-5463

## Data sources

Data sources chapter provide links to any data used from external providers:

- URL for MetaDataCatalog:
https://docs.google.com/spreadsheets/d/1ZXpwR7Gfto-uRzVdXzMpQF4frbrvMLH_IyLqonFZRSw/edit#gid=0

- URL for tMaxAHG Catalog:
https://docs.google.com/spreadsheets/d/1ksY7xlg9wOsICOBRmZkHPKdd9KOislNwPDzyuJ3UIUI/edit#gid=0


## Funding sources

- Canada Research Chair in Phytoplankton Ecophysiology (DAC)

- Latitude & Light; NSERC of Canada Discovery Grant (DAC)

## Keywords

Growth symmetry, Light intensity, PAR, Photoperiod, picocyanobacteria, PUR

## Additional information and support

- Sensitive Data Flag - Human Participants:  NO
- Sensitive Data Flag - Indigenous Partnerships: NO
- Sensitive Data Flag - Government Partnerships: NO
- Sensitive Data Flag - Industry Partnerships: NO
- Access Restrictions - NO

## Software  

The software (and version) used to create the dataset:

R version 4.2.2 (2022-10-31 ucrt) -- "Innocent and Trusting"
Copyright (C) 2022 The R Foundation for Statistical Computing
Platform: x86_64-w64-mingw32/x64 (64-bit)

## Repo content information

This chapter summarizes the structure of the repository with a decription of each folder, as applicable.

### Code

Code folder contains: Import_MCData.Rmd, Import_MetaData.Rmd, MCDielLight.Rmd, Merge_MCData.Rmd, Process_GrowthCurveData.Rmd, Process_GrowthRateSolisenseLRCData.Rmd, Process_GrowthSymmetryData.Rmd, Process_MCData.Rmd, Process_SolisenseLRCData.Rmd.

- Import_MCData.Rmd imports Multi-Cultivator MC247 and MC257 files from Data/RawData/MCData.zip folder and stores MultiCulti data in Data/ImportedData/ImportedMCData folder as: 
20211214_PICO_MC247_RUN39_TargetDataMetaFilter.Rds, 
20211223_PICO_MC257_RUN40_TargetDataMetaFilter.Rds, 
20211229_PICO_MC247_RUN43_TargetDataMetaFilter.Rds, 
20220107_PICO_MC257_RUN44_TargetDataMetaFilter.Rds, 
20220113_PICO_MC247_RUN45_TargetDataMetaFilter.Rds, 
20220122_PICO_MC257_RUN46_TargetDataMetaFilter.Rds,
20220206_PICO_MC257_RUN50_TargetDataMetaFilter.Rds
20220405_PICO_MC247_RUN60_TargetDataMetaFilter.Rds, 
20220410_PICO_MC257_RUN62_TargetDataMetaFilter.Rds, 
20220420_PICO_MC257_RUN65_TargetDataMetaFilter.Rds, 
20220507_PICO_MC257_RUN71_TargetDataMetaFilter.Rds, 
20220607_PICO_MC257_RUN74_TargetDataMetaFilter.Rds, 
20220615_PICO_MC257_RUN77_TargetDataMetaFilter.Rds, and
20230816_PICO_MC257_RUN121_TargetDataMetaFilter.Rds.

- Import_MetaData.Rmd imports culture MetaData Catalog from a google sheet and stored in Data/ImportedData/ImportedMetaData folder as: CultureCatalog.Rds.
  
- Merge_MCData.Rmd reads in all individually processed MultiCulti runs from the "/Data/ProcessedData/ProcessedMCData" folder and merges the data into 1 data frame. Growth estimate flags are defined based on absolute amplitude change. Growth estimates are set to 0 for models that returned a negative growth estimate and if the absolute amplitude change threshold was not met. For conditions that were replicated, a mean growth estimate was calculated. This single data frame is saved as a .Rds for further analysis called "PICO_Cleaned_MCData.Rds" in the "/Data/CleanedData/CleanedMCData" folder.

- Process_GrowthCurveData.Rmd separately processes and combines all .Rds from Data/ImportedData/ImportedMCData folder. This .Rmd generates PicoDiel_Processed_GrowthCurve.Rds (stored in Data/ProcessedData/ProcessedGrowthCurveData folder) and GrowthCurve_SupPlot.png (stored in Output/Plots folder).

- Process_GrowthRateSolisenseLRCData.Rmd processes and combines PicoDiel_Processed_GrowthRateAll.Rds from ProcessedGrowthRateData folder and PicoDiel_Processed_SolisenseJVPSII.Rds from ProcessedSolisenseData folder. 
This .Rmd generates PicoDiel_Processed_GrowthJVPSII.Rds (stored in ProcessedGrowthRateSolisenseData folder) and plots (stored in Output/Plots folder).

- Process_GrowthSymmetryData.Rmd processes Growth Symmetry (GS) catalog from a google sheet. This .Rmd generates PicoDiel_Processed_GrowthSymmetryData.Rds (stored in Data/ProcessedData/ProcessedGrowthSymmetryData folder) and plots (stored in Output/Figures folder).

- Process_MCData.Rmd processes and combines all .Rds from Data/ImportedData/ImportedMCData folder and creates: 
20211214_PICO_MC247_RUN39_ProcessDataNestGrowth.Rds, 
20211223_PICO_MC257_RUN40_ProcessDataNestGrowth.Rds, 
20211229_PICO_MC247_RUN43_ProcessDataNestGrowth.Rds, 
20220107_PICO_MC257_RUN44_ProcessDataNestGrowth.Rds, 
20220113_PICO_MC247_RUN45_ProcessDataNestGrowth.Rds, 
20220122_PICO_MC257_RUN46_ProcessDataNestGrowth.Rds, 
20220206_PICO_MC257_RUN50_ProcessDataNestGrowth.Rds, 
20220405_PICO_MC247_RUN60_ProcessDataNestGrowth.Rds, 
20220410_PICO_MC257_RUN62_ProcessDataNestGrowth.Rds, 
20220420_PICO_MC257_RUN65_ProcessDataNestGrowth.Rds, 
20220507_PICO_MC257_RUN71_ProcessDataNestGrowth.Rds, 
20220607_PICO_MC257_RUN74_ProcessDataNestGrowth.Rds, 
20220615_PICO_MC257_RUN77_ProcessDataNestGrowth.Rds, and
20230816_PICO_MC257_RUN121_ProcessDataNestGrowth.Rds

This .Rmd implements logistic growth curve fits to MultiCulti growth trajectories.

For Growth Symmetry: Process_MCData.Rmd also creates:
20211214_PICO_MC247_RUN39_ProcessDataNestGrowthFit.Rds,
20211223_PICO_MC257_RUN40_ProcessDataNestGrowthFit.Rds,
20211229_PICO_MC247_RUN43_ProcessDataNestGrowthFit.Rds,
20220107_PICO_MC257_RUN44_ProcessDataNestGrowthFit.Rds,
20220113_PICO_MC247_RUN45_ProcessDataNestGrowthFit.Rds,
20220122_PICO_MC257_RUN46_ProcessDataNestGrowthFit.Rds,
20220206_PICO_MC257_RUN50_ProcessDataNestGrowthFit.Rds,
20220405_PICO_MC247_RUN60_ProcessDataNestGrowthFit.Rds,
20220410_PICO_MC257_RUN62_ProcessDataNestGrowthFit.Rds,
20220420_PICO_MC257_RUN65_ProcessDataNestGrowthFit.Rds,
20220507_PICO_MC257_RUN71_ProcessDataNestGrowthFit.Rds,
20220607_PICO_MC257_RUN74_ProcessDataNestGrowthFit.Rds,
20220615_PICO_MC257_RUN77_ProcessDataNestGrowthFit.Rds,
20230816_PICO_MC257_RUN121_ProcessDataNestGrowthFit.Rds,

stored in ProcessedMCDataLogisticFit folder.

- Process_SolisenseLRCData.Rmd process PicoDiel_Imported_SolisenseLight_LRC.Rds stored in ImportedSolisenseData folder, process Turner Catalog (google sheet) and PicoDiel_Processed_PigmentsAll.Rds stored in ProcessedPigmentsData folder (contained cell/L for each ToD) and creates PicoDiel_Processed_SolisenseJVPSII.Rds stored in ProcessedSolisenseData folder.

### Data/CleanedData

Cleaned data in formats for long-term storage. CleanedData folder contains modified data with the appropriate column/row headers and data structure.

CleanedData folder contains 1 folder: CleanedMCData.

- Folder CleanedMCData contains PICO_Cleaned_MCData.Rds generated from Merge_MCData.Rmd (stored in Code folder).

### Data/ImportedData

Imported data in formats for long-term storage.

ImportedData folder contains: ImportedHourlyGrowth, ImportedMCData, ImportedMetaData, ImportedSolisenseData folders.

- Folder ImportedHourlyGrowth contains ImportedData_hourlyGrowth.Rds generated from Process_GrowthCurveData.Rmd (stored in Code folder).

- Folder ImportedMCData contains 
20211214_PICO_MC247_RUN39_TargetDataMetaFilter.Rds, 
20211223_PICO_MC257_RUN40_TargetDataMetaFilter.Rds, 
20211229_PICO_MC247_RUN43_TargetDataMetaFilter.Rds, 
20220107_PICO_MC257_RUN44_TargetDataMetaFilter.Rds, 
20220113_PICO_MC247_RUN45_TargetDataMetaFilter.Rds, 
20220122_PICO_MC257_RUN46_TargetDataMetaFilter.Rds,
20220206_PICO_MC257_RUN50_TargetDataMetaFilter.Rds
20220405_PICO_MC247_RUN60_TargetDataMetaFilter.Rds, 
20220410_PICO_MC257_RUN62_TargetDataMetaFilter.Rds, 
20220420_PICO_MC257_RUN65_TargetDataMetaFilter.Rds, 
20220507_PICO_MC257_RUN71_TargetDataMetaFilter.Rds, 
20220607_PICO_MC257_RUN74_TargetDataMetaFilter.Rds, 
20220615_PICO_MC257_RUN77_TargetDataMetaFilter.Rds, and
20230816_PICO_MC257_RUN121_TargetDataMetaFilter.Rds generated from Import_MCData.Rmd (stored in Code folder).

- Folder ImportedMetaData contains CultureCatalog.Rds generated from Import_MetaData.Rmd (stored in Code folder).

- Folder ImportedSolisenseData contains PicoDiel_Imported_SolisenseLight_LRC.Rds copy paste from BalticPhotoperiod repo. It is possible to generated this Rds. from Process_SolisenseLRCData.Rmd (stored in Code folder) after uncomment top chunks (It takes about 2h to run all).

### Data/ProcessedData

Processed data in formats for long-term storage.

ProcessedData folder contains: ProcessedGrowthCurveData, ProcessedGrowthRateData, ProcessedGrowthRateSolisenseData, ProcessedGrowthSymmetryData, ProcessedMCData, ProcessedMCDataLogisticFit, ProcessedMCDielLightData, ProcessedPigmentsData, ProcessedSolisenseData.

- Folder ProcessedGrowthCurveData contains PicoDiel_Processed_GrowthCurve.Rds generated from Process_GrowthCurveData.Rmd (stored in Code folder).

- Folder ProcessedGrowthRateData contains PicoDiel_Processed_GrowthRateAll.Rds generated from Process_GrowthRateData.Rmd (stored in Code folder in BalticPhotoperiod repository).

- ProcessedGrowthRateSolisenseData contains PicoDiel_Processed_GrowthJVPSII.Rds generated from Process_GrowthRateSolisenseLRCData.Rmd (stored in Code folder).

- Folder ProcessedGrowthSymmetryData contains PicoDiel_Processed_GrowthSymmetryData.Rds generated from Process_GrowthSymmetryData.Rmd (stored in Code folder).

- Folder ProcessedMCData contains: 20211214_PICO_MC247_RUN39_ProcessDataNestGrowth.Rds, 
20211223_PICO_MC257_RUN40_ProcessDataNestGrowth.Rds, 
20211229_PICO_MC247_RUN43_ProcessDataNestGrowth.Rds, 
20220107_PICO_MC257_RUN44_ProcessDataNestGrowth.Rds, 
20220113_PICO_MC247_RUN45_ProcessDataNestGrowth.Rds, 
20220122_PICO_MC257_RUN46_ProcessDataNestGrowth.Rds,
20220206_PICO_MC257_RUN50_ProcessDataNestGrowth.Rds, 
20220405_PICO_MC247_RUN60_ProcessDataNestGrowth.Rds, 
20220410_PICO_MC257_RUN62_ProcessDataNestGrowth.Rds, 
20220420_PICO_MC257_RUN65_ProcessDataNestGrowth.Rds, 
20220507_PICO_MC257_RUN71_ProcessDataNestGrowth.Rds, 
20220607_PICO_MC257_RUN74_ProcessDataNestGrowth.Rds, 
20220615_PICO_MC257_RUN77_ProcessDataNestGrowth.Rds, and
20230816_PICO_MC257_RUN121_ProcessDataNestGrowth.Rds generated from Process_MCData.Rmd (stored in Code folder).

- ProcessedMCDataLogisticFit contains: 20211214_PICO_MC247_RUN39_ProcessDataNestGrowthFit.Rds,
20211223_PICO_MC257_RUN40_ProcessDataNestGrowthFit.Rds,
20211229_PICO_MC247_RUN43_ProcessDataNestGrowthFit.Rds,
20220107_PICO_MC257_RUN44_ProcessDataNestGrowthFit.Rds,
20220113_PICO_MC247_RUN45_ProcessDataNestGrowthFit.Rds,
20220122_PICO_MC257_RUN46_ProcessDataNestGrowthFit.Rds,
20220206_PICO_MC257_RUN50_ProcessDataNestGrowthFit.Rds,
20220405_PICO_MC247_RUN60_ProcessDataNestGrowthFit.Rds,
20220410_PICO_MC257_RUN62_ProcessDataNestGrowthFit.Rds,
20220420_PICO_MC257_RUN65_ProcessDataNestGrowthFit.Rds,
20220507_PICO_MC257_RUN71_ProcessDataNestGrowthFit.Rds,
20220607_PICO_MC257_RUN74_ProcessDataNestGrowthFit.Rds,
20220615_PICO_MC257_RUN77_ProcessDataNestGrowthFit.Rds,
20230816_PICO_MC257_RUN121_ProcessDataNestGrowthFit.Rds generated from Process_MCData.Rmd (stored in Code folder).

xxxx

- Folder ProcessedPigmentsData contains BalticPhotoperiod_Processed_PigmentAll.Rds and BalticPhotoperiod_Processed_PigmentsExp.Rds generated from Process_PigmentsData.Rmd (stored in Code folder).

- Folder ProcessedSolisenseData contains BalticPhotoperiod_Processed_SolisensePigmentsAll.Rds generated from Process_SolisensePigmentsData.Rmd (stored in Code folder).

### Data/RawData

Raw data files in various formats contains original files generated by analytical equipment, received from a data provider or outside contractor.
Subfolders contain files from a single instrument.

RawData folder contains 6 zipped folders: JazEmData.zip, MCData.zip, OlisData.zip, PamasData.zip, SolisenseNSData.zip, and SolisenseOSData.zip.

- Folder JazEmData.zip contains files generated from Jaz radiospectrometer.
- Folder MCData.zip contains files generated from Multi-Cultivator MC247 and MC257.
- Folder OlisData.zip contains files generated from OLIS CLARiTY spectrophotometer.
- Folder PamasData.zip contains files generated from PAMAS counter.
- Folder SolisenseNSData.zip contains files generated from Solisense FRR kinetic fluorometer new software (NS).
- Folder SolisenseOSData.zip contains files generated from Solisense FRR kinetic fluorometer old software (OS).

### Docs

Docs folder contains: BalticPhotoperiod.bib and INSTRUCTIONS.md.

### Manuscript

Manuscript folder contains all the files needed to generate the manuscript.

### Output

Output from knit .Rmd, Figures and tables produced from analysis.

The Output folder contains 3 folders: Figures, FiguresRds, and TablesRds. 
- Folder Figures contains all plots that will be used in the final manuscript.
- Folder FiguresRds contains all .Rds needed to generate these plots.
- Folder TablesRds contains all tables that will be used in the final manuscript (also contain stats analysis).
  
### Data Dictionary

- URL for Data Dictionary:
https://docs.google.com/spreadsheets/d/1byJ7NV2LrHfzkcw9GQgZdQijKw1UbdzvtvZ1d1KL_cY/edit#gid=0

### Manuscript

- URL for main Manuscript:
https://docs.google.com/document/d/1rpUJyodvmd8ISzSk8PKRrZo73a6tK26yKlcucbD-EHI/edit

- URL for Supplementary materials:
https://docs.google.com/document/d/1mx0k0i898YFBWFq6-NiF_deLP90VUFrvjNK-PYeWEpI/edit#heading=h.pfv5hkliwuke

