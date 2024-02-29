---
title: "Changing diel growth symmetries and light-capture in PhycoCyanin and PhycoErythrin-rich picocyanobacteria, across photic regimes and growth phases"
author:
- Sylwia Śliwińska-Wilczewska:
    institute:
    - MTA
    - UG
    email: ssliwinskawilczews@mta.ca
- Marta Konik:
    institute:
    - VU
    - IOPAN
    email: mk@iopan.gda.pl
- Mireille Savoie:
    institute: MTA
    email: msavoie@mta.ca
- Naaman Omar:
    institute: MTA
    email: nomar@mta.ca
- Douglas A. Campbell:
    institute: MTA
    email: dcampbel@mta.ca
    correspondence: true
institute:
- MTA: Department of Biology, Mount Allison University, 53 York St., Sackville NB,
    Canada, E4L 1C9
- UG: "Institute of Oceanography, University of Gdansk, 46 Pilsudskiego St, P81-378,
    Gdynia, Poland"
- VU: Department of Geography, University of Victoria, Victoria, BC V8P 5C2, Canada
- IOPAN: "Institute of Oceanology, Polish Academy of Sciences, 81-712 Sopot, Poland"
output:
  bookdown::word_document2:
    reference_docx: Template.docx
    code-folding: show
    keep_md: yes
    fig.caption: yes
    toc: FALSE
    pandoc_args:
    - "--lua-filter=scholarly-metadata.lua"
    - "--lua-filter=author-info-blocks.lua"
  html_document:
    df_print: paged
  word_document:
    reference_docx: Template.docx
    code-folding: show
    keep_md: yes
    fig.caption: yes
    toc: FALSE
    pandoc_args:
    - "--lua-filter=scholarly-metadata.lua"
    - "--lua-filter=author-info-blocks.lua"
bibliography:
- BalticPhotoperiod.bib
- packages.bib
csl: "plos-one.csl"
---









# Abstract {.unnumbered}
XXX Correct the abstract Sylwia!

Picocyanobacteria are the most abundant phytoplankters in aquatic ecosystems, and arecrucial to the optical properties of ocean water, influencing its color and transparency. We grew two PhycoCyanin(PC)-rich and two PhycoErythrin(PE)-rich strains of *Synechococcus*, under a matrix of 4 photoperiods and 6 light levels. Using high frequency measurements, we found the strains were generally opportunistic in exploiting higher light diel light doses to achieve faster growth rates, although some strains suffered photoinhibition of growth under 900 µmol photons m^−2^s^−1^ and 24 h photoperiod. Using whole-cell absorbance spectra we showed that the PE-rich strains always had a higher Photosynthetically Usable Radiation (PUR)/Photosynthetically Active Radiation (PAR) ratio than did the PC-rich strains. In general, the PUR/PAR ratio decreased with increasing light. We observed an increase in cell-specific pigment content during initial growth, followed by a sharp decrease as cells transitioned to pre-stationary phase. Our results show the PE-rich strains are stronger light harvesting competitors, but the PC-rich strains may have lower N-quotients for their light capture system. These differences may help explain differential seasonal prevalence of PE-rich and PC-rich picocyanobacteria, in terms of costs of exploitation of different photic regimes.

# Introduction {.unnumbered}

The photic regime, comprised of light level (PAR), duration (photoperiod), and spectral quality, is a pivotal influence on the growth and productivity of phytoplankton within aquatic ecosystems. In polar regions, characterized by prolonged periods of wintertime darkness and continuous daylight during summer, phytoplankton encounter unique challenges. Light is the primary limiting factor for biomass production in winter, suppressing phytoplankton growth and metabolic activity, whereas the extended daylight in summer boosts photosynthetic activity [@arrigoSeaIceEcosystems2014]. In temperate regions, seasonal variation in light-limitation is less pronounced, but phytoplankton are still influenced by daily and seasonal fluctuations. There is a clear contrast between more favorable conditions for phytoplankton growth in spring and summer, compared to fall and winter [@huismanHowSinkingPhytoplankton2002; @holtropVibrationalModesWater2021]. In the tropics, daylight remains nearly constant throughout the year [@behrenfeldClimatedrivenTrendsContemporary2006], and phytoplankton productivity is rather controlled by nutrients resupply into the euphotic zone [@hutchinsMarinePhytoplanktonChanging2016; @liPhytoplanktonResponsesNitrogen2015] and zooplankton grazing [@christakiGrowthGrazingProchlorococcus1999].

Cyanobacteria growth undergoes distinct phases, including lag phase, exponential growth phase, stationary phase, and death phase [@reynoldsEcologyPhytoplankton2006]. During the lag phase, cyanobacteria acclimate to the environment and prepare for active growth by synthesizing essential cellular components. The exponential growth phase is marked by rapid cell division and biomass accumulation, fueled by optimal environmental conditions and nutrient availability. As nutrient levels become limited, algae enter the stationary phase, characterized by a balance between cell division and death, leading to a plateau in population growth. The death phase occurs when resources are depleted, and the algae experience cell death and decomposition, contributing to nutrient recycling in aquatic ecosystems [@reynoldsEcologyPhytoplankton2006]. Cell death may also be associated with the release of toxins into the environment. Understanding the temporal progression of growth phases is essential for predicting cyanobacterial activity and their impact on ecosystem dynamics over time.

*Synechococcus*, a diverse genus of picocyanobacteria, exhibits a nearly ubiquitous distribution spanning diverse geographical regions [@flombaumPresentFutureGlobal2013], while demonstrating a remarkable range of adaptations to environmental conditions. *Synechococcus*' capacity to thrive across diverse marine and freshwater habitats positions it as a pivotal agent in energy and nutrient transfer within food webs, and serves as a link connecting the microbial loop with higher trophic levels, offering direct sustenance to grazers, including zooplankton and small fish [@liCompositionUltraphytoplanktonCentral1995]. *Synechococcus*, as one of the two dominant picocyanobacterial genera in oceanic waters, also significantly affects light attenuation and availability for other photosynthetic organisms, and influences the ocean colour, allowing for satellite detection of *Synechococcus* rich communities [@bracherObtainingPhytoplanktonDiversity2017; @xiGlobalRetrievalPhytoplankton2020]. General relations among optical absorption spectra and pigment compositions have been used to determine diagnostic pigment indices of major phytoplankton functional types [@vidussiPhytoplanktonPigmentDistribution2001; @fishwickFunctionalRelationshipsBiooptical2006; @hirataSynopticRelationshipsSurface2011]. Modeling suggests that *Synechococcus* abundance will rise due to climate warming [@flombaumPresentFutureGlobal2013]. The projected changes may vary geographically and may include shifts in the spatial distribution of the main picocyanobacteria, as well as changes in the proportions among the *Synechococcus* sp. lineages [@sixMarineSynechococcusPicocyanobacteria2021]. However, knowledge about the impact of these environmental changes on the occurrence and ecophysiology of various picocyanobacterial phenotypes is not sufficiently known.

*Synechococcus* exhibits significant phenotypic diversity across many lineages, encompassing strains rich in PhycoErythrin (PE-rich) or PhycoCyanin (PC-rich) [@haverkampColorfulMicrodiversitySynechococcus2009; @aguileraEcophysiologicalAnalysisReveals2023]. These phycobilin pigment-proteins are pivotal for light absorption during photosynthesis and confer distinctive colours to the picocyanobacteria. The disparate light preferences between PC-rich and PE-rich *Synechococcus* sp. strains influence their ecological niches. PC-rich strains thrive in environments with elevated light levels, such as surface waters and coastal regions, where blue light predominates. PE-rich strains exhibit adaptation to low-light conditions, primarily inhabiting the deeper layers of the water column where green light prevails. These differences result in PC-rich and PE-rich *Synechococcus* sp. strains predominantly occupying complementary habitats [@sixLightVariabilityIlluminates2007; @haverkampColorfulMicrodiversitySynechococcus2009; @sixMarineSynechococcusPicocyanobacteria2021].

Photic regimes and growth phases of PC-rich and PE-rich *Synechococcus* sp. may drive spatial and temporal variability of *Synechococcus* biomass and community lineage composition within aquatic environments, relating to varying metabolic costs between physiological strategies. The aim of this research was to determine whether photic regimes and growth phases affect diel growth symmetries and light-capture in PC-rich and PE-rich *Synechococcus* sp. 

# Material and Methods {.unnumbered}

## Culture condition and experimental setup {.unnumbered}

Two non-axenic PhycoCyanin(PC)-rich (CCBA_056 or CCBA_077) and two PhycoErythrin(PE)-rich (CCBA_048 or CCBA_127) strains of *Synechococcus* were obtained from Culture Collection of Baltic Algae (CCBA; https://ccba.ug.edu.pl/pages/en/home.php). Pre-cultures of picocyanobacteria strains were kept in Tissue Culture Flasks (VWR International, Cat. No. 10062-872, PA, USA) and were transferred to fresh f/2 media [@guillardCulturePhytoplanktonFeeding1975] at salinity of 8 PSU every two weeks, under a photoperiod of 12 h and Photosynthetically Active Radiation (PAR) of 10 µmol photons m^−2^s^−1^ supplied from cool white fluorescent tubes, at 22℃.

Cultures of each strain were grown in 8 x 80 mL round bottom glass tubes in a Multi-Cultivator MC 1000-OD (Photon Systems Instruments, Drásov, Czech Republic). Each culture tube contained 75 mL of f/2 medium inoculated with and 5 mL of growing pre-culture, to achieve exponential growth from the beginning of the experiment, with little to no lag phase upon inoculation. 

Cultures grew at 22℃, with photoperiods of 8, 12, 16, or 24 h, with peak Photosynthetically Active Radiation (PAR) of 30, 90, 180, 300, 600, or 900 µmol photons m^−2^s^−1^ supplied from white LED lamps independently to each culture tube. To reflect the natural movement of the sun, the photoperiods of 8-16 h were applied in the shape of a sine wave, while the 24-hour photoperiod was applied in a square shape. Since the area under a sine curve is 1/2 the area under a square of equal width, the 24 h square photoperiod cultures received 4 times the diel photon dose of the 12 h sine photoperiod cultures.
 
The cultures of picocyanobacteria were acclimatized for one day to the new conditions corresponding to the incubation conditions of the proper culture. Tubes contained Glass Aeration Tubes and were closed with a silicone inert stopper perforated by an aeration input tube extending to the bottom of the culture tube, and a pressure outlet tube. Aeration with a total air flow rate of around 1,100 mL min^−1^ distributed across 8 tubes for ~ 140 mL min^−1^ tube^−1^ ensures mixing and provides sufficient air/CO~2~ supply to cultures across the entire culture volume. Cultivation and monitoring functions (light, temperature, optical density, and aeration gas) of the Multi-Cultivator system was controlled via the Photobioreactor Control Software (Photon Systems Instruments, Drásov, Czech Republic). 

## The growth curve and chlorophyll specific exponential growth rate analysis {.unnumbered}

Picocyanobacterial growth was monitored every 5 minutes by automatically recording OD~680~, OD~720~, and ΔOD (ΔOD = OD~680~-OD~720~) for 14 days, independently for each culture tube. The exceptions were experiments conducted with a photoperiod of 24 h and light of 600 or 900 µmol photons m^−2^s^−1^, which lasted 7 days.

Based on the obtained measurements of growth we determined exponential chlorophyll specific exponential growth rate (µ) by fitting logistic growth curves to plots of the chlorophyll *a* proxy of ΔOD vs. elapsed time for each combination of strain, photoperiod, and peak PAR. We used a modified Levenberg-Marquardt fitting algorithm [@minpack.lm].

## The growth symmetry analysis {.unnumbered}

xxxx Add proper text here Sylwia!!!

Using the 5-minute time interval, the absolute growth increment (AGI) was computed, defined as the OD680 change between the consecutive measurements d(OD680)/dt. Values above 0 represent OD680 increase and growth of the picocyanobacteria cultures. Increase of the AGI curve reflects acceleration of the growth, and decrease the deceleration phase, consequently (Fig. 1).

Based on the AGI were determined the acceleration phase length (AccLen), defined as the time (expressed in h) between the start of the photoperiod and the time of the tMaxDGI. This relationship was defined as diel growth symmetry (GS; Eq. (1)).
GS(h)=AccLen/(Photoperiod length)  (1)
The maximum value within each photoperiod was called the maximum daily growth increment (maxDGI), and the highest of all of them, was recorded for each experiment setup and referred to as the maximum absolute growth increment (maxAGI). The maxAGI marked the point of the sigmoid curve fitted to the growth curve, indicating the transition point leading to the pre-stationary phase. Additionally, the total daily growth (TDG), defined as the difference in OD680 at the end and at the beginning of each photoperiod was estimated.


![<span id="fig:FirstDerivative"></span>Figure 1: **A) Example of a growth curve (tracked as OD680; red solid line) of a *Synechococcus* sp. strain vs. elapsed time (h)**. The vertical dotted lines indicate the time to reach the diel maximum of the 1st derivative of growth (vertical dotted line; tMaxDG). The vertical blue solid line represents the time when the cultures reached their maximum absolute hourly growth (tMaxAHG), taken as an index of transition from exponential to pre-stationary growth phases. **B) The 1st derivative (taken over 1 h increments) for growth vs. elapsed time.** Within a diel period the acceleration length (AccLen) is the time between the start of the photoperiod and the time to reach the diel maximum of the 1st derivative of growth (vertical dotted line; tMaxDG). Decleration length is then the time from tMaxDG to the end of the photoperiod. We then define the diel growth symmetry (GS) as AccLen/DecLen.](../Output/Figures/Fig_FirstDerivative.png)

## Determining the number of cells {.unnumbered}

The number of picocyanobacterial cells was calculated using linear regression models based on cell concentration (N mL^−1^) and OD at 680 nm. The OD of cultures was measured using a CLARIOstar Plus Plate Reader (BMG, Labtech, Ortenberg, Germany) and calculation of the cell number was conducted using the PAMAS S40 GO Particle counter (PAMAS Partikelmess- und Analysesysteme GmbH, Rutesheim, Germany). The linear correlations between N and OD~680~ for individual strains were used to estimate the number of cells based on OD measurements obtained from Multi-Cultivator system. Linear regression, coefficient of determination, Pearson correlation coefficients, and p-value was presented in Tab. S1 (Supplementary materials).

## Whole-cell absorbance spectra measurements {.unnumbered}

Absorbance measurements on intact cells in suspension were conducted in OLIS CLARiTY 17 UV/Vis/NIR with integrating cavity upgrade spectrophotometer (On-Line Instrument Systems, Inc., Bogart, GA, USA) according to the method described by [@blakeSituSpectroscopyIntact2012] with modifications. In an experiment, identical 8 mL solutions that contained f/2 medium, were added to both the sample and reference observation cavities of the spectrophotometer. After recording a baseline from 375 to 710 nm, 1 mL was withdrawn from the sample cavity and replaced with 1 mL of the cell suspension of tested picocyanobacteria. The pathlength corrected absorbance per cm was performed by determining the Javorfi coefficients [@javorfiQuantitativeSpectrophotometryUsing2006] as described in the equipment manual.

## Estimating Photosynthetically Usable Radiation (PUR) {.unnumbered}

Using whole-cell absorbance spectra of *Synechococcus* sp. cultures as described above (Fig. <a href="#fig:OlisSpectra">2</a>) we estimated Photosynthetically Usable Radiation (PUR) according to the method proposed by [@morelAvailableUsableStored1978]. Initially, we normalized the obtained whole-cell absorbances (AbsNorm~440~) and emission spectra of the white LED lamps (EmNorm~440~) to a reference wavelength of 440 nm. The PUR value, which is the ratio of the normalized sum of absorbance and emission spectra to the sum of normalized emission spectra multiplied by the intensity of the tested light (PAR) was calculated (Eq. (1)).

$$\begin{equation}
  PUR=PAR\frac{sum(AbsNorm_440*EmNorm_440)}{sum(EmNorm_440)}
  \qquad(1)
\end{equation}$$


![<span id="fig:OlisSpectra"></span>Figure 2: **Whole-cell absorbance spectra of PC-rich (solid green lines) or PE-rich (dashed red lines) cultures of *Synechococcus* sp.** Representative absorbance spectra, normalized A~440nm~, were measured from the exponential or pre-stationary phases of growth, together with emission spectra of the white LED lampused for culture growth (Photosynthetically Active Radiation (PAR), normalized to emission at 440 nm (light gray area), in this example 300 µmol photons m^−2^s^−1^). Estimated Photosynthetically Usable Radiation (PUR) is shown as a green area for the PC-rich strain and a red area for the PE-rich strain, with total PUR given for each culture (µE = µmol photons m^−2^s^−1^). Peaks characteristic of known pigments are labelled; Chl *a*, chlorophyll *a*; PC, phycocyanin; PEB-rich PE, phycoerythin-rich phycoerythrin; PUB-rich PE, phycourobilin-rich phycoerythrin, Car, carotenoids.](../Output/Figures/Fig_OlisSpectra.png)

## Pigment content analysis {.unnumbered}

The pigment content: chlorophyll *a* (Chl *a*), carotenoids (Car), phycoerythrin (PE), phycocyanin (PC), and allophycocyanin (APC) in *Synechococcus* sp. cultures over time was estimated with previously determined linear correlations between pigment content obtained by extraction technique and absorbance values of individual pigment peaks (nm) obtained from the whole-cell absorbance spectra. Linear regression, coefficient of determination, Pearson correlation coefficients, and p-value was presented in Tab. S2 (Supplementary materials). Total amount of phycobilin pigments (Total Phyco) for individual strains was obtained by adding the content of PE, PC, and APC.

Pigments extraction were performed using formula from [@stricklandPracticalHandBook1972] for Ch *a* and Car concentrations. PE, PC, and APC were calculated based on [@bennettCOMPLEMENTARYCHROMATICADAPTATION1973]. The extracts contained photosynthetic pigments were measured using a CLARIOstar Plus Plate Reader (BMG, Labtech, Ortenberg, Germany), at wavelengths of 480, 665, and 750 nm for Chl *a* and Car calculation and at 565, 620, 650, and 750 nm for PE, PC, and APC. The values of individual pigment peaks (nm) from the whole-cell absorbance spectra were obtained by Olis-modernized Cary 14 UV/Vis/NIR with Integrating Sphere upgrade spectrophotometer (On-Line Instrument Systems, Inc., Bogart, GA, USA). For the linear model, the following wavelengths were analyzed: 480 (Car), 565 (PE), 620 (PC), 650 (APC), and 665 (Chl *a*) nm.

## Estimating cumulative diel PAR {.unnumbered}

Based on the length and shape of the photoperiod (sine wave for photoperiod of 8-16 h; square for photoperiod of 24 h) and the given light level, we estimated the value of the cumulative diel PAR. For a photoperiod arranged in the shape of a sine wave we used Eq. (2). For a continuous 24 h photoperiod we used Eq. (3).

$$\begin{equation}
\begin{split}
  Cumulative~diel~PAR~(µmol~photons~m^{−2}~d^{−1})= \\ \frac{PAR~(µmol~photons~m^{−2}~s^{−1})*60~(s~min^{−1})*60~(min~h^{−1})*photoperiod~(h~d^{−1})}{2}
  \qquad(2)
\end{split}
\end{equation}$$

$$\begin{equation}
\begin{split}
  Cumulative~diel~PAR~(µmol~photons~m^{−2}~d^{−1})= \\ PAR~(µmol~photons~m^{−2}~s^{−1})*60~(s~min^{−1})*60~(min~h^{−1})*photoperiod~(h~d^{−1})
  \qquad(3)
\end{split}
\end{equation}$$

## Changes effective absorption cross section of PSII and PSII flux per unit volume {.unnumbered}
xxx I really need Doug help here!

Kolber, Z., Klimov, D., Ananyev, G., Rascher, U., Berry, J., & Osmond, B. (2005). Measuring photosynthetic parameters at a distance: laser induced fluorescence transient (LIFT) method for remote measurements of photosynthesis in terrestrial vegetation. Photosynthesis research, 84, 121-129.

Oxborough, K., Moore, C. M., Suggett, D. J., Lawson, T., Chan, H. G., & Geider, R. J. (2012). Direct estimation of functional PSII reaction center concentration and PSII electron flux on a volume basis: a new approach to the analysis of Fast Repetition Rate fluorometry (FRRf) data. Limnology and Oceanography: Methods, 10(3), 142-154.

Keller, B., Vass, I., Matsubara, S., Paul, K., Jedmowski, C., Pieruschka, R., ... & Muller, O. (2019). Maximum fluorescence and electron transport kinetics determined by light-induced fluorescence transients (LIFT) for photosynthesis phenotyping. Photosynthesis Research, 140, 221-233.

Calculation of the absorption cross section of PSII photochemistry (\u03C3~PSII~'; nm^2^ quanta^-1^) under ambient light through an iterative curve fit to the saturation phase of an Fast Repetition Rate fluorometry (FRRf) single turnover (ST) measurement of tested picocyanobacteria were obtained using SoliSense laser-induced fluorescence transient (LIFT) fluorometer equipped with a prototype temperature control unit (LIFT-REM, Soliense Inc., New York, USA). PSII flux per unit volume (JV~PSII~; xxxx add proper unit) was calculated according to the method proposed by [Campbell?; Oxborough et al., 2012]. 

PC-rich and PE-rich picocyanobacteria were measured under diel peak PAR growth light under a blue LED (Ex 445 nm) and orange (Ex 590 nm) excitation. Excitation protocols were used to manipulate the level of photosynthetic activity and chlorophyll fluorescence (ChlF). Flash Power for blue excitation was 60000 and for orange excitation was 14000 µmol photons m^−2^s^−1^. The intensity of the blue and orange LIFT LED in DC mode and excitation power were calibrated using a quantum sensor (LI-250, LI-COR, Inc.). Data were collected during an rapid light curve (RLC) sequence during which light intensity was increased from 0 to 320 µmol photons m^−2^s^−1^ and then decreased from 320 to 0 µmol photons m^−2^s^−1^ with a 1-s pause in darkness between measurements. Acquisitions were made at 10-s intervals. [Campbell and Kolber?; Kolber et al., 2005; Oxborough et al., 2012].

## Statistical analysis {.unnumbered}

All analysis of obtained results was conducted using R version 4.3.0 [@rcoreteamLanguageEnvironmentStatistical2019] running under RStudio [@teamrstudio.RStudioIntegratedDevelopment2015]. To determine significant differences in studied experiments the “stats” v. 3.6.2 R standard packages were used. This package provides basic statistical functions, including the *lm()* function for linear regression, *aov()* function for ANOVA, and *t.test()* function for t-test. 

Linear regression, coefficient of determination (R square), Pearson correlation coefficients (R), and p-value was used to calculate the number of cells (N mL^−1^) and  pigment content (µg mL^-1^) for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. 

We performed three-way factorial ANOVA of chlorophyll specific exponential growth rate, estimated from logistic fits of chlorophyll proxy OD~680~-OD~720~, index of diel growth symmetry, PUR/PAR ratio, total Phyco/Chl *a* ratio, and effective absorption cross section of PSII (\u03C3~PSII~'; nm^2^ quanta^-1^) measured under diel peak PAR growth light under Ex445 nm (blue) or under Ex590 nm (orange) excitation in relation to the cumulative diel photon dose (µmol photons m^−2^d^−1^) or in relation to the total Phyco/Chl *a* ratio.

To examine statistical differences between models, we performed one-way ANOVA of a three parameter model (Harrison and Platt, 1986) from pooled data and data fit across different photoperiods (8, 12, 16, or 24) or data fit across different peak PAR (30, 90, 180, 300, 600 together with 900) from chlorophyll specific exponential growth rate, for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea, grown at 30, 90, 180, 300, 600, or 900 peak PAR µmol photons m^−2^s^−1^; and photoperiods of 8, 12, 16, or 24 h. 

One-way ANOVA was also used to examine statistical differences between single phase exponential decay fit model of pooled data across different strains for a given phase of growth and across different phase of growth for a given strain from index of diel growth symmetry; (AccLen/DecLen ratio), PUR/PAR ratio, total Phyco/Chl *a* ratio, and effective absorption cross section of PSII (\u03C3~PSII~'; nm^2^ quanta^-1^) measured under diel peak PAR growth light under Ex590 nm (orange) excitation in relation to the cumulative diel photon dose (µmol photons m^−2^d^−1^).

T-test of linear fit model of pooled data across different strains for a given phase of growth and across different phase of growth for a given strain from effective absorption cross section of PSII (\u03C3~PSII~'; nm^2^ quanta^-1^) measured under diel peak PAR growth light under Ex445 nm (blue) excitation in relation to the cumulative diel photon dose (µmol photons m^−2^d^−1^) or in relation to the total Phyco/Chl *a* ratio, as well as from effective absorption cross section of PSII (\u03C3~PSII~'; nm^2^ quanta^-1^) measured under diel peak PAR growth light under Ex590 nm (orange) excitation in relation to the total Phyco/Chl *a* ratio was performed.

The *SSasymp()* function (Self-Starting Nls Asymptotic Regression Model) was used to perform a single phase exponential decay fit model. A modified Levenberg-Marquardt fitting algorithm [@minpack.lm] was used for estimating logistic fits of chlorophyll proxy OD~680~-OD~720~ vs. elapsed time for each combination of strain, photoperiod, and peak PAR. The trends of change in the growth symmetry (GS) were tested using the Mann-Kendall test [@toutenburgHollanderWolfeNonparametric1975] on the ±5 photoperiods to avoid noise during the first few days of the experiment. Statistical differences for all analyzes were determined at the level of significance \u03B1 = 0.05. 

Manuscript was prepared as Rmarkdown document [@handelAndreasHandelCustom2020]. Figures were plotted using “ggplot” [@wickhamDataAnalysis2016] R package.


# Results {.unnumbered}

## Changes in chlorophyll specific exponential growth rate {.unnumbered}

Research Question:
Does cumulative diel photon dose consistently explain achieved growth rates across a matrix of photoperiods and peak PAR?

Test:  Do strains show distinct growth responses to cumulative diel photon dose, depending upon photoperiod?
  Yes.  Every strain shows photoperiod-specific responses to cumulative diel photon dose that differ from a single light response model fit to the pooled data from a strain.
  

Test:  Do strains show distinct growth responses to cumulative diel photon dose, depending upon peak PAR?
  Yes.  In supplmental data, strains generally show peak-PAR specific responses to cumulative diel photon dose, that differ from a single light response model fit to the pooled data from a strain. Exceptions are that for strains 77 and 48 peak PAR of 600 or 900 µmol photons m^−2^d^−1^ are not significantly different from the pooled data model.  A caveat to this findings is that cumulative diel photon dose is, of course, a product of photoperiod and PAR, so the highest levels of cumulative photon dose are only achieved under the 600 or 900 µmol photons m^−2^d^−1^.
  
All four strains show saturation of growth rate under increasing cumulative diel PAR, but the achieved estimates of µ~max~ vary depending upon photoperiod and peak diel PAR.  Plots of growth rates vs. cumulative diel PUR, estimated for exponential phase cultures, show similar patterns (Supplemental).

![<span id="fig:GrowthRatePhotoperiod"></span>Figure 3: **Chlorophyll specific exponential growth rates (d^−1^) vs. cumulative diel photon dose (µmol photons m^−2^d^−1^).** Growth rates (+/- SE falling within symbols) were estimated from logistic fits of chlorophyll proxy OD~680~-OD~720~ vs. elapsed time (Fig. S4), for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), 600 (orange), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), 16 (triangle), or 24 (diamond) h. Solid blue line shows a fit of the pooled growth rates for each strain, with a three parameter model (Harrison and Platt, 1986). We also fit the same model separately for 8 (dotted line), 12 (long dash line), 16 (dashed line), or 24 (two dash line) h photoperiods, since for all strains they were significantly different (ANOVA, *p* < 0.05) from the fit of pooled data.](../Output/Figures/Fig_GrowthRate_Photoperiod.png)

## Changes of diel growth symmetry {.unnumbered}
Supplemental figures show consistent variations in short term growth rates over diel cycles.  We sought to analyze the intra-diel patterns of growth, initially by separating growth over the photoperiod into an acclerating phase of increasing hourly growth increments, and a deceleration phase, of decreasing hourly growth increments.

Research Question:
Do strains show consistent patterns of diel growth across cumulative diel photon doses?

No.
The length of the diel acceleration phase of growth increases with increasing photoperiod, but the slope of accleration phase vs. cumulative diel photon dose decreases with increasing peak PAR. 

During pre-stationary phase these responses dampen but persist.

![<span id="fig:AccLen"></span>Figure 4: **Hours of photoperiod to reach maximum hourly growth vs. cumulative diel photon dose (µmol photons m^−2^d^−1^).** Time-resolved growth was estimated over hourly intervals for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), or 16 (triangle) h. The horizontal lines indicate the time (h) to reach the maximum light for a given photoperiod; 4 h for the 8 h photoperiod; 6 h for the 12 h photoperiod; or 8 h for the 16 h photoperiod. Figure presents data (small symbols) and means (big symbols) from exponential phase of growth, or from pre-stationary phase of growth, *n* = 1-5.](../Output/Figures/Fig_AccLen.png)

Research Question:
Do strains show consistent patterns of diel symmetry (AccLen/DecLen) across cumulative diel photon doses?

Yes.
The ratio of the diel acceleration phase of growth to the deceleration phase shows a consistent exponential decay in relation to cumulative photon dose, across different combinations of photoperiod and peak PAR.
Although all strains shows this response pattern, the exponential decay model parameters differ significantly among strains.
During pre-stationary phase this response dampens and even disappears. 

![<span id="fig:GS"></span>Figure 5: **Index of diel growth symmetry (AccLen/DecLen ratio) vs. cumulative diel photon dose (µmol photons m^−2^d^−1^).** Diel growth symmetry was estimated for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), or 16 (triangle) h. Figure presents data (small symbols) and means (big symbols) from exponential phase of growth, or from pre-stationary phase of growth, *n* = 1-5. Blue solid line shows single phase exponential decay fit for data from each strain and growth phase, with fit parameters presented. Different lowercase letters indicate significant differences between the fit models for different strains within a given phase of growth. Different uppercase letters indicate significant differences between the fit models for different phases of growth within a given strain (ANOVA; *p* < 0.05).](../Output/Figures/Fig_GS.png)

## Changes of PUR/PAR ratio {.unnumbered}

Research Question:
Do strains show consistent patterns of light capture efficacy (PUR/PAR ratio) across cumulative diel photon doses?

Yes.
The ratio of PUR/PAR shows a consistent exponential decay in relation to cumulative photon dose, across different combinations of photoperiod and peak PAR.
Although all strains shows this response pattern, the exponential decay model parameters differ significantly among strains.
During pre-stationary phase this response dampens and even disappears. 
The PE-rich strains show a much higher PUR/PAR ratio under low cumulative diel photon dose, but decay towards a plateau close to the PC-rich strains as cumulative diel photon dose increases.

![<span id="fig:PURPARRatio"></span>Figure 6: **Changes of PUR/PAR ratio vs. cumulative diel photon dose (µmol photons m^−2^d^−1^).** PUR/PAR ratio was estimated for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), 600 (orange), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), 16 (triangle), or 24 (diamond) h. Figure presents data (small symbols) and means (big symbols) from exponential phase of growth, or from pre-stationary phase of growth. Blue solid line shows single phase exponential decay fit for data from each strain and growth phase, with fit parameters presented. Different lowercase letters indicate significant differences between the fit models for different strains within a given phase of growth. Different uppercase letters indicate significant differences between the fit models for different phases of growth within a given strain (ANOVA; *p* < 0.05).](../Output/Figures/Fig_PURPARRatio.png)

## Changes effective absorption cross section of PSII {.unnumbered}

Research Question:
Do strains show consistent patterns of effective absorption cross section for PSII photochemistry across cumulative diel photon doses?

Yes.
The \u03C3~PSII~' shows a consistent, sharp exponential decay in relation to cumulative photon dose, across different combinations of photoperiod and peak PAR.
Although all strains shows this response pattern, the exponential decay model parameters differ significantly among strains.
During pre-stationary phase this response dampens but persists. 
The PE-rich strains show a much higher \u03C3~PSII~' under low cumulative diel photon dose, and remain higher than the PC-rich strains even as cumulative diel photon dose increases.


![<span id="fig:Sigma590"></span>Figure 7: **Effective absorption cross section of PSII** (σ~PSII~'; nm^2^ quanta^-1^) **measured under diel peak PAR growth light  vs. cumulative diel photon dose (µmol photons m^−2^d^−1^).** Effective absorption cross section of PSII (σ~PSII~'; nm^2^ quanta^-1^) was estimated using FRRf induction curves with excitation of phycobilisomes using Ex~590nm~ (orange) excitation, for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), 600 (orange), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), 16 (triangle), or 24 (diamond) h. Figure presents data (small symbols) and means (big symbols) from exponential phase of growth, or from pre-stationary phase of growth. Blue solid line shows single phase exponential decay fit for data from each strain and growth phase. Different lowercase letters indicate significant differences between the fit models for different strains within a given phase of growth. Different uppercase letters indicate significant differences between the fit models for different phases of growth within a given strain (T-test; *p* < 0.05).](../Output/Figures/Fig_Sigma590.png)

Research Question:
Does \u03C3~PSII~' show a consistent relation to phycobilisome:chlorophyll ratio?
The \u03C3~PSII~' excited through chlorophyll absorbance at 445 nm was consistently small across strains and growth conditions, since in cyanobacteria the number of chlorophyll serving PSII is nearly fixed (CITATIONS DOUG). For \u03C3~PSII~' excited through phycobilisome absorbance at 590 nm, strains show consistent positive correlation with phycobilin:chlorophyll ratio.  Strains in exponential growth show significant scatter around this positive relation, likely related to regulatory control of \u03C3~PSII~', beyond pigment composition. Under pre-stationary phase the plots of \u03C3~PSII~' vs. phycobilin:chlorophyll show much less scatter, suggesting an increase in reliance upon compositional regulation to control light delivery to PSII, as opposed to shorter term regulation.

The linear fits also vary significantly among strains.


![<span id="fig:SigmaPig590"></span>Figure 8: **Changes of effective absorption cross section of PSII** (σ~PSII~'; nm^2^ quanta^-1^) **measured under diel peak PAR growth light under Ex590 nm (orange) excitation vs. total Phyco/Chl *a* ratio.** Effective absorption cross section of PSII (σ~PSII~'; nm^2^ quanta^-1^) was estimated for two PhycoCyanin(PC)-rich cultures (056, 077) and two PhycoErythrin(PE)-rich cultures (048, 127) of *Synechococcus* sp. originating from the Baltic Sea. Cultures were grown at 30 (dark gray), 90 (light gray), 180 (purple), 300 (red), 600 (orange), or 900 (yellow) peak PAR µmol photons m^−2^s^−1^ (µE); and photoperiods of 8 (square), 12 (circle), 16 (triangle), or 24 (diamond) h. Figure presents data (small symbols) and means (big symbols) from exponential phase of growth, or from pre-stationary phase of growth. Blue solid line shows linear model fit for data from each strain and growth phase. Different lowercase letters indicate significant differences between the fit models for different strains within a given phase of growth. Different uppercase letters indicate significant differences between the fit models for different phases of growth within a given strain (t-test; *p* < 0.05).](../Output/Figures/Fig_SigmaPig590.png)

# Discussion {.unnumbered}

## The role of photoperiod for picocyanobacteria growth in aquatic ecosystems {.unnumbered}

In this work, we have shown that not only the daily dose of light, but also the length of exposure affected the picocyanobacteria growth rate. The PE-rich and PC-rich strains of *Synechococcus* sp. showed faster logistic growth rates with increasing photoperiod, including constant light conditions. Most of the strains were able to survive even under dose of light of 77,760,000 µmol photons m^−2^ per day. In addition, one of PC-rich strains showed the fastest growth rate in these extreme conditions.

Phytoplankton are highly sensitive to changes in photoperiod, which serves as a key environmental cue for their metabolic activities and life cycle events [@huismanHowSinkingPhytoplankton2002; @alberteFunctionalOrganisationPhotosynthetic1980; @larochePelagicLightDependentMicrobiome2022]. The duration of light exposure within a day regulates various physiological processes, including photosynthesis, growth, reproduction, and nutrient assimilation in phytoplankton. Changes in photoperiod trigger adaptive responses, shaping the temporal dynamics and community structure of phytoplankton. 

Here, we confirmed that *Synechococcus* sp. can exist and even become the dominant faction of phytoplankton in all geographic zones on Earth as long as they have access to light. In regions with a longer photoperiod (summer in the temperate zone and summer at the poles), PC-strains may become dominant species in the surface waters whereas some of PC-strains of *Synechococcus* sp. may be less numerous than PE-strains in surface waters (where the light intensity could be extremely high) when the photoperiod is quite low (autumn and winter in temperate zones and tropical water throughout the year). Our research has also highlighted the possibility of occurrence of both PE-rich and PC-rich *Synechococcus* sp. in conditions of continuous irradiation. Thus, it can be predicted that *Synechococcus* may become the dominant fraction of phytoplankton during the Arctic summer near the poles regions regardless of their genetic lineages and pigments composition.

## The importance of Photosynthetically Active Radiation (PAR) for picocyanobacteria growth {.unnumbered}

Photosynthetically Active Radiation (PAR) refers to the spectral range of solar radiation (approximately 400-700 nm) that is capable of driving photosynthesis [@morelAvailableUsableStored1978]. Light intensity, a measure of the amount of PAR reaching a specific area, directly affects the physiology of picocyanobacteria [@aguileraEcophysiologicalAnalysisReveals2023; @sliwinska-wilczewskaPhotosyntheticPigmentsChanges2020; @sliwinska-wilczewskaEcophysiologicalCharacteristicsRed2018]. Optimal light intensity levels provide the necessary energy for efficient photosynthesis, promoting phytoplankton growth, reproduction, and biomass production. The availability and distribution of PAR and light intensity in aquatic ecosystems are influenced by cloud cover, water depth, and light attenuation due to water turbidity and suspended particles [@kirkLightPhotosynthesisAquatic1983; @fieldPrimaryProductionBiosphere1998; @torremorellAnnualPatternsPhytoplankton2009]. *Synechococcus* sp., a widely studied picocyanobacterial genus, exhibits remarkable adaptability to different light intensities, particularly under white light conditions. White light encompasses the entire visible spectrum, and *Synechococcus* sp. has developed various strategies to optimize its photosynthetic efficiency across a range of light intensities. Under high-light conditions, *Synechococcus* employs photoprotective mechanisms to prevent the harmful effects of excess light energy. These include the dissipation of excess energy as heat via non-photochemical quenching (NPQ) and the regulation of antenna pigments, such as phycobilisomes, to balance light absorption and energy transfer. In contrast, under low-light conditions, *Synechococcus* sp. increases the expression of light-harvesting complexes to enhance light absorption and capture [@chenGenomicTranscriptomicEvidence2022; @dufresneUnravelingGenomicMosaic2008; @mella-floresProchlorococcusSynechococcusHave2012]. In our work, the PE-rich and PC-rich *Synechococcus* sp. strains showed faster logistic growth rates with increasing light, although some strains suffered photoinhibition. The *Synechococcus* sp. strains reach their plateau in the light intensity range of 180-300 µmol photons m^−2^s^−1^. Growth at 900 µmol photons m^−2^s^−1^ was also noted but not as efficient as under moderate light. The exception was one PC-rich strain, which under this condition reached the maximum growth rate.

Numerous studies have highlighted the significance of PAR and light intensity as a key driver of phytoplankton productivity and its influence on ecosystem dynamics, biogeochemical cycling, and food web interactions [e.g., @kirkLightPhotosynthesisAquatic1983; @fieldPrimaryProductionBiosphere1998; @torremorellAnnualPatternsPhytoplankton2009; @churilovaPhytoplanktonBloomPhotosynthetically2020]. Our research shows that an increase in light intensity can result in the dominance of both PE-rich and PC-rich picocyanobacteria in aquatic ecosystems and confirmed the possibility of occurrence of *Synechococcus* sp. in extremely high irradiance conditions.

## The importance of Photosynthetically Usable Radiation (PUR) for picocyanobacteria growth {.unnumbered}

Photosynthetically Usable Radiation (PUR) is the fraction of radiant energy (Photosynthetically Active Radiation; PAR) of such wavelength that it can be absorbed by the cyanobacteria and algae. Thus, PUR is always smaller than PAR (PUR < PAR) and depends on the spectral composition of the submarine radiant energy available to algae and their pigment composition determining the spectral absorption properties [@morelAvailableUsableStored1978]. In this study, the PE-rich strains always had a higher PUR/PAR ratio than the PC-rich strains. The PUR/PAR ratio decreased with increasing light in the PE-rich strains, while it initially increased under low light and short photoperiod in the PC-rich strains.

PUR plays a fundamental role in the growth and productivity of phytoplankton within aquatic ecosystems [@behrenfeldClimatedrivenTrendsContemporary2006; @falkowskiGlobalCarbonCycle2000; @morelOpticalModelingUpper1988]. Phytoplankton, as primary producers, heavily rely on PUR for their energy acquisition through photosynthesis. The availability of PUR directly influences the photosynthetic rates and overall metabolic activity of phytoplankton. High levels of PUR promote optimal photosynthetic efficiency, leading to enhanced growth, reproduction, and biomass accumulation. Conversely, insufficient or suboptimal PUR availability can limit the metabolic processes and growth of phytoplankton. The spatial and temporal distribution of PUR within aquatic ecosystems is influenced by various factors, including solar zenith angle, water depth, water clarity, and the presence of light-absorbing substances such as dissolved organic matter [@morelAvailableUsableStored1978; @morelOpticalModelingUpper1988]. Understanding the dynamics and availability of PUR is crucial for comprehending the variability of picocyanobacteria communities in different aquatic environments. As we face ongoing environmental changes, including alterations in light regimes due to climate change and human activities, assessing the impact of changing PUR on picocyanobacteria communities becomes increasingly important for predicting and managing the response of aquatic ecosystems. Our results indicate that PE-rich strains of *Synechococcus* sp., due to their high content of phycoerythrin, can better use the available radiation. Therefore, their long-term dominance in the environment can be postulated, especially in places where access to light is limited.

## The changes in pigment content of picocyanobacteria {.unnumbered}

Temporal variations in cell-specific pigment content of *Synechococcus* sp. were observed during the growth phase, characterized by an initial increase followed by a sharp decrease. These trends exhibited dependency on growth, light intensity, and photoperiod, manifesting subsequent to the attainment of daily maximum absolute growth. Maximum pigment content was documented under conditions of low irradiance and extended photoperiod. Moreover, PC-rich strains had more pigments in the cell compared to PE-rich strains of *Synechococcus* sp.

Pigment dynamics are profoundly influenced by the prevailing light regimes. Primary photosynthetic pigments in *Synechococcus* sp. comprise chlorophyll *a*, responsible for light energy capture. Under low-light conditions, picocyanobacteria tend to increase their chlorophyll *a* content to enhance light absorption and maximize energy capture for photosynthesis. Conversely, high-light conditions often lead to a decrease in chlorophyll *a* content, serving as a photoprotective mechanism against excessive irradiation. In addition to chlorophyll *a*, picocyanobacteria utilize phycobilins, including phycocyanin and phycoerythrin, as accessory pigments to enhance light harvesting efficiency. Adapting to low-light environments, picocyanobacteria enhance phycobilin production to compensate for limited irradiance, thereby optimizing their photosynthetic capabilities. The chlorophyll/phycobilin ratio serves as a valuable indicator of the prevailing light conditions and the balance between chlorophyll-based and phycobilin-based light harvesting strategies. Elevated light intensities result in a decreased chlorophyll/phycobilin ratio as picocyanobacteria allocate resources towards efficient phycobilin-mediated light capture. These intricate changes in pigment composition and ratios represent vital adaptations that enable picocyanobacteria to optimize photosynthetic efficiency and thrive in dynamic light environments [@chakdarCyanobacterialPhycobilinsProduction2016; @stadnichukCyanobacterialPhycobilisomesPhycobiliproteins2015; @bealeBiosynthesisCyanobacterialTetrapyrrole1994].

# Conclusion {.unnumbered}

Understanding the influence of light intensity and photoperiod on the dynamics of picocyanobacteria is imperative for predicting their spatial distribution across various geographic regions and their response to observed environmental changes. Our findings have substantiated that *Synechococcus* sp., irrespective of its genetic lineages and pigment composition, can thrive and even dominate the phytoplankton community worldwide when exposed to sufficient light. Furthermore, our investigations have demonstrated the survival capacity of both PE-rich and PC-rich *Synechococcus* sp. strains under conditions of exceptionally high and continuous irradiation. Consequently, it can be predicted that *Synechococcus* sp. has the potential to emerge as the prevailing phytoplankton component during the Arctic summer near polar regions. Nevertheless, our results showed the PE-rich strains are stronger light-harvesting competitors as they tend to live deeper in the water column, but the PC-rich strains may have lower N-quotients for their light capture system. Additionally, we anticipate that PC-rich strains of *Synechococcus* sp. could be less abundant than PE-rich strains in surface waters, where light intensity tends to be extremely high, especially during periods of reduced photoperiod, such as autumn and winter in temperate zones and throughout the year in tropical waters. Conversely, in regions characterized by an extended photoperiod i.e., summer in the temperate zone and summer at the poles, PC-rich strains may assume dominance in surface waters. These differences may help explain differential seasonal prevalences of *Synechococcus* sp., in terms of the costs of exploitation of different photic regimes.

# References {.unnumbered}
