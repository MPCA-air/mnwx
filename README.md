# mnwx
This R package retrieves and processes meteorological data for air modeling.


The following meteorological stations are available:

|call_sign |name                            |state |county      |years     | elevation_m|has_aerminute |upper_air_station             |
|:---------|:-------------------------------|:-----|:-----------|:---------|-----------:|:-------------|:-----------------------------|
|AXN       |Alexandria                      |MN    |Douglas     |2012-2016 |         432|Yes           |MPX - Chanhassen, MN          |
|*BRD       |Brainerd                        |MN    |Crow Wing   |2012-2016 |         372|Yes           |MPX - Chanhassen, MN          |
|DLH       |Duluth Int'l Arpt               |MN    |St. Louis   |2012-2016 |         435|Yes           |INL - International Falls, MN |
|**DYT       |Duluth Sky Harbor Arpt          |MN    |St. Louis   |2009-2013 |         186|No            |INL - International Falls, MN |
|FAR       |Fargo Int'l Arpt.               |ND    |Cass        |2012-2016 |         272|Yes           |ABR- Aberdeen, SD             |
|FCM       |Flying Cloud Arpt               |MN    |Scott       |2012-2016 |         276|Yes           |MPX - Chanhassen, MN          |
|FSD       |Sioux Falls Int'l Arpt          |SD    |Minnehaha   |2012-2016 |         433|Yes           |ABR- Aberdeen, SD             |
|GFK       |Grand Forks Int'l Arp't         |ND    |Grand Forks |2012-2016 |         255|Yes           |ABR- Aberdeen, SD             |
|HCO       |Hallock                         |MN    |Kittson     |2012-2016 |         249|No            |INL - International Falls, MN |
|*HIB       |Hibbing                         |MN    |St. Louis   |2012-2016 |         408|Yes           |INL - International Falls, MN |
|*INL       |International Falls             |MN    |Koochiching |2012-2016 |         353|Yes           |INL - International Falls, MN |
|LSE       |La Crosse                       |WI    |La Crosse   |2012-2016 |         292|Yes           |MPX - Chanhassen, MN          |
|MIC       |Crystal                         |MN    |Hennepin    |2012-2016 |         262|Yes           |MPX - Chanhassen, MN          |
|MJQ       |Jackson                         |MN    |Jackson     |2012-2016 |         439|No            |MPX - Chanhassen, MN          |
|MML       |Marshall                        |MN    |Lyon        |2012-2016 |         359|No            |MPX - Chanhassen, MN          |
|MSP       |Minneapolis/St. Paul Int'l Arpt |MN    |Hennepin    |2012-2016 |         256|Yes           |MPX - Chanhassen, MN          |
|OWA       |Owatonna                        |MN    |Steele      |2012-2016 |         344|No            |MPX - Chanhassen, MN          |
|*PKD       |Park Rapids                     |MN    |Hubbard     |2012-2016 |         439|Yes           |MPX - Chanhassen, MN          |
|RST       |Rochester                       |MN    |Olmsted     |2012-2016 |         396|Yes           |MPX - Chanhassen, MN          |
|RWF       |Redwood Falls                   |MN    |Redwood     |2012-2016 |         311|Yes           |MPX - Chanhassen, MN          |
|STC       |St. Cloud                       |MN    |Sherburne   |2012-2016 |         310|Yes           |MPX - Chanhassen, MN          |
|STP       |St. Paul Downtown Arpt          |MN    |Ramsey      |2012-2016 |         212|Yes           |MPX - Chanhassen, MN          |
|ULM       |New Ulm                         |MN    |Brown       |2012-2016 |         308|No            |MPX - Chanhassen, MN          |


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
