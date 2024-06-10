[About](Project.html) [Data](Data.html)

# Using Fluorometer Measurements to Gather Verifiable Chlorophyll A Concentration Data

### *Manatee County Natural Resources Department-Environmental Protection Division; Intern Brendan McKnight*

Here in Manatee county, water quality of our waterways is very important to us. We have two water quality monitoring programs that assess the most important waterways throughout the county, with about half being inland locations and half being out in the bay. These sites are assessed monthly, however this does not provide the Environmental Protection Division (EPD) with enough data to conduct investigations into the causes and effects of nutrient loading/eutrophication, and what can be done to reduce it. In order to assess eutrophication, the concentration of chlorophyll a, a pigment contained in the algae responsible for blooming, must be determined. The current method approved by the EPA to determine chlorophyll a concentration involves taking a sample from the field, and bringing it back to the lab for hours of preparation and testing. Despite this, fluorometers exist that carry the capabilities to determine the chlorophyll a concentration in an environment by emitting light and recording the light response made by the algae in the water. Unfortunately, due to their lack of accuracy, they are not approved as a method of collecting verifiable chlorophyll a concentrations. They are however very precise, and with the ability to correct the accuracy of such readings, the possibility for a new method to collect data on eutrophication is possible. This is the practical goal of this project, to collect enough data comparing field and lab analyzed results in the hopes of calculating a correction factor for in-vivo fluorometer readings that qualify them as verified data. If this is achieved, the EPD can gather data regarding eutrophication remarkably faster and more frequently allowing us to investigate more thoroughly the issues causing eutrophication in our county's waterways. With this ability, the EPD would be able to report on the severity of causes of nutrient loading as well as be able to compare the effectiveness of different efforts being made to reduce nutrient loading. By using the technology we already have at our footsteps, we may be able to make a lasting effect in the scientific community that is concerned with eutrophication, and help our precious environments that are being put at risk.

Use this page to learn more about this project by visiting the multiple tabs below. This project is ongoing so for now the currents pages are; About and Data. As the project progresses over it's span of ten weeks, the contents and tabs will be changed and added to as it works to become a site for the findings and results of this project.

# About

#### Scientific Narrative

The Manatee County Natural Resources department has two programs that assess water quality both off the coast of Tampa and Sarasota Bay, as well as in freshwater systems. These programs are named the Regional Ambient Monitoring Program (RAMP) and Surface Water Ambient Monitoring Program (SWAMP). There are 80 sites in total between the two programs where water quality is regularly assessed. Eutrophication of bodies of water is a worldwide issue, and locally poses a threat to the many important aquatic ecosystems in and around Manatee County. The Natural Resources Department’s Environmental Protection Division (EPD), among many other purposes, uses the RAMP and SWAMP to better understand the causes of eutrophication and what can be done about it. To investigate eutrophication, chlorophyll a analysis must be carried out to determine the concentration of phytoplankton in the water. This is done via laboratory analysis of water samples taken in the field, a process that can be both time and labor intensive, but necessary to creating sets of verified, validated data that can be used in decision making processes. Because of the time and energy needed to do chlorophyll a analysis at all 80 sites, data is mostly only recorded once a month at each location. This means that current data collection procedures do not produce enough results to be able to show correlation between causes and results of eutrophication. The main goal of this project is to be able to increase the amount of data collections that can be used as reference data to assess how protection efforts and ecological events affect the level of eutrophication in the waters in and around Manatee County.

Fluorometers serve as an efficient method to record values of chlorophyll a concentration in both fresh and saltwater, by emitting UV light and recording the irradiance emitted as a result of the light interaction with phytoplankton light harvesting complexes. Although this is possible, it is not an EPA approved method of measuring chlorophyll a concentration due to too much variance. Instead, the EPA approved method entails taking samples back to a lab where acetone is used to dissolve all cells and material, leaving chlorophyll a in the sample where concentration can be verifiably measured using a fluorometer. Thus, one goal of this project is to collect enough data from both field fluorometer measured chlorophyll a concentration and EPA approved measurements of chlorophyll a concentration. These two data sets are to be used to determine a correction factor that can be implemented to achieve the goal of creating an EPA approved method of chlorophyll a data collection using fluorometric field recordings. This would allow for more efficient data collection meaning the RAMP and SWAMP sites could be tested weekly for eutrophication levels. If this is achieved, the EPD can investigate how weather events and certain environmental protection efforts are affecting levels of eutrophication in surrounding waterways. One effort made by the Manatee County Government to reduce eutrophication is street sweeping to reduce nutrients washed into the waterways after storms. In one area encompassing a section of Bowlee’s Creek where two SWAMP stations exist, street sweeping has been doubled. If field fluorometer data could be verifiable, street sweeping statistics recorded by sweeping vehicles could be used in accordance with weekly, or even biweekly, chlorophyll a concentration to show the effects of street sweeping efforts on eutrophication in Manatee County’s waterways and be used to implement these efforts across the county. Many other efforts to decrease nutrient loading could be tested as well as the effects of ecological events if field fluorometer measurements can become an EPA approved method of chlorophyll a concentration measurement.

#### Timeline of Goals

I. Visit SWAMP stations regularly to collect as much data as possible. At each station visited, record field measurements of chlorophyll a, turbidity, salinity, and any other possible covariates. Along with field measurements, collect a water sample to be brought back to the laboratory for verified chlorophyll a analysis.

II\. Form data set containing all data collected from SWAMP sites, including laboratory chlorophyll a analysis. Use Quarto to build an html file that updates findings and results live as data is collected. In due time, publish file as a web link using github.

III\. Investigate data set using statistical application, focusing on the relationship between laboratory analyzed chlorophyll a concentrations and chlorophyll a concentration as determined by field measurements. Investigate the role of other factors such as salinity, turbidity, etc., as covariates in the relationship between the two chlorophyll a measurement types.

IV\. Use results from data investigation to form a correction factor that accounts for the errors in equipment used for field measurements of chlorophyll a, along with any identified covariates relating to such measurements of chlorophyll a. Use correction factor to form a method of chlorophyll a concentration determination that provides data that is both verifiable and able to be validated by standards put forth by the EPA.

V. Implement new method of chlorophyll a data collection in areas where efforts to reduce nutrient loading and the subsequent eutrophication have been carried out. Investigate the roles of these efforts on eutrophication through frequent data collection, and present which efforts are most effective in attempts to have them implemented county wide.

# Data

#### Raw Field Data

```{r}
#| warning: false
#| echo: false

library(tidyverse)
library(knitr)
library(kableExtra)


field_data <- read_csv("field_data.csv")

field_data_table <- field_data %>%
  select(Station, date, Chla) %>%
  arrange(Station, date, Chla)

kable(field_data_table)
```

#### Raw Laboratory Data

```{r}
#| warning: false
#| echo: false

library(tidyverse)
library(knitr)
library(kableExtra)

lab_data <- read_csv("lab_data.csv")

lab_data_table <- lab_data %>%
  select(Station, date, Chla) %>%
  arrange(Station, date, Chla)

kable(lab_data_table)
```

#### Linear Regression Comparison

```{r}

```
