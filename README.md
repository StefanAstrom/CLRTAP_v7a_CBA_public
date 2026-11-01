# 2026_v7a1_Goth_Prot_CBA
This depository contains the tables and python code used to calculate the costs and benefits of emission control scenarios discussed in the Air Convention as of September 2026. The Corresponding GAINS model scenario group is GAINS v7a

## Licencing

This material has been produced during the realization of the project funded by the Nordic Council of Ministers. The project has been led by Stefan Åström from the UNECE Air Convention Task Force on Integrated Assessment Modelling (TFIAM) and Anthesis AB. Project collaborators have been Krister Mars & Lovisa Årebäck from Anthesis AB, Henrik Lindhjem & Ståle Navrud from Menon Economics, Jesper Bak from the Air Convention Working Group on Effects (WGE) and Aarhus University), and Mike Holland from Econometrics Research Consultants (EMRC). 

*CBA GBG Protocol 2026  © 2026 by Stefan Åström, Lovisa Årebäck, Krister Mars, Henrik Lindhjem, Ståle Navrud, Mike Holland and Jesper Bak, is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/*

### Nordic Council of Ministers terms and conditions

Unless otherwise specified in the agreement, the title, copyright and any other right in material and results that have emerged during the realization of the action, belong to the administrative body. The administrative body's use of the rights is, however, limited to the Nordic Council of Ministers' rights, see below, and is subject to the following restrictions:

- the use may not be contrary to section 10 of these terms and conditions concerning a duty of confidentiality,

- the use may not have any commercial purpose, 

- the use may not infringe a third party's title, copyright or other right.

On publication of material and results, the administrative body is under an obligation to state that they have been produced during the realization of the action funded by the Nordic Council of Ministers.

The Nordic Council of Ministers acquires a permanent, unlimited and cost-free right to use material and results produced during the realization of the action of the work and may transfer this right to others. The right to use the material and results includes among other things:

- the right to copy preliminary or final reports, 

- the right to publish material and results,

- the right to have material and results translated into other languages,

- the right to use material and results in all activities of the Nordic Council of Ministers.

All rights to publication in all current and future printed and electronic formats belong to the Nordic Council of Ministers, which has the right to publish material and results under the licence used by NCM. However, the administrative body is entitled to publish the final result of the project if the Nordic Council of Minister has not published the result within six month after the completion of the action.

## Installation
Requires Python 3.11 or newer (tested with Python 3.11.15).

pip install -r requirements.txt

## Running Order
1. EMEP_country_level_analysis: Extracts variables from the EMEP .nc files and exports them to Raw_Data.
2. Table_Conversion: Reads input data from Raw_Data and creates processed datasets in Processed_Data.
3. CBA_v7: Reads processed datasets from Processed_Data and performs the cost-benefit analysis.
   
Results are written to the Tables and Plots folders.

## Input data and source overview

Below is a table containing a description and source overview of the input files for the CBA, available in the Raw Data folder

| CBA Section | Name | File/Source |Download date|
|:--------|:--------|:--------|:--------|
|  General   |  Regional Allocation   |  12 <br> https://tool.valesor.eu/   | 31st of August 2026 |
|  General   |  Population in 5 yr Cohorts   |  8 <br> https://tool.valesor.eu/   |31st of August 2026|
|  General   |  Life Expectancy at 5 year Cohorts   |  WPP2024_GEN_F01_DEMOGRAPHIC_INDICATORS_FULL <br> UN World population prospects   |31st of August 2026|
|  General   |  Air Pollution Costs   |  LRTAP_ctry_GNFR_APcost_v7a_090926_0 <br> TFIAM Web page   |31st of August 2026|
|  Biodiversity   |  Exceedence of CL in Forest and Seminatural ecosystems   |  v7a_2040_clempn_exc_allecosys <br> GAINS Explorer online   |31st of August 2026|
|  Fertilisation   |  Non-exceedence of CL in Forest ecosystems   |  v7a_2040_clempn_exc_allecosys <br> GAINS Explorer online |31st of August 2026|
|  Climate   |  Emission levels   |  LRTAP_ctry_GNFR_emis_v7a_090926_0 <br> TFIAM Web page   |31st of August 2026|
|  Climate   |  Emissions Damage Costs   |  SLCF_econ_value <br> https://doi.org/10.1017/bca.2023.8   |31st of August 2026|
|  Climate   |  Emissions Climate Forcing Values   |  Climate_Metric <br> https://doi.org/10.1017/bca.2023.8   |31st of August 2026|
|  Health   |  PM2.5 Concentrations   |  v7a_2040_yoll_Europe <br> GAINS Explorer online   |31st of August 2026|
|  Health   |  Exposure Respone Function (ERF)   |  Health_ERF <br> https://tool.valesor.eu/   |31st of August 2026|
|  Health   |  Morbidity Costs   | 12/Nordic_mor_cost <br> https://tool.valesor.eu/ & https://doi.org/10.1787/76ca89a2-en   |31st of August 2026|
|  Health   |  Mortality Costs   |  12/Nordic_mor_cost <br> https://tool.valesor.eu/ & https://doi.org/10.1787/76ca89a2-en   |31st of August 2026|
|  Health   |  Mortality Incidents Rate per Cohort   |  8 <br> https://tool.valesor.eu/ & https://doi.org/10.1787/76ca89a2   |31st of August 2026|
|  Health   |  Morbidity Incidents Rate per Cohort   |  8 <br> https://tool.valesor.eu/ & https://doi.org/10.1787/76ca89a2   |31st of August 2026|