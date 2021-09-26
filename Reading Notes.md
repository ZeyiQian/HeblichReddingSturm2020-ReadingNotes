## Notes Title - HeblichReddingSturm2020   
## Instructor
Prof. Junfu Zhang
## Student
Li Shen  
Zeyi Qian  

## Reading Paper 
### Paper Title
THE MAKING OF THE MODERN METROPOLIS: EVIDENCE FROM LONDON

### Authors Name
STEPHAN HEBLICH  
STEPHEN J. REDDING  
DANIEL M. STURM  


### Publishing Time
The Quarterly Journal of Economics (2020), 2059–2133. doi:10.1093/qje/qjaa014.
Advance Access publication on May 7, 2020.

### Description
Using newly constructed spatially disaggregated data for London from 1801 to 1921, 
we show that the invention of the steam railway led to the first large-scale separation of workplace and residence. 
We show that a class of quantitative urban models is remarkably successful in explaining this reorganization of economic ac- tivity. 
We structurally estimate one of the models in this class and find substantial agglomeration forces in both production and residence. 
In counterfactuals, we find that removing the whole railway network reduces the population and the value of land and buildings 
in London by up to 51.5% and 53.3% respectively, and decreases net commuting into the historical center of London by more than 300,000 workers.


## Reading Notes
### Ⅰ. INTROUCTION

#### 1. Motivation：Huge commuting flows   vs.   Little knowledge about it's role in sustaining dense concentrations of economic activity
*  Impose substantial real resource costs in terms of time spent commuting and the construction of large networks of complex transportation infrastructure
*  Create commercial and residential areas, with their distinctive characteristics for production and consumption


#### 2. Historical events：Steam railways created in the mid-19th century


#### 3. Evidence for the positive effect of residential separation on agglomeration
*  Data set for Greater London during 1801-1921
*  Quantitative urban model


#### 4.Contribution：
*  Empirical estimation
    + Agglomeration effect：change of the relationship between travel time and distance as IV
*  Theoretical models
    + First, it proves that the urban models established by this paper all have the same land and commuter market clearing conditions, so reliable results can be obtained in such models, and a series of factors that have not been observed to determine the spatial distribution of the economy can be controlled. 
    + Second, a new structural estimation method is developed for such urban models that uses bilateral commuter flows from the base year (1921) and performs a comparative static analysis from that base year. This paper shows that the estimation procedure can be used to recover unobserved historical employment and commuting data from bilateral commuting data in the base year as well as historical data on population and land rents. 
    + Thirdly, paper shows that the urban model can quantitatively explain the spatial restructuring of economic activities in Greater London with the invention of steam railways.


### Ⅱ. BACKGROUND

#### Three geographical definitions of boundaries: F.1(A)
*  Greater London as defined by the Modern boundaries of the Greater London Authority (GLA) ：99 boroughs and 283 parishes
*  Historic County of London：29 boroughs and 183 parishes
*  The city of London： 111 parishes

      ![image](https://user-images.githubusercontent.com/91390400/134820433-d95f9211-6c7c-4971-a4aa-c4c3708e3908.png)

#### BC 43:London has a long history of settlement
#### In the early 19th century
*  Walking: about 3 miles per hour
*  Equestrian: about 6 miles per hour
*  Steam passenger rail: 21 miles per hour (rail development in London was carried out competitively by private companies)
#### In the first half of the 19th century
*  Public goods were largely provided by local parishes and gatekeepers
#### 1841: F.1(B)
*  First census year, there are only a few railway lines and the line density in central London county is relatively low.
#### 1881: F.1(C)
*  London county is crisscrossed by a dense railway network that extends further into the heart of the county.
#### 1921: F.1(D)
*  Density of overground and underground railway lines is further increased.


### Ⅲ. DATA

#### Bilateral Commuting：complete matrix of bilateral commuting flows between boroughs in Greater London
*  Closed commuting market：commuting flows between other parts of England and Wales and Greater London were small in 1921
*  Workplace employment-employment by workplace for each borough: summing across rows in the matrix of bilateral commuting flows for Greater London (come to this place)
*  Residence employment-employment by residence for each borough: summing across columns in the matrix of bilateral commuting flows for Greater London (leave this place) 
*  Employment participation rate for each borough in 1921: dividing residence employment by population 


#### Population by Residence
*  Population censuses of England and Wales from 1801-1891 was provided by the Cambridge Group for the History of Population and Social Structure (Cambridge Group)
1801，1811，1821，1831，1841，1851，1861，1871，1891（no 1881）
*  Population data from 1901-1921 stem from the Integrated Census Microdata Project (I-CeM).
*  Assuming that the ratio of residence employment to population is stable for a given borough over time
*  Use the 1921 value of this ratio and the historical population data to construct residence employment for earlier census years

#### Rateable Values
*  Measure the value of floor space using rateable values, which correspond to the annual flow of rent for the use of land and buildings
*  Equal the price times the quantity of floor space in the model
*  These rateable values cover all categories of property (except Crown property occupied by the Crown,Places for divine worship,Concerns listed under No. III Schedule A)
*  Rateable values data: 1815,1843,1847,1852,1860,1881,1896,1905,1911,1921
*  To create consistent spatial units over time, match parishes with the spatial units provided by the CGKO (Cambridge Group Kain Oliver) map
*  use area weights to create the same mappable units as for the population data-parish-level panel for the years 1815, 1843, 1848, 1852, 1860, 1881 and 1896
*  aggregate these parish data to the 1921 boroughs using area weights

      ![image](https://user-images.githubusercontent.com/91390400/134823058-8dd81a46-108b-40ad-a430-a76adfc98037.png)


#### Transport Network
*  GIS dataset on the transport network in Greater London over time using historical maps of the overground railway network, the underground railway network, and the omnibus and tram network, provided by the Cambridge Group for the History of Population and Social Structure, which based its digitization on Cobb (2003)
*  Measure bilateral travel times by distinguishing four transport networks based on the historical average travel speeds by transport mode in London reported in _London County Council (1907)_: 
    + (i) overgroundrailways (21 mph)
    + (ii) underground railways (15 mph)
    + (iii)omnibuses and trams (6 mph)
    + (iv) walking (3 mph)
*  Assumption 
    + workers follow the least-cost path in terms of travel time 
    + workers incur a travel time cost of 3 minutes when changing between modes of transport and can only connect to the railway network at railway stations
    + sets of points connected to each transport network at time _t_: s_t^OR，s_t^UR,s_t^OT  (OR, UR, and OT indicate overground railways, underground railways, and omnibuses and trams,)
    +  vector of assumed travel time weights for each transport network by δ = [1 δUR δOT δWA] ( normalize the weight for overground railways to 1, and the superscript WA indicates walking)
    +  the bilateral travel times between boroughs n and i at time t as dW ni $t = d_ni^W t(s_t^OR，s_t^UR,s_t^OT , δ)$, where the superscript W indicates the weighting by transport mode
    +  use an instrumental variable based on bilateral travel times in which walking is assumed to be the only mode of transport, so that bilateral travel times depend solely on straight-line distance.
    +  bilateral travel times in the absence of other modes of transport by d^S_ni, where the superscript S is a mnemonic for straight-line distance


#### Historical Employment by Workplace and Commuting Data
*  Compare model’s historical predictions for workplace employment in Greater London with data on the “day population” of the City of London that are available from the day censuses of 1866, 1881, 1891, and 1911
*  Compare model’s predictions for commuting distances with historical commuting data based on the residence addresses of the employees of Henry Poole bespoke tailors, which has been located at the same workplace address in Savile Row in the City of Westminster since 1822

#### Data for Other Cities
*  historical data on population, employment,and commuting distances for Berlin, Paris, Boston, Chicago, New York, and Philadelphia
![image](https://user-images.githubusercontent.com/91390400/134824040-b741edba-d401-48e9-9d16-3b15ed06abd6.png)



### IV. REDUCED-FORM EVIDENCE

#### IV.A. City Size and Structure over Time

#### IV.B. Difference-in-Differences Event-Study Specification



