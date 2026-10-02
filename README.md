# README — Ecological effects of dumping massive amounts of Sargassum in Caribbean beach and forest sites

## DATASET OVERVIEW

This repository contains data and R code associated with the study:

"Ecological effects of dumping massive amounts of the nuisance seaweed, Sargassum, in Caribbean beach and forest sites"

Authors:
Ricardo DeSantiago
Rosa E. Rodríguez-Martínez
David Lipson
Andrew Alvarez
Jeremy D. Long

Study system:
Puerto Morelos, Quintana Roo, Mexico

Study period:
August 2022 – August 2023

The study experimentally examined the ecological effects of adding large quantities of pelagic Sargassum to two terrestrial habitats commonly used as Sargassum dumping sites: beach habitat and tropical semi-evergreen forest.

The experiment crossed habitat (Beach, Forest) with Sargassum treatment (Sargassum Addition, Control). Five paired plots were established at each habitat. Sargassum addition plots received large piles of approximately 4 m3 of Sargassum, while paired control plots were left unmanipulated.

The study monitored decomposition, soil nutrients, soil respiration, plant communities, and arthropod communities over approximately one year.




## IMPORTANT DATA-PROVENANCE NOTES
<a href="https://handle.test.datacite.org/10.5072/zenodo.612805"><img src="https://sandbox.zenodo.org/badge/447768452.svg" alt="DOI"></a>


GitHub repository referenced in the manuscript:
https://github.com/ricdesantiago/Sargasso_Subsidy

SHARING/ACCESS INFORMATION

Licenses/restrictions placed on the data: No restrictions

Links to publications that cite or use the data: --

Links to other publicly accessible locations of the data: --

Links/relationships to ancillary data sets: --

Was data derived from another source? No.
If yes, list source(s): 

Recommended citation for this dataset: DeSantiago,R. 2026. Sargasso_Subsidy. https://github.com/ricdesantiago/Sargasso_Subsidy.git

Additional related data collected that was not included in the current data package: 
Soil_Chemicals2.csv



## STUDY DESIGN

Location:
Puerto Morelos, Quintana Roo, Mexico

Beach site:
A beach/dune transition site near 20.99343° N, 86.82442° W. On beach in front of Moon Palace Resort property.

Forest site:
A forest clearing/perimeter within Jardín Botánico ECOSUR "Dr. Alfredo Barrera Marín," approximately 20.84400° N, 86.90278° W.

The forest site had no known history of receiving dumped Sargassum. The beach and forest sites were selected to represent habitats in the region that are used for Sargassum disposal.

Experimental factors:

Habitat:

* Beach
* Forest

Treatment:

* Sargassum addition
* Control

Replication:

* 5 paired plots per habitat
* One Sargassum-addition plot and one unmanipulated control plot per pair

Plot spacing:

* Paired plot centers were separated by approximately 9 m.

Sargassum additions:

* Large piles were constructed in August 2022.
* Initial piles were approximately 4 m3.
* Mean initial volume was approximately 5.25 m3 at the beach and 3.31 m3 at the forest.
* Sargassum was collected from drift material accumulated at offshore barriers.
* The material consisted of a mixture of Sargassum fluitans and Sargassum natans.

Sampling periods:

* Trip 1 = August 2022
* Trip 2 = November 2022
* Trip 3 = March 2023
* Trip 4 = August 2023




## DATA FILES

File List: 
Sargassum_piles.csv < volumetric estimates for sargassum piles on beach and forest sites>
mesh_bag_inverts.csv < invertebrate counts of small and large mesh bags. This file is the invertebrate data taken directly from "mesh_bag_exp.csv">
mesh_bag_exp.csv < sargassum weights from start to finish of small and large mesh bags, also includes invertebrate counts although those were analyzed using a "mesh_bag_inverts.csv">
interior_survey.csv < plant percent cover of quadrats within the interior of sargassum piles and controls>
interior_graphs.csv <effect sizes of percent cover in interior of sargassum piles, utilizes data (Cohen's d effect sizes) calculated using "interior_survey.csv" file>
perimeter_survey.csv <plant percent cover of quadrats on the exterior perimeter of sargassum piles and controls>
perimeter_graphs.csv <effect sizes of percent cover in exterior perimeter of sargassum piles and controls, utilizes data (Cohen's d effect sizes) calculated using "perimeter_survey.csv" file>
ladder.csv <plant percent cover of quadrats on the exterior perimeter (two sides) sargassum piles and controls, and at two distances away from the pile>
Pitfalls.csv < invertebrate counts of pitfall traps installed in sargassum piles and controls>
pitfalls_effsize.csv <effect sizes of invertebrate counts calculated from data contained within "Pitfalls.csv" file>
stickies.csv <invertebrate counts of sticky traps installed over sargassum piles and controls>
sticky_effsize.csv <effect sizes of invertebrate counts calculated from data contained within "stickies.csv" file>
Soil_Chemicals2.csv <soil chemistry (Nitrate, Nitrite, pH, KH) obtained from soil samples obtained from below sargassum piles and controls. These data were obtained for reference using liquid extractions and litmus test strips; they remain part of the dataset but were not utilized beyond helping us understand any obvious patterns in the field>
sargasso_nitrates.csv <soil chemistry (Ammonium, Nitrate, Dissolved Organic Carbon) data obtained from soil samples and analyzed at SDSU by the Lipson Laboratory>
gas_readings.csv <soil respiration data obtained from gas chamber sampling and analyzed at SDSU by the Lipson Laboratory>



## FILE DESCRIPTIONS

Sargassum_piles.csv

```

Purpose:
Measurements of the volume/decomposition of the large experimental Sargassum piles.

Used to:
- Quantify change in pile volume through time.
- Compare decomposition between Beach and Forest habitats.
- Generate pile-volume figures.

Variables identified from the analysis code include:
- Treatment
- Trip
- Block
- Location
- ellipsoid_vol
- Ellipsoid_prc_D

Interpretation:
"Ellipsoid_prc_D" represents pile volume expressed as a percentage of the initial volume. Initial pile volume is therefore represented as 100%.

Pile volume was calculated from pile dimensions using the volume equation for an elliptic cone:

V = (1/3) * pi * a * b * h

where:
a = semi-major axis of pile footprint
b = semi-minor axis of pile footprint
h = pile height


# DATA DICTIONARY

The following data dictionary describes the variables contained in the CSV files associated with this study. Variable definitions are based on the field methods, manuscript, and R analysis code. Variables are identified as measured (field-collected) or derived (calculated from other variables). Units and definitions are provided where they could be established from the study materials.

## Sargassum_piles.csv

This file contains measurements of Sargassum pile dimensions and calculated pile volumes collected throughout the experiment. Sargassum pile volume was used to quantify changes in pile size over the course of the experiment.

| Variable           | Description                                                  | Type           | Units / Format        | Variable status |
| ------------------ | ------------------------------------------------------------ | -------------- | --------------------- | --------------- |
| `Date`             | Date on which pile measurements were collected               | Date/character | M/D/YY                | Measured        |
| `Trip`             | Sampling trip number                                         | Integer        | 1–4                   | Measured        |
| `Location`         | Experimental habitat/site                                    | Categorical    | Forest or Beach       | Measured        |
| `Treatment`        | Experimental treatment                                       | Categorical    | Control or Sargassum  | Measured        |
| `Block`            | Experimental block identifier                                | Integer        | —                     | Measured        |
| `Height`           | Height of Sargassum pile                                     | Numeric        | M                     | Measured        |
| `D1`               | First measured horizontal dimension of the Sargassum pile    | Numeric        | M                     | Measured        |
| `D2`               | Second measured horizontal dimension of the Sargassum pile   | Numeric        | M                     | Measured        |
| `Diameter`         | Diameter calculated from pile measurements                   | Numeric        | M                     | Measured        |
| `r`                | Radius calculated from pile dimensions                       | Numeric        | M                     | Measured        |
| `ellipsoid_vol`    | Calculated volume of the Sargassum pile                      | Numeric        | m³                    | Derived         |
| `OG_ellipsoid_Vol` | Initial/original calculated Sargassum pile volume            | Numeric        | m³                    | Derived         |
| `Ellipsoid_prc_D`  | Percent change in pile volume relative to the initial volume | Numeric        | %                     | Derived         |
| `delta`            | Change in pile volume                                        | Numeric        | Not used              | Derived         |
| `Area`             | Area associated with the Sargassum pile measurements         | Numeric        | m³                    | Derived         |
| `GPS_Lat `         | Latitude of the experimental plot/site                       | Character      | Geographic coordinate | Measured        |
| `GPS_Lon`          | Longitude of the experimental plot/site                      | Character      | Geographic coordinate | Measured        |
| `mean_A`           | Mean area measurement                                        | Numeric        | m³                    | Derived         |
| `mean_D1`          | Mean D1 measurement                                          | Numeric        | m³                    | Derived         |
| `mean_r`           | Mean radius                                                  | Numeric        | m³                    | Derived         |
| `mean_pile_Vol`    | Mean calculated pile volume                                  | Numeric        | m³                    | Derived         |
| `pile_vol_SE`      | Standard error of mean pile volume                           | Numeric        | m³                    | Derived         |

Pile volume was calculated using:

V = (1/3) × π × a × b × h

where `a` and `b` represent the semi-major and semi-minor axes of the pile and `h` represents pile height.

Sampling trips correspond to:

* Trip 1: August 2022
* Trip 2: November 2022
* Trip 3: March 2023
* Trip 4: August 2023





mesh_bag_exp.csv
~~~~~~~~~~~~~~~~

Purpose:
Measurements of Sargassum decomposition using smaller quantities of Sargassum enclosed in mesh bags.

Experimental treatments:
- Small mesh: 0.18 mm openings
- Large mesh: 10 mm openings

Small mesh bags excluded larger arthropods and therefore primarily represented physical processes and microbial decomposition.

Large mesh bags allowed access by larger mesodetritivores in addition to microbes and physical processes.

Starting wet biomass:
Approximately 235 g per bag.

Sampling:
- August 2022: initial deployment
- November 2022
- March 2023

The March 2023 dataset was incomplete for some portions of the experiment and was excluded from the decomposition analysis described in the manuscript.

Variables identified from the code include:
- Rep_no. (Replicate)
- Trip 
- Site
- Treatment (mesh size)
- prc_Delta (percent change from original mass)
- prc_means (mean percent change)
- prc_SE (standard error)
- ratio (ratio calculation from initial mass)

DATA DICTIONARY: mesh_bag_exp.csv

Variable        Description                                  Type          Units / Format
--------------  -------------------------------------------  ------------  ----------------
Trip            Sampling trip number                         Integer       1–3
Site            Experimental habitat                         Categorical   Beach / Forest
Treatment       Mesh size treatment                          Categorical   small / large
Rep_no.         Replicate number                             Integer       1–10
Bag_ID          Unique mesh-bag identifier                   Character     S1–S10 / L1–L10
Wi_Wet          Initial wet mass of Sargassum                Numeric       g
Wf_Ddry         Final dry mass of Sargassum                  Numeric       g
ratio           Wet-to-dry mass conversion ratio             Numeric       Unitless
Dry_est         Estimated initial dry mass                   Numeric       g
Orig_mass       Original dry mass used in calculations       Numeric       g
prc_Delta       Percent of original mass remaining           Numeric       %
prc_means       Mean percent mass remaining                  Numeric       %
prc_SE          Standard error of percent mass remaining     Numeric       %
mean_Wi         Mean initial wet mass                        Numeric       g
mean_SE         Standard error of mean initial wet mass      Numeric       g
Unnamed: 15     Blank spreadsheet column                     Unused        —
Unnamed: 16     Blank spreadsheet column                     Unused        —
Unnamed: 17     Blank spreadsheet column                     Unused        —
Unnamed: 18     Blank spreadsheet column                     Unused        —
Amphipoda       Number of amphipods recovered                Numeric       Count
Arachnida       Number of arachnids recovered                Numeric       Count
coleoptera      Number of beetles recovered                  Numeric       Count
orthoptera      Number of orthopterans recovered              Numeric       Count
hemiptera       Number of hemipterans recovered               Numeric       Count
dermaptera      Number of earwigs recovered                  Numeric       Count
Hymenoptera     Number of hymenopterans recovered            Numeric       Count
julida          Number of Julida recovered                   Numeric       Count
collembola      Number of springtails recovered               Numeric       Count


mesh_bag_inverts.csv
```

Purpose:
Counts of arthropods associated with Sargassum contained in large mesh decomposition bags.

Arthropods were identified to order in the study.

Variables include:

* Rep_no.
* Trip
* Site
* Amphipoda
* Arachnida
* Hymenoptera
* pair (collapsing "site" and "rep_no." for ease of use.

The manuscript describes talitrid amphipods as an important beach-associated decomposer, while microbial decomposition was relatively more important in the forest.

*counts are total number of individuals in the that bag.

CATEGORICAL VARIABLE DEFINITIONS

Site:
  Beach   = Beach/dune experimental habitat
  Forest  = Tropical semi-evergreen forest experimental habitat

Treatment:
  small   = Small-mesh bag (0.18 mm)
  large   = Large-mesh bag (10 mm)

Trip:
  1 = August 2022
  2 = November 2022
  3 = March 2023





interior_survey.csv

```

Purpose:
Plant percent-cover measurements collected within the experimental plot interiors.

Plant cover was measured using 0.5 m x 0.5 m quadrats containing a 100-point grid.

Three quadrats were sampled per plot.

In August and November 2022, quadrats were positioned using a haphazard placement procedure. In March and August 2023, quadrats were positioned using random directions and distances from the plot center.

The analysis grouped plants into:
- Grasses
- Other plants

 variables including:
- Block
- Treatment
- Trip
- bermuda (grass cover)
- other_plants
- other_plant_cover
- bare_prc_cover
- leaf_prc_cover
- total_plant_prc_cover
- [additional columns used to create long-format plant-cover data]

The study primarily emphasizes Bermuda grass and other plants rather than species-level community composition.

values represent percent cover (0–100)

DATA DICTIONARY: Interior_survey.csv

Description:
This file contains vegetation and ground-cover observations collected from
0.5 x 0.5 m quadrats within experimental plots. Three quadrats were surveyed
within each plot during each sampling trip. Plant taxa and ground-cover
categories were recorded as percent cover.

Variable             Description                                  Type
-------------------  -------------------------------------------  ------------
Trip                 Sampling trip number                         Integer
Site                 Experimental site/habitat                     Categorical
Block                Experimental block identifier                 Integer
Treatment            Experimental treatment                        Categorical
Quadrat              Quadrat identifier within block               Character
Rock                 Percent cover of rock                         Numeric
substrate            Percent cover of substrate                    Numeric
leaf_litter          Percent cover of leaf litter                   Numeric
sargasso             Percent cover of Sargassum                      Numeric
Cynodon_dactylon     Percent cover of Cynodon dactylon              Numeric
others               Percent cover categorized as other vegetation Numeric
Annona_spp.          Percent cover of Annona spp.                   Numeric
Cenchrus_purpureus   Percent cover of Cenchrus purpureus            Numeric
Euphorbia            Percent cover of Euphorbia                      Numeric
Misc_Dicot            Percent cover of miscellaneous dicots          Numeric
Cucumber             Percent cover of cucumber                       Numeric
NPS                  Percent cover recorded as NPS                   Numeric
Pirch                Percent cover recorded as Pirch                 Numeric
WPS                  Percent cover recorded as WPS                    Numeric
Sporobolus_jacquemontii
                     Percent cover of Sporobolus jacquemontii        Numeric
Fuzzy                Percent cover recorded as Fuzzy                 Numeric
Cenchrus_spinifex    Percent cover of Cenchrus spinifex              Numeric
Dactyloctenium_aegyptium
                     Percent cover of Dactyloctenium aegyptium       Numeric
Scaevola_taccada     Percent cover of Scaevola taccada               Numeric
Pilea_microphylla    Percent cover of Pilea microphylla              Numeric
Iron_weed             Percent cover recorded as Iron weed             Numeric
SAP                  Percent cover recorded as SAP                   Numeric
Reddish-Green        Percent cover recorded as Reddish-Green         Numeric
Misc_Mono            Percent cover of miscellaneous monocots         Numeric
Bulb                 Percent cover recorded as Bulb                   Numeric
Passiflora_spp       Percent cover of Passiflora spp.                Numeric
Stinging Nettle      Percent cover of stinging nettle                Numeric
UAP                  Percent cover recorded as UAP                    Numeric
False Buttonweed     Percent cover of false buttonweed               Numeric
Phaseolus            Percent cover of Phaseolus                       Numeric
Phyllanthus_spp.     Percent cover of Phyllanthus spp.               Numeric
Cnidoscolus aconitifolius
                     Percent cover of Cnidoscolus aconitifolius       Numeric
Hevelia pobp         Percent cover recorded as Hevelia pobp          Numeric
Canavalia_rosea      Percent cover of Canavalia rosea                Numeric
Bohemaria            Percent cover recorded as Bohemaria             Numeric
Palm                 Percent cover of palms                          Numeric
Tree                 Percent cover of trees                          Numeric
Cakile_maritima      Percent cover of Cakile maritima                Numeric
Solanum_spp.         Percent cover of Solanum spp.                   Numeric
Archontophoenix_spp.
                     Percent cover of Archontophoenix spp.            Numeric
Oplismenus_compositus
                     Percent cover of Oplismenus compositus           Numeric
Vine                 Percent cover of vines                          Numeric
Pithecellobium_dulce 
                     Percent cover of Pithecellobium dulce            Numeric
Acalypha_rhomboidea  Percent cover of Acalypha rhomboidea             Numeric
Ambrosia_spp.        Percent cover of Ambrosia spp.                   Numeric
Tournefortia_gnaphalodes
                     Percent cover of Tournefortia gnaphalodes        Numeric
Ipomea               Percent cover recorded as Ipomea                 Numeric
Berchemia_scadens    Percent cover of Berchemia scadens              Numeric
Legume               Percent cover categorized as legume               Numeric
Rose                 Percent cover recorded as Rose                   Numeric
Unnamed: 55          Blank spreadsheet column                        Unused
bermuda              Percent cover of Bermuda grass                   Numeric
leaf_cover           Percent cover of leaf material                   Numeric
bare_cover           Percent cover of bare ground                     Numeric
other_plants         Percent cover of other plants                    Numeric
Unnamed: 60          Blank spreadsheet column                        Unused
grass_means          Mean grass cover calculated across quadrats      Numeric
other_plant_means    Mean other-plant cover across quadrats           Numeric

interior_graphs.csv
```

Purpose:
Processed/derived data used to generate figures showing plant effects and/or effect sizes for the interior survey.

Variables nclude:

* Trip
* Effect_size (calculated using Cohen's d (d= (M1 - M2)/SDpooled) and manually entered
* [other columns, including Site/Cover as used by the plotting code]


perimeter_survey.csv

```

Purpose:
Plant percent-cover measurements collected immediately outside the original Sargassum pile perimeter.

Quadrats were positioned around the perimeter of plots to assess effects extending beyond the Sargassum pile footprint.

Variables identified from the code include:
- Block
- Treatment
- Trip
- bermuda
- other_plants
- total_plant_prc_cover
- dead_prc_cover
- bare_prc_cover
- [additional columns]

The perimeter survey was used to examine potential spillover effects of Sargassum additions on vegetation outside the pile footprint.

perimeter_graphs.csv
```

Purpose:
Processed/derived data used to produce perimeter plant-cover and effect-size figures.

Variables include:

* Trip
* Effect_size
* Cover
* Site
* Data

The code filters the dataset to records where Data == "eff_size" for effect-size plotting and excludes:

* all_plants
* dead
* bare

*Dataset created from perimeter_survey.csv data for simplicity in graphing. 


ladder.csv

```

Purpose:
Plant-cover measurements collected at distances beyond the experimental pile perimeter to examine the spatial extent of Sargassum effects.

The R code identifies variables including:
- Trip
- Site
- Treatment
- Quadrat
- Dist_from_edge
- Bermuda
- Other_pants
- percent_cover
- [additional columns]

"Other_pants" appears to be a spelling variation/typo for "Other_plants" in the R code.

The analysis excluded Quadrat == "0" when evaluating distances beyond the pile perimeter because the zero-distance measurements overlapped with perimeter surveys.

Distance categories include:
- Distance 1
- Distance 2

*Due to changes in methodology and no effect detected, these data wrecks not used in the final manuscript analyses.







Pitfalls.csv
```

Purpose:
Counts of crawling arthropods collected using pitfall traps.

Pitfall traps:

* Two traps per plot
* Traps placed at opposing poles of each plot
* Approximately 24-hour deployment
* Cups filled approximately halfway with water and approximately five drops of dish soap

Arthropods were identified to order.

The R code converts selected columns into a long-format variable named "Taxa" and a count variable named "Count".

crawling arthropods including:

* Arachnids
* Hymenopterans
* Crustaceans
* Talitrid amphipods at the beach

*units individuals per trap per 24-hour deployment.
* Effect_size (calculated using Cohen's d (d= (M1 - M2)/SDpooled) and manually entered


pitfalls_effsize.csv

```

Purpose:
Effect-size data used to generate the crawling-arthropod effect-size figure.

Variables :
- Trip
- Effect_size
- Order
- Site

effect sizes, lower limits, and upper limits were manually entered into this file.

* Effect_size (calculated using Cohen's d (d= (M1 - M2)/SDpooled) and manually entered

Stickies.csv
~~~~~~~~~~~~

Purpose:
Counts of flying/aerial arthropods collected using sticky traps.

Sticky traps:
- Two double-sided sticky cards per plot
- Approximately 127 mm x 76 mm
- Positioned approximately 130 mm above the substrate or Sargassum pile
- Approximately 1 m from the plot center
- Approximately 24-hour deployment

Arthropods were identified to order.

The R code converts selected columns into:
- Taxa
- Count

The manuscript identifies flying arthropods including:
- Diptera
- Hymenoptera

Amphipods could also occur on sticky traps because they may move by jumping.
*counts represent individuals per trap per 24-hour deployment.


stickies.csv
~~~~~~~~~~~~

Purpose:
Raw data used to calculate effect sizes that will be used in manuscript

The code uses variables including:
- Site
- Trip
- Treatment
- Amphipods
- Diptera
- Hymenoptera

*used to generate Cohen's d effect sizes

sticky_effsize.csv
~~~~~~~~~~~~~~~~~~

Purpose:
Effect-size data used to generate the aerial-arthropod effect-size figure.

Variables identified from the R code include:
- Trip
- Effect_size
- Order
- Site

Manually input effect sizes generated from the stickies.csv file. This was done for simplicity in code.


Soil_Chemicals2.csv
~~~~~~~~~~~~~~~~~~~

Purpose:
Soil/sediment chemistry measurements associated with the Sargassum manipulation. These were obtained for preliminary data using store bought litmus paper tests to determine if an obvious pattern existed and guide the manipulation. These data were not included in manuscript but kept for records.

The R code uses this file to examine nitrate and other chemical variables.

Variables include:
- Exp
- Type
- Trt
- Site
- Block
- Trip
- Nitrate
- pH
- KH

The analysis focuses on sediment samples associated with the Sargassum manipulation and sediment treatment.

* not used in manuscript



sargasso_nitrates.csv
```

Purpose:
Soil/sediment nitrogen and carbon measurements used in the primary nutrient analyses.

Variables include:

* NH4
* N
* C
* site
* block
* trip
* treatment
* pair
* NH4_transformed

NH4:
Ammonium concentration.

N:
Nitrate concentration.

C:
Dissolved organic carbon or carbon measurement, as used in the analysis.

The manuscript describes measurement of:

* Ammonium
* Nitrate
* Dissolved organic carbon (DOC)

Soil/sediment cores:

* Approximately 50 mL cores
* Collected from all plots
* Collected approximately 30 cm toward the plot center from plot edges
* Overlying Sargassum and leaf litter were removed before sampling

Ammonium and nitrate were measured using spectrophotometry. Dissolved organic carbon was assessed following the cited soil-carbon method.

NH4 was positively skewed in the R analysis and was transformed using:

log1p(NH4)





gas_readings.csv

```

Purpose:
Soil respiration measurements associated with the Sargassum manipulation.

The R code identifies variables including:
- gCO2_m2_h
- month
- plotnum
- site
- trip

Soil respiration was measured by collecting gas samples from inverted 1.87-L containers placed approximately 30 cm toward the plot center from the plot edge.

Containers were deployed for approximately one hour.

Gas samples were analyzed for CO2 using gas chromatography.

The manuscript describes the response variable as CO2 production/soil community respiration.




VARIABLE CODING
---------------

Treatment
~~~~~~~~~

The experimental treatment is generally coded as:
- Sargassum = Sargassum addition
- Control = unmanipulated control

Habitat / Site
~~~~~~~~~~~~~~

The study contains two habitats:
- Beach
- Forest

The R code sometimes uses alternative labels:
- Dune = Beach
- Jungle = Forest

Sampling Trip
~~~~~~~~~~~~~


1 = August 2022
2 = November 2022
3 = March 2023
4 = August 2023





METHODS SUMMARY
---------------

Sargassum pile decomposition
```

Large Sargassum piles were monitored by measuring pile volume through time.

Because the initial pile volumes differed between habitats, pile volume was converted to a percentage of initial volume for decomposition analyses.

Smaller quantities of Sargassum were also placed in mesh bags to separate the relative contributions of physical processes/microbial activity from larger arthropods.

Small mesh:
0.18 mm

Large mesh:
10 mm

Starting wet biomass:
approximately 235 g per bag

At the final sampling, Sargassum was dried to obtain dry biomass. Starting dry biomass was estimated using the dry:wet mass ratio, and decomposition was calculated as a percentage of initial dry biomass.

Soil nutrients

```

Sediment/soil cores were collected from experimental plots.

Measured variables included:
- Ammonium
- Nitrate
- Dissolved organic carbon

Samples were processed and analyzed using spectrophotometric and carbon-analysis methods described in the manuscript.


Soil respiration
```

Soil respiration was estimated from CO2 accumulation in approximately 1.87-L inverted containers deployed for one hour.

Gas samples were analyzed by gas chromatography.

The measurements were intended to represent respiration of the soil community beneath the experimental piles rather than respiration occurring directly on the Sargassum piles.

Plant community

```

Plant cover was estimated using 0.5 m x 0.5 m quadrats with a 100-point grid.

Only the upper/canopy layer was recorded at each point.

Plants were generally analyzed as:
- Grasses
- Other plants

Bermuda grass (Cynodon dactylon) was particularly important at the beach site.
 


Arthropod community
```

Crawling arthropods:
Measured using pitfall traps.

Flying/aerial arthropods:
Measured using sticky traps.

Arthropods were generally identified to order for the community-level analyses.






## STATISTICAL ANALYSES

The R Markdown contains analyses including:

* Linear mixed-effects models
* ANOVA
* Welch two-sample t-tests
* Standard two-sample t-tests
* Levene's tests
* Estimated marginal means
* Cohen's d effect sizes
* Residual/normality diagnostics
* Rank transformation
* Log1p transformation

Pile decomposition:
Linear mixed-effects model examining pile volume percentage as a function of Trip, Location, and their interaction, with Block as a random effect.

Mesh-bag decomposition:
ANOVA examining mesh size, habitat/site, and their interaction.

Where mesh size interacted with habitat, analyses were conducted separately by habitat.

Large-mesh decomposition:
Welch two-sample t-test comparing decomposition between habitats.

Arthropods in mesh bags:
Three-way ANOVA involving arthropod order, habitat, and sampling trip.

Soil nutrients and respiration:
Linear mixed-effects models examining treatment, habitat, sampling trip, and their interactions, with plot identity/pairing represented as a random factor.

Soil respiration:
rank-transformed the response because of large variance.

Plant community:
Cohen's d was used to quantify treatment differences in plant cover.

Arthropod community:
Cohen's d was used to quantify treatment differences in crawling and flying arthropod abundance.

All analyses and figures were conducted in R.

## R SOFTWARE AND PACKAGES

R studio version Version 2025.09.2+418 (2025.09.2+418)

knitr
patchwork
tidyverse
tidyr
ggplot2
ggfortify
lme4
lmerTest
car
nlme
ggpubr
multcompView
boot
Hotelling
mvnTest
vegan
factoextra
FactoMineR
agricolae
glmm
HH
rstatix
effsize
broom
performance
DHARMa
glmmTMB
emmeans
kableExtra




## MISSING DATA AND EXCLUSIONS


Mesh-bag decomposition:

* Initial deployment (Trip 1) was excluded when calculating percent change because it represents the starting condition.
* Incomplete March 2023 data were excluded from the primary mesh-bag decomposition analysis.
* Large-mesh bags were used for the comparison of overall decomposition between habitats.

Plant distance surveys:

* Some distance measurements were excluded/corrected because the distance from the original pile edge changed as piles decomposed.
* The manuscript states that some distance comparisons were removed because the corrected distances did not permit rigorous comparison across habitats.

Arthropod data:

* Some beach large-mesh bags were not recovered in March 2023 because of vandalism.



 
The primary analysis script is:

Sargasso_Subsidy_code.Rmd

The R Markdown script expects the data files to be located in the project working directory:

~/Documents/GitHub/Sargasso_Subsidy


Recommended project structure:

Sargasso_Subsidy/
|
|-- README.txt
|-- Sargasso_Subsidy_code.Rmd
|
|-- data/
|   |-- Sargassum_piles.csv
|   |-- mesh_bag_inverts.csv
|   |-- mesh_bag_exp.csv
|   |-- interior_survey.csv
|   |-- interior_graphs.csv
|   |-- perimeter_survey.csv
|   |-- perimeter_graphs.csv
|   |-- ladder.csv
|   |-- Pitfalls.csv
|   |-- pitfalls_effsize.csv
|   |-- Stickies.csv
|   |-- stickies.csv
|   |-- sticky_effsize.csv
|   |-- Soil_Chemicals2.csv
|   |-- sargasso_nitrates.csv
|   |-- gas_readings.csv
|   |-- nmec.csv
|
|-- figures/


## CITATION

[TODO: Add the final citation for the dataset.]

Suggested study citation:

DeSantiago, R., R. E. Rodríguez-Martínez, D. Lipson, A. Alvarez, and J. D. Long.
"Ecological effects of dumping massive amounts of the nuisance seaweed, Sargassum,
in Caribbean beach and forest sites."



## CONTACT

Corresponding author:
Dr. Ricardo DeSantiago

Email:
[desantiago87@gmail.com](mailto:desantiago87@gmail.com)



## PERMITS AND ACCESS

The experimental work was conducted with permission from the Mexican government under permit:

CONANP-00-007

Permission was also obtained from the local property managers.

Beach site:
Moon Palace Resorts

Forest site:
Jardín Botánico ECOSUR "Dr. Alfredo Barrera Marín"



## ACKNOWLEDGMENTS

The manuscript acknowledges assistance from personnel at Jardín Botánico ECOSUR "Dr. Alfredo Barrera Marín," Moon Palace Resorts/Gerencia Ambiental de Palace Resorts, and other collaborators and field/laboratory personnel.



# END README
