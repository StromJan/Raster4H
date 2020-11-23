# Raster4H (Raster for Helsinki)
Raster datasets for Helsinki area created from HSY and Helsinki city open access data. 
- Made to be manipulated by P4UL scripts (https://github.com/mjsauvinen/P4UL)
- PALM-ready input files utilize P4UL scripts and Topography/Orography maps from RasterH3D (https://github.com/mjsauvinen/RasterH3D/)
- Final version has updated topography and orography maps for whole Helsinki area using the same open access LiDar dataset from https://kartta.hel.fi/ Created mainly using scripts kindly provided by Mikko Auvinen  (https://github.com/mjsauvinen) from the Finnish Meteorological Institute (FMI).

### Data formats
The processed data is given in npz format to be directly used with P4UL library and in georeferenced TIFF (GeoTIFF) for more general and standardised presentation.

### Disclaimer 
- All rasters were created in June 2019. Any changes made after this time to the source files such as buildings added by Helsinki city are obviously not included.
- Building type has missing buildings and should be only used as a mask on more accurate maps.
- HSY map layer "water impervious surfaces (2018)" is originally from vegetation type, but is included in pavement type as asphalt/concrete mixture.
- Updated topography and orography maps do NOT have data from the military areas of Santahamina etc. for security reasons.

### Licenses
Raster files are published under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
The publishers of the original datasets must be attributed accordingly, see [LICENSE file](LICENSE).

### Contributors
Jani Strömberg<sup>1</sup> (raster processing, npz files, documentation)  
Sasu Karttunen<sup>1</sup> (georeferenced TIFFs, documentation)  
<sup>1</sup> Institute for Atmospheric and Earth System Research / Physics, Faculty of Science, University of Helsinki, Finland

## Topography, orography and tree height
### Tiivistelmä
Laserkeilausaineistosta määritetyt pinnan- ja maastonmuodot sekä puuston korkeus. Tiedot on ilmoitettu liukulukuna yksikkönä
metriä merenpinnan tasosta npz-muodossa ja kokonaislukuna yksikkönä 10 cm merenpinnan tasosta GeoTIFF-muodossa pinnan- ja maastonmuodoille.
Puuston korkeus on ilmoitettu vastaavalla tavalla, mutta suhteessa maan pintaan kyseisessä pisteessä. Vaakaresoluutio on kaikissa 1 metri.

### Abstract
Lidar-derived data of topography, orography and tree height at 1 m horizontal resolution. For topography and orography, the data is given in floating point
type signifying meters from mean sea level (npz format) or as a signed integer number with unit of 10 cm difference from sea level (GeoTIFF).
The tree height is given in same format, but with respect to the local ground level (agl).

## Land cover
### Tiivistelmä
HSY:n avoimesta seudullisesta maanpeiteaineistosta tehty kartta, jossa näkyy Helsingin alueen maanpeitto kolmeen luokkaan jaoteltuna.

### Abstract
Helsinki region land cover raster created from open HSY data. Land cover types are classified into three categories.

### Metatiedot / metadata:
https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

### Luokat / Labels
0: Ei dataa / No data
2: Maa / Ground
6: Rakennus / Building
9: Vesi / Water

## Soil type
### Tiivistelmä
Geologian tutkimuskeskuksen Maaperä 1:20 000 / 1:50 000 / 1:100 000 - aineistoista luotu Helsingin alueen kartta maalajeista päällimmäisen 0.4 - 0.9 metrin syvyydeltä. 1:100 000 datassa olevia kartoittamattomia alueita on täydennetty tarkemmilla 1:20 000/1:50 000 kartoilla ja yhdistetty yhdeksi vektorikartaksi. Tästä seuraa horisontaalinen raja keskellä karttaa, mihin tarkempi kartta loppuu.

### Abstract
The superficial deposits of Helsinki area at 0.4 - 0.9 meter depth taken from Geological Survey of Finland’s 1:20 000 / 1:50 000 / 1:100 000 data.
1:100 000 uncharted areas are filled with more precise information taken from 1:20 000/1:50 000 maps and combined into a single vector map. This results in a horizontal line across the map from where the finer map ends.

### Metatiedot / metadata:
20-/50k http://tupa.gtk.fi/paikkatieto/meta/maapera_20_50k.html
100k     http://tupa.gtk.fi/paikkatieto/meta/maapera_100k.html

### Luokat / Labels
0: Ei dataa / No data
1: Karkea / Coarse
2: Medium / Medium
3: Medium-hieno / Medium-fine
4: Hieno / Fine
5: Erittäin hieno / Very fine
6: Orgaaninen / Organic
7: Luokittelematon / Unclassified

## Building type
### Tiivistelmä
Helsingin kaupungin avoimesta datasta tehty kartta, jossa näkyy Helsingin alueen rakennukset luokiteltuna asuinrakennuksiin ja yleisiin- tai liikerakennuksiin. Käytetään vain täydennyksenä jo olemassa olevaan laserkeilausaineistoon, sillä vektorikartasta puuttuu huomattavasti rakennuksia.

### Abstract
Building raster map created for Helsinki area from open data. The map tells roughly which buildings are residential and which are public or office buildings. Used only as a mask to pre-existing LiDAR data.

### Luokat / Labels
0: Ei dataa / No data
10: Asuinrakennus / Residential
20: Public or office

### Metatiedot / metadata:
Specific information and metadata:
https://hri.fi/data/dataset/helsingin-rakennukset 

## Pavement type
Tiivistelmä: HSY:n ja Helsingin kaupungin avoimesta datasta tehty kartta, joka käyttää seudullisen maanpeiteaineiston maankäyttökerroksia ja Helsingin kaupungin YLRE (Ylisten alueiden Reksteri) tietoja katu- ja viheralueista sekä niiden materiaaleista.
HSY:n aineisto yhdistetty Helsingin kaupungin kanssa siten, että kerrokset päällystetty/päällystämätön on määritetty vastaavasti asfalttibetoniksi/kivituhkaksi.

### Abstract
Pavement raster map created from HSY and Helsinki city open data. HSY layers "paved/unpaved roads" are defined as "asphalt/fine gravel" respectively.

### Metatiedot / metadata:
YLRE: https://hri.fi/data/fi/dataset/helsingin-kaupungin-yleisten-alueiden-rekisteri
HSY:   https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

### Luokat / Labels
0: Ei dataa / No data
1: Asfalttibetoni (paved) / Asphalt concrete (paved)
2: Betoni / Concrete
3: Puusilppu / Wood shavings
4: Hiekka / Sand
5: Tekonurmi / Artificial turf
6: Hieno sora (päällystämätön) / Fine gravel (unpaved)
7: Mukulakivi / Cobblestone
8: Tartan, kumi / Tartan, rubber
9: Teräs / Steel
10: Sora / Gravel
11: Puu / Wood
12: Graniitti / Granite
13: Tiili, keraaminen kivi / Brick, ceramic
14: Luonnonkivet, kallio / Natural stone, rock
15: Muovi / Plastic
16: Muu materiaali / Other material

## Water type
Tiivistelmä: HSY:n avoimesta seudullisesta maanpeiteaineistosta tehty kartta, jossa näkyy Helsingin alueen vesistöt kahdessa kerroksessa.

### Abstract
Helsinki region water body raster created from open HSY data. Sea map and smaller water bodies merged into a single layer. 

### Metatiedot / metadata:
https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

### Luokat / Labels
0: Ei dataa / No data
1: Merialue / Sea, saltwater
2: Lammikot, purot, joet / Ponds, streams, rivers

## Vegetation type
### Tiivistelmä
HSY:n avoimesta seudullisesta maanpeiteaineistosta tehty kartta, jossa näkyy Helsingin alueen karkea kasvillisuusryhmien luokittelu.

### Abstract
Generalized vegetation raster map created from open HSY data.

### Metatiedot / metadata:
https://www.hsy.fi/fi/asiantuntijalle/avoindata/Sivut/AvoinData.aspx?dataID=38

### Luokat / Labels
0: Ei dataa / No data
1: Avokallio /Open rock
2: Vettä läpäisemätön pinta / Impervious surface
3: Paljas maa / Bare soil
4: Matala kasvillisuus / Low vegetation
5: Pelto / Field, farmland
6: Puusto 2-10 m / Trees 2-10 m
7: Puusto 10-15 m / Trees 10-15 m
8: Puusto 15-20 m / Trees 15-20 m
9: Puusto yli 20 m / Trees over 20 m