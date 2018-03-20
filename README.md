# mnwx
This R package retrieves and processes meteorological data for air modeling.


The following meteorological stations are available:

| call_sign     | name          | county  | state  |
| ------------- |:-------------:| -------:|--------|
| AXN           | Alecandria    | Douglas |  MN    |
|     |       |      |  |
| |     |      | |


> *1-min. data (January-May) and 5-min data (June-December) for the year 2013 (January through May).
>
> **Duluth Sky Harbor (KDYT) METAR AWOS site exceeded EPA Region 5 allowable calms in 2014 making 2012-2016 dataset ineligible for use. The previous AERMET v14134 2009-2013 files will be allowed for use. MPCA will be working with area meteorological data to find a workable solution to best serve the Duluth/Superior (Twin Ports) area and will update and post once available.

<br>

Data files within each zip file follow the 8-character naming convention of SFCUPAYY (ex., MSPMPX12):

- The first three characters, SFC, represents the meteorological surface station ID (ex., MSP);
- The fourth through sixth characters, UPA, represents the upper air station ID (ex., MPX for the Chanhassen, MN upper air station);
- The last two characters, YY, represents the two digit year (ex., 12 = 2012, 16 = 2016, 5Y = five-year concatenated file, etc.).

Each zip file contains:

- 5-year wind roses (SFCUPA5Y_windrose_YYYY-YYYY.bmp)
- 5-year wind frequency counts (SFCUPA5Y_FreqCount_YYYY-YYYY.csv)
- AERSURFACE outputs for each year (SFC_YYYY_AERSURFACE.out)
- 5-year concatenated profile file (SFCUPA5Y_YYYYYYYY.pfl)
- 5-year concatenated surface file (SFCUPA5Y_YYYYYYYY.sfc)
- 5 subfolders for each individually-processed year, each of which contains:
    - Yearly wind rose (SFCUPAYY_windrose.bmp)
    - AERMET stage 3 input file (SFCUPAYY.in3)
    - Wind frequency counts (SFCUPAYY_FreqCount.csv)
    - AERMET stage 3 message file (SFCUPAYY.ms3)
    - AERMET stage 3 output – profile file (SFCUPAYY.pfl)
    - AERMET stage 1 report file (SFCUPAYY.rp1)
    - AERMET stage 2 report file (SFCUPAYY.rp2)
    - AERMET stage 3 report file (SFCUPAYY.rp3)
    - AERMET stage 3 output – surface file (SFCUPAYY.sfc)
