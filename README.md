# Raster4H
Raster datasets for Helsinki area created from HSY and Helsinki city open access data. 
Made to be manipulated by P4UL scripts (https://github.com/mjsauvinen/P4UL)
PALM-ready input files utilize P4UL scripts and Topography/Orography maps from RasterH3D (https://github.com/mjsauvinen/RasterH3D/)

Usage: Made to be used in modeling purposes where information about surface types is required.

DISCLAIMER: 
- All rasters were created in June 2019. Any changes made after this time to the source files such as buildings added by Helsinki city are obviously not included.
- Building type has missing buildings and should be only used as a mask on more accurate maps.
- HSY map layer "water impervious surfaces (2018)" is originally from vegetation type, but is included in pavement type as asphalt/concrete mixture.

## Soil type

Tiivistelmä: Geologian tutkimuskeskuksen Maaperä 1:20 000 / 1:50 000 / 1:100 000 - aineistoista luotu Helsingin alueen kartta maalajeista päällimmäisen 0.4 - 0.9 metrin syvyydeltä. 1:100 000 datassa olevia kartoittamattomia alueita on täydennetty tarkemmilla 1:20 000/1:50 000 kartoilla ja yhdistetty yhdeksi vektorikartaksi. Tästä seuraa horisontaalinen raja keskellä karttaa, mihin tarkempi kartta loppuu.

Abstract: The superficial deposits of Helsinki area at 0.4 - 0.9 meter depth taken from Geological Survey of Finland’s 1:20 000 / 1:50 000 / 1:100 000 data.
1:100 000 uncharted areas are filled with more precise information taken from 1:20 000/1:50 000 maps and combined into a single vector map. This results in a horizontal line across the map from where the finer map ends.

Tarkemmat tiedot ja metatiedot:

More information and metadata:

20-/50k http://tupa.gtk.fi/paikkatieto/meta/maapera_20_50k.html

100k     http://tupa.gtk.fi/paikkatieto/meta/maapera_100k.html

## Building type

Tiivistelmä: Helsingin kaupungin avoimesta datasta tehty kartta, jossa näkyy Helsingin alueen rakennukset luokiteltuna asuinrakennuksiin ja yleisiin- tai liikerakennuksiin. Käytetään vain täydennyksenä jo olemassa olevaan laserkeilausaineistoon, sillä vektorikartasta puuttuu huomattavasti rakennuksia.

Abstract: Building raster map created for Helsinki area from open data. The map tells roughly which buildings are residential and which are office buildings. Used only as a mask to pre-existing LiDAR data.

Tarkemmat tiedot ja metatiedot:
Specific information and metadata:
https://hri.fi/data/dataset/helsingin-rakennukset 


## Pavement type

Tiivistelmä: HSY:n ja Helsingin kaupungin avoimesta datasta tehty kartta, joka käyttää seudullisen maanpeiteaineiston maankäyttökerroksia ja Helsingin kaupungin YLRE (Ylisten alueiden Reksteri) tietoja katu- ja viheralueista sekä niiden materiaaleista.
HSY:n aineisto yhdistetty Helsingin kaupungin kanssa siten, että kerrokset päällystetty/päällystämätön on määritetty vastaavasti asfalttibetoniksi/kivituhkaksi.

Abstract: Pavement raster map created from HSY and Helsinki city open data. HSY layers "paved/unpaved roads" are defined as "asphalt/fine gravel" respectively.

Tarkemmat tiedot: 
YLRE: https://hri.fi/data/fi/dataset/helsingin-kaupungin-yleisten-alueiden-rekisteri
HSY:   https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

## Water type


Tiivistelmä: HSY:n avoimesta seudullisesta maanpeiteaineistosta tehty kartta, jossa näkyy Helsingin alueen vesistöt kahdessa kerroksessa.

Abstract: Helsinki region water body raster created from open HSY data. Sea map and smaller water bodies merged into a single layer. 


Tarkemmat tiedot:
https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38


## Vegetation type

Tiivistelmä: HSY:n avoimesta seudullisesta maanpeiteaineistosta tehty kartta, jossa näkyy Helsingin alueen karkea kasvillisuusryhmien luokittelu.

Abstract: Generalized vegetation raster map created from open HSY data. 


Tarkemmat tiedot:
https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

