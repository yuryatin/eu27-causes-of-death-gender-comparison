# Description

This R code visualizes the proportion of deaths by ICD-10 category across age groups for both sexes, using the Eurostat dataset **estat_hlth_cd_aro**.

# Data source

The Eurostat dataset **estat_hlth_cd_aro** is currently available at:
[https://ec.europa.eu/eurostat/api/dissemination/sdmx/2.1/data/hlth_cd_aro?format=TSV&compressed=true](https://ec.europa.eu/eurostat/api/dissemination/sdmx/2.1/data/hlth_cd_aro?format=TSV&compressed=true)

# How to use this R code

1. Install [R](https://www.r-project.org), a free software environment for statistical computing and graphics.  
2. Copy all the code fragments from the file `notebook.ipynb` (found in this repository) into a new `.R` file.  
3. Run the `.R` file in your installed R environment.

# How to plot statistics for specific countries

In the 7th section of the notebook, you can change the default values for the input variables:
```r
region = 'EU27_2020'
region_name = 'EU27 countries'
year_to_analyze = 2022
condition = 'I20-I25' #'I' #I = all CVD
condition_name = 'CHD' # 'CVD'
```
The available regions/countries (`region`) are: `EU27_2020 EU28 AT BE BG CH CY CZ DE DK EE EL ES FI FR FX GE HR HU IE IS IT LI LT LU LV MT NL NO PL PT RO RS SE SI SK TR UK`.

After changing the `region` variable, you may want to manually update `region_name` so that the plot correctly attribute the data.

You can also customize the year (`year_to_analyze`), which can take values from 2011 through 2022, and the medical condition (condition).

The available ICD-10 codes are: `A15-A19_B90 ACC ACC_OTH A_B A_B_OTH B15-B19_B942 B180-B182 B20-B24 C C00-C14 C00-D48 C15 C16 C18-C21 C22 C25 C32 C33_C34 C43 C50 C53 C54_C55 C56 C61 C64 C67 C70-C72 C73 C81-C86 C88_C90_C96 C91-C95 C_OTH D00-D48 D50-D89 E E10-E14 E_OTH F F01_F03 F10 F_OTH G20 G30 G_H G_H_OTH I I20-I25 I20_I23-I25 I21_I22 I30-I51 I60-I69 I_OTH J J09-J11 J12-J18 J40-J44_J47 J40-J47 J45_J46 J_OTH K K25-K28 K70_K73_K74 K72-K75 K_OTH L M M_OTH N N00-N29 N_OTH O P Q R R95 R96-R99 RHEUM_ARTHRO R_OTH TOTAL TOXICO U071 U072 U_COV19_OTH V01-Y89 V01-Y89_OTH V_Y85 W00-W19 W65-W74 X40-X49 X60-X84_Y870 X85-Y09_Y871 Y10-Y34_Y872`. 

You can check their descriptions in the Eurostat documentation:
[ICD-10 code descriptions](https://ec.europa.eu/eurostat/cache/metadata/Annexes/hlth_cdeath_sims_an_2.pdf)

Several additional categories include:
- `B180-B182` Chronic viral hepatitis B and C
- `K72-K75` Chronic liver disease (excluding alcoholic and toxic liver disease)
- `U071` COVID-19, virus identified
- `U072` COVID-19, virus not identified
- `U_COV19_OTH` COVID-19, other

The `condition_name` variable specifies the medical condition name that will be **shown** on the plot.

# The output

This code saves a `plot.svg` file in the same folder as your new `.R` script. It looks like this:

![plot](https://github.com/user-attachments/assets/fc38970d-4b73-4260-8ecd-cf7c96c8b1e4)

# Already generated GIFs

You may also want to check the `generated_gifs_for_countries` folder in this repository for GIFs that have already been generated for selected EU countries and specific cardiovascular ICD10 code groups.

![estat_hlth_cd_aro_I21 I22_vs_CV_in_France](https://github.com/user-attachments/assets/63eaa2a2-6bd4-40dd-b70b-29d56e6cf95f)
