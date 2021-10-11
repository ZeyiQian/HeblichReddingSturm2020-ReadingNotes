## Reading Notes on HeblichReddingSturm2020   
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
The Quarterly Journal of Economics (2020), 2059–2133.

### Description
Using newly constructed spatially disaggregated data for London from 1801 to 1921, 
we show that the invention of the steam railway led to the first large-scale separation of workplace and residence. 
We show that a class of quantitative urban models is remarkably successful in explaining this reorganization of economic activity. 
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

![image](https://user-images.githubusercontent.com/91390400/134824649-e984df97-9ec3-4353-8a74-6391cdf7f100.png)

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

![image](https://user-images.githubusercontent.com/91390400/134824621-bd529c53-0021-400c-bbd5-fa4cbc3b4ae9.png)



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
    + sets of points connected to each transport network at time $t$ ： 
    
    $$\tilde{s}_t^{OR}，\tilde{s}_t^{UR}, \tilde{s}_t^{OT}$$ 
    
    (OR, UR, and OT indicate overground railways, underground railways, and omnibuses and trams,)
     
    +  vector of assumed travel time weights for each transport network by
    
    $$\mathbf{δ} = [1 \\ δ^{UR} \\ δ^{OT}\\ δ^{WA}]$$
    
    ( normalize the weight for overground railways to 1, and the superscript WA indicates walking)
    
    +  the bilateral travel times between boroughs n and i at time t as 
     
      $$d^W_{nit} = d^W_{nit}(\tilde{s}_t^{OR}，\tilde{s}_t^{UR}, \tilde{s}_t^{OT}, \mathbf{δ})$$, 
      where the superscript W indicates the weighting by transport mode

    +  use an instrumental variable based on bilateral travel times in which walking is assumed to be the only mode of transport, so that bilateral travel times depend solely on straight-line distance.
    +  bilateral travel times in the absence of other modes of transport by $d^S_{ni}$, where the superscript S is a mnemonic for straight-line distance


#### Historical Employment by Workplace and Commuting Data
*  Compare model’s historical predictions for workplace employment in Greater London with data on the “day population” of the City of London that are available from the day censuses of 1866, 1881, 1891, and 1911
*  Compare model’s predictions for commuting distances with historical commuting data based on the residence addresses of the employees of Henry Poole bespoke tailors, which has been located at the same workplace address in Savile Row in the City of Westminster since 1822

#### Data for Other Cities
*  historical data on population, employment,and commuting distances for Berlin, Paris, Boston, Chicago, New York, and Philadelphia

![image](https://user-images.githubusercontent.com/91390400/134824606-3e5d912f-66f3-4c59-b51a-69d7367eec0c.png)


### IV. REDUCED-FORM EVIDENCE

#### IV.A. City Size and Structure over Time
![image](https://user-images.githubusercontent.com/91390400/134824579-e9e30484-5e46-4d04-a3d0-5c903f2b75d9.png)
 *  Population is expressed as an index relative to its value in 1801 (such that 1801 = 1). 
 *  City of London: sharp drop in 1851 (FⅡ.Left)
 *  Greater London: grew substantially (FⅡ.Right)
 
![image](https://user-images.githubusercontent.com/91390400/134824582-e669cadc-0390-44a1-979f-0fd5b550e703.png)
 *  City of London’s residential (or “night”) population: day population > night population (FⅢ.Left)
 *  Steep decline in its night population from 1851 onward coincides with a sharp rise in its day population (FⅢ.Left)
 *  As this expansion occurs, and undeveloped land becomes developed, the share of already-developed land in overall land values tends to fall (FⅢ.Right)
 *  In the years after 1851 when the City of London experiences the largest declines in its residential population, its rateable value share increases from 9% to 11%. (FⅢ.Right)
 

![image](https://user-images.githubusercontent.com/91390400/134828359-ba11f54e-72dd-4dd5-9c1d-4e464fdc7285.png)
 *  A sharp rise in public transport journeys per head of population from around 7 in 1834 under 400 in 1921


![image](https://user-images.githubusercontent.com/91390400/134824586-1ef8c36d-e0a9-493c-b6f7-f78be91358a3.png)
*   Following the construction of the first railway in 1836, a sharp reduction in the City of London’s population-weighted average travel times to other boroughs (FⅣ.Left)
*   Employment by Residence < Workplace (FⅣ.Right)



#### IV.B. Difference-in-Differences Event-Study Specification

##### baseline specification
DID：  

$$log R_{jt} = α_j+\sum_{τ=−60 }^{τ=60}β_τ(S_j × I_{jτ})  +  (μ_j × Year_t)+ d_t + u_{jt} \qquad(1)$$

DDD：

$$log R_{jt} = α_j+\sum_{τ=−60 }^{τ=60}β_τ(S_j × I_{jτ}) +\sum_{τ=−30 }^{τ=30}β_τ(S_j × I_{jτ}× I_j^{Center}) +  (μ_j × Year_t)+ d_t + u_{jt} \qquad(2)$$

![image](https://user-images.githubusercontent.com/91390400/134829147-16533f95-7509-433b-ac7b-120cedf2cda5.png)

##### Results
*   DID：For central London and outer areas, the absolute value of the coefficient increases for 60 years after the railway is built. One of the reasons may be that the value of the connection to the railway network increases over time as the railway network expands
*   DDD：Reduced travel times increase the population of the suburbs of Greater London and decrease the population of the central areas.
 
### V. Theoretical Framework
The authors develop a dynamic model, in which adjustment costs for investments in durable building capital introduce gradual adjustment in response to changes in the transport network. The authors introduce these investments in durable building capital following the standard approach to *intertemporal saving and investment decisions* in Obstfeld and Rogoff (1996). Time is discrete and is indexed by $t$.

>##### Locations
The authors consider a city (Greater London) that is embedded within a wider economy (Great Britain). The economy as a whole consists of a discrete set of locations ($M$). Greater London comprises a subset of these locations $N \in M$. 

Locations are allowed to differ from one another in terms of their attractiveness for production and residence, as determined by productivity, amenities, the supply of floor space, and transport connections, where each of these location characteristics can evolve over time.

>##### Workers
The economy consists of two types of infinitely-lived agents: workers and landlords. Workers are assumed not to have access to a saving or borrowing technology and are modeled as “hand to mouth,” as in Kaplan and Violante (2014). Workers simultaneously choose their preferred residence $n$ and workplace $i$ given their idiosyncratic draws. And each worker chooses a residence-workplace pair either in Greater London or in the rest of the economy. 

Denote an exogenous continuous measure of workers in Great Britain by $L_{Mt}$. 

Denote the endogenous measure of workers who choose a residence-workplace pair in Greater London by $L_{Nt}$.



#### V.A. Preferences(worker)
>##### The intertemporal preferences of worker $ω$ living in residence $n$ and working in workplace $i$ at time $t$ are additive separable and isoelastic:

$$U_{nit}(\omega)=\sum_{s=t}^{\infty } \rho ^{s-t}\frac{U_{nit}(\omega)^{1-\frac{1}{\zeta} }}{1-\frac{1}{\zeta} } \qquad(F1)$$
where, $\zeta >0$ is the intertemporal elasticity of substitution;<br>
$ \rho$ is the subjective rate of time discount;<br>
$U_{nit}(\omega)$ is the worker’s instantaneous utility function.

>##### The instantaneous utility for worker $ω$ residing in location n and working in location i is :(in Cobb-Douglas functional form)

$$ U_{ni}(\omega)= \frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}} \left (\frac{C_{ni}(\omega ) }{\alpha}  \right )^{\alpha }  \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{1-\alpha }  \qquad(F2)$$

where,the authors suppress the time subscript from now on, except where important;   
$0<\alpha<1$;   
$B_{ni}$ captures amenities from the bilateral commute from residence n to workplace i that are common across all workers;   
$b_{ni}(\omega)$ is an idiosyncratic amenity draw that captures all the idiosyncratic factors that can cause an individual to live and work in particular locations in the city;   
$\kappa_{ni}$ is an iceberg commuting cost;  
$C_{ni}(\omega )$ is consumption of a single tradeable homogeneous final good;  
$H_{ni} (\omega )$ is consumption of residential floor space.



##### The utility maximization problem of workers is:
$$\max_{ C_{ni},H_{ni} }  U_{ni}(\omega)$$
$$subject \ to$$
$$P_nC_{ni}+Q_nH_{ni}= w_i $$ 
where,   
$P_n$ is the price index for consumption goods, which may include both tradeable and nontradeable consumption goods;   
$Q_n$ is the price of residential floor space;   
$w_i$ is the wage.   
*Note that without access to a savings or borrowing technology, workers choose their residence, workplace, consumption of the final and residential floor space use each period to maximize their instantaneous utility.*

Now, the Lagrange function is :
$$
\mathcal{L} = \frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}} \left (\frac{C_{ni}(\omega ) }{\alpha}  \right )^{\alpha }  \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{1-\alpha } + \lambda (w_i - P_nC_{ni}-Q_nH_{ni})$$

First Order Conditions:
$$\frac{\partial L}{\partial C_{ni}}=\frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}} \alpha \left ( \frac{C_{ni}}{\alpha}  \right )^{\alpha -1} \frac{1}{\alpha }  \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{1-\alpha }-\lambda P_n=0 $$

$$\frac{\partial L}{\partial H_{ni}}=\frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}}  \left ( \frac{C_{ni}}{\alpha}  \right )^{\alpha }(1-\alpha)  \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{-\alpha } \frac{1}{1-\alpha }-\lambda Q_n=0 $$

$$\frac{\partial L}{\partial \lambda}=w_i - P_nC_{ni}-Q_nH_{ni}=0 \qquad(F2.1) $$

rearrange them to get:
$$\frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}}  \left ( \frac{C_{ni}}{\alpha}  \right )^{\alpha -1}  \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{1-\alpha }=\lambda P_n \qquad(F2.2)$$

$$\frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}}  \left ( \frac{C_{ni}}{\alpha}  \right )^{\alpha } \left ( \frac{H_{ni} (\omega )}{1-\alpha }  \right )^{-\alpha } =\lambda Q_n \qquad(F2.3)$$

divided $(F2.2)$ by $(F2.3)$ to get:
$$\frac{C_{ni}^{\alpha -1}}{C_{ni}^\alpha } \frac{\alpha ^{1-\alpha }}{\alpha ^{-\alpha }} \frac{H_{ni}^{1-\alpha }}{H_{ni}^{-\alpha }}\frac{(1-\alpha) ^{\alpha-1 }}{(1-\alpha) ^{\alpha }} =\frac{P_n}{Q_n} $$
which can be simplified as:
$$\frac{\alpha }{(1-\alpha) }\frac{H_{ni}}{C_{ni}} =\frac{P_n}{Q_n} \qquad(F2.4)$$
$(F2.4)$ can be rewritten as:
$$H_{ni}=\frac{P_n}{Q_n}\frac{1-\alpha }{\alpha }C_{ni} \qquad(F2.5)$$

substituting $(F2.5)$ to $(F2.1)$ can get:

$$w_i - P_nC_{ni}-Q_n \left [ \frac{P_n}{Q_n}\frac{1-\alpha }{\alpha }C_{ni} \right ] =0 $$
rearrange them to get:
$$ C_{ni}= \frac{\alpha w_i }{P_n}\qquad(F2.6)$$

substituting $(F2.6)$ to $(F2.5)$ can get:
$$ H_{ni}= \frac{(1-\alpha) w_i }{Q_n} \qquad(F2.7)$$

Substituting $(F2.6)$ and $(F2.7)$ to $(F2)$ 
$$U_{ni}(\omega)= \frac{B_{ni}b_{ni}(\omega)}{k_{ni}} \left (\frac{\frac{\alpha w_i }{P_n} }{\alpha}  \right )^{\alpha }  \left ( \frac{\frac{(1-\alpha) w_i }{Q_n}}{1-\alpha }  \right )^{1-\alpha }$$

$$=\frac{B_{ni}b_{ni}(\omega)}{\kappa_{ni}}\frac{w_i^\alpha}{P_n^\alpha} \frac{w_i^{1-\alpha}}{Q_n^{1-\alpha}}$$
$$=\frac{B_{ni}b_{ni}(\omega)w_i}{\kappa_{ni}P_n^\alpha Q_n^{1-\alpha}} \qquad(3) $$
which is indirect utility for a worker $\omega$ residing in $n$ and working in $i$, and $0<\alpha<1$. 


>#### Distribution of Utility

##### Assume that idiosyncratic amenities $b_{ni}(\omega)$ are drawn from an independent extreme value (Fréchet) distribution for each residence-workplace pair and each worker:

$$ G(b)= e^{-b^{-\epsilon}} \qquad(4)$$
where, $\epsilon > 1$ is shape parameter, which controls the sensitivity of worker location decisions to economic variables;and the scale parameter is normalized to 1.

##### From the indirect utility function in equation (3), the utility($u$) also has Fréchet distribution. The *distribution of utility* for residence $n$ and workplace $i$ is:

$$ G_{ni}(u)=Pr[u_{ni}\le u ]$$
$$=Pr[\frac{B_{ni}b_{ni}(\omega)w_i}{\kappa_{ni}P_n^\alpha Q_n^{1-\alpha}}\le u]$$
$$=Pr[\frac{B_{ni}w_i}{\kappa_{ni}P_n^\alpha Q_n^{1-\alpha}} \frac{1}{u}  \le \frac{1}{b_{ni}(\omega)} ]$$
$$=Pr[\frac{\kappa_{ni}P_n^\alpha Q_n^{1-\alpha}}{B_{ni}w_i} u  \ge b_{ni}(\omega) ]$$
$$= e^{-\Psi_{ni}u^{-\epsilon }},$$
where $\Psi_{ni} = (B_{ni}w_i)^{\epsilon}(\kappa_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}$ is the location paremeter; $n \in N, i \in N$.

##### <!-- Since the maximum of a sequence of Fréchet distributed random variables is itself Fréchet distributde-->The distribution of utility across all residences $k$ and all workplaces $l$ is:

$$G_(u)=Pr[max(u_{ni})\le u ]$$
$$= \prod_{k}\prod_{l}e^{-\Psi_{kl}u^{-\epsilon }}$$
$$= e^{\sum_{k}\sum_{l} -\Psi_{kl}u^{-\epsilon }}$$
$$=e^{-\Psi_{M}u^{-\epsilon }}$$
where, $\Psi_{M} =\sum_{k}\sum_{l}\Psi_{kl}, k\in M \ and \ l\in M  $

<!--
#####From the indirect utility function in equation (3), the authors have the following monotonic relationship between idiosyncratic amenities $(b_{ni}(\omega))$ and utility $(U_{ni}(\omega))$:
$$ b_{ni}(\omega)= \frac{U_{ni}(\omega)k_{ni} P_n^\alpha Q_n^{1-\alpha}}{B_{ni}w_i} \qquad(3.1)$$

#####Together equations (4) and (3.1) imply that the *distribution of utility* for residence $n$ and workplace $i$ is:

$$G_{ni}(u)= e^{-\Psi_{ni}u^{-\epsilon }}, where \  \Psi_{ni} = (B_{ni}w_i)^{\epsilon}(k_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}  \ is\ the \ location \ paremeter.$$

Since the maximum of a sequence of Fréchet distributed random variables is itself Fréchet distributed, the distribution of utility across all residences $k$ and all workplaces $l$ is:

$$ G(u)= e^{-\Psi_{M}u^{-\epsilon }}, where \  \Psi_{M} =\sum_{k\in M}\sum_{l\in M}\Psi_{kl}   $$
-->
##### Given this Fréchet distribution for utility,the expected utility is:
$$ E(u)= \int_{0}^{\infty } uG'(u)du$$
$$=\int_{0}^{\infty }u(- \Psi_M )(-\epsilon u^{-\epsilon -1})e^{-\Psi_{M}u^{-\epsilon }}du$$
$$=\int_{0}^{\infty } \epsilon  \Psi_M u^{-\epsilon }e^{-\Psi_{M}u^{-\epsilon }}du$$

define $y=\Psi_M u^{-\epsilon }$, so $dy=-\epsilon \Psi_M u^{-\epsilon -1}du=-\epsilon \Psi_M u^{-\epsilon}u^{-1}du $, and $u =y^{-1/\epsilon}\Psi_M^{1/\epsilon} $
then,
$$E(u)= \int_{0}^{\infty }-u e^{-y} dy$$
$$?=\int_{0}^{\infty } - \Psi_M^{1/\epsilon} y^{-1/\epsilon}\Psi_M^{1/\epsilon} e^{-y}dy $$
which can be written as:
$$E(u)= \nu \Psi_M^{1/\epsilon}$$
$$E(u)= \nu [{\textstyle \sum_{k \in M}\sum_{l \in M}} (B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}]^{1/\epsilon}\qquad(C9)$$
where $ \nu = \Gamma(\frac{\epsilon-1}{\epsilon})$ is the Gamma function. In general, $\Gamma (a)=\int_{0}^{\infty } x^{a-1}e^{-x}dx$.


>#### Bilateral common amenities

$$ B_{ni} = B_n^R B_i^L B_{ni}^I \qquad(5)$$
where, $B_n^R, B_i^L, B_{ni}^I > 0$;<br>
$B_n^R$ is residence component common across all workplaces;<br>
$B_i^L$ is workplace component common across all residences;<br>
$ B_{ni}^I$ is idiosyncratic component (BnIi) specific to an individual residence-workplace pair.

>#### Residence and Workplace Choices

<!--
##### Using the distribution of utility for pairs of residence and employment locations, the probability that a worker chooses the bilateral commute from $n$ to $i$ out of all possible bilateral commutes is:

$$\lambda_{ni} = Pr[u_{ni} \ge max\left \{ u_{kl} \right \};\forall k,l ]$$
$$  = \int_{0}^{\infty } \prod_{l\ne i} G_{ni}(u)[\prod_{k\ne n}\prod_{l\in M} G_{kl}(u) ]d G_{ni}(u)$$
$$\int_{0}^{\infty } \prod_{k\in M}\prod_{l\in M} \epsilon \Psi_{ni}u^{-\epsilon-1}e^{-\Psi_{kl}u^{-\epsilon }}du $$
$$=\int_{0}^{\infty }  \epsilon \Psi_{ni}u^{-\epsilon-1}e^{-\Psi_{M}u^{-\epsilon }}du$$
-->

##### The probability that the worker chooses to live in location $n$ and work in location $i$ is:
$$\frac{L_{ni}}{L_M} =\frac{\Psi_{ni}}{\Psi_{M}} = \frac{(B_{ni}w_i)^{\epsilon}(k_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}}{ {\textstyle \sum_{k \in M}\sum_{l \in M}} (B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}} $$
where $L_{ni}$ is the measure of commuters from residence $n$ to workplace $i$; $L_M$ is the measure of workers in the economy as a whole.

##### Summing across workplaces and residences in Greater London, the probability that a worker chooses a residence-workplace pair in Greater London is given by:

$$\frac{L_{N}}{L_M} =\frac{{\textstyle \sum_{n \in N}\sum_{i \in N}}(B_{ni}w_i)^{\epsilon}(k_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}}{ {\textstyle \sum_{k \in M}\sum_{l \in M}} (B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}} $$

##### The probability that a worker chooses to live in location $n$ and work in location $i$ conditional on choosing a residence-workplace pair in Greater London is:

 $$ λ_{ni}=\frac{L_{ni}/L_M}{L_N/L_M} = \frac{L_{ni}}{L_N}= \frac{(B_{ni}w_i)^{\epsilon}(k_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}}{  \sum_{k \in N}\sum_{l \in N} (B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}}       \qquad(6)  \ \ i,n \in N$$ 

Summing across workplaces $i \in N$ to obtain the probability that a worker lives in residence $n \in N$, conditional on choosing a residence-workplace pair in Greater London:

$$\lambda_n^R =\frac{\sum_{i \in N}(B_{ni}w_i)^{\epsilon}(k_{ni} P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}}{\sum_{k \in N} \sum_{l\in N}(B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}} \qquad(7-1)$$

Summing across residences $n \in N$ to obtain the probability that a worker is employed in workplace $i \in N$, conditional on choosing a residence-workplace pair in Greater London:

$$ \lambda_n^R =\frac{\sum_{n\in N}(B_{ni}w_i)^{\epsilon}(k_{ni}P_n^\alpha Q_n^{1-\alpha})^{-\epsilon}}{\sum_{k \in N}\sum_{l \in N}(B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}} \qquad(7-2)$$

##### Expected utility conditional on choosing a residence-workplace pair is the same across all residence-workplace pairs in the economy:

$$\bar{U} = \nu [ \sum_{k \in N}\sum_{l \in N} (B_{kl}w_l)^{\epsilon}(k_{kl} P_k^\alpha Q_k^{1-\alpha})^{-\epsilon}]^{1/\epsilon} \qquad(8)$$
which is based on equation (C9).




### VI. Quantitative Analysis

#### VI.A Combined Land and Commuter Market Clearing
*  “Exact Hat Algebra” approach:Dekle, Eaton, and Kortum (2007), using rates of change rather than horizontal values to estimate the impact of changes in transport networks.
*  In particular, we rewrite our combined land and commuter market-clearing condition (16) for another year τ in terms of the values of variables in a
baseline year of t and the relative changes of variables between years τ and t.

$$ τ \neq t$$

Put（15）：
$$v_{n}=\sum_{i \in N} \lambda_{n i \mid n}^{R} w_{i}$$
into (16)：
$$ Q_{n}=Q_{n} H_{n}^{R}+q_{n} H_{n}^{L}=(1-\alpha)\left[\sum_{i \in N} \lambda_{n i \mid n}^{R} w_{i}\right] R_{n}+\frac{\beta^{H}}{\beta^{L}} w_{n} L_{n}$$
$$ ={Q}_{n t}=(1-\alpha) \cdot v_{n t} \cdot R_{n t}+\frac{\beta^{H}}{\beta^{L}} \cdot w_{n t} \cdot L_{n t}$$

$$ 
Q_{n}=Q_{n} H_{n}^{R}+q_{n} H_{n}^{L}=(1-\alpha)\left[\sum_{i \in N} \lambda_{n i \mid n}^{R} w_{i}\right] R_{n}+\frac{\beta^{H}}{\beta^{L}} w_{n} L_{n}=(1-\alpha)\ v_{n t}R_{n t}+\frac{\beta^{H}}{\beta^{L}}w_{n t}L_{n t}
$$

because 
$$\hat{x}_{n t}=\frac{x_{n \tau}}{x_{n}}$$

and α，β are constant.
So we have (17):
$$\hat{{Q}}_{n t} {Q}_{n t}=(1-\alpha) \hat{v}_{n t} v_{n t} \hat{R}_{n t} R_{n t}+\frac{\beta^{H}}{\beta^{L}} \hat{w}_{n t} w_{n t} \hat{L}_{n t} L_{n t}$$

According  (13), we have (18):

$$
\hat{L}_{i t} L_{i t}=\sum_{n \in N} {\lambda_{n i t \mid n}^{R} \hat{\lambda}_{n i t \mid n}^{R} \hat{R}_{n  t}R_{n t}} 
$$

$$
\hat{L}_{i t} L_{i t}=\sum_{n \in N} \frac{\lambda_{n i t \mid n}^{R} \hat{w}_{i t}^{\epsilon} \hat{\kappa}_{n i t}^{-\epsilon}}{\sum_{\ell \in N} \lambda_{n t t \mid n}^{R} \hat{w}_{\ell t}^{\epsilon} \hat{k}_{n \ell t}^{-\epsilon}} \hat{R}_{n t} R_{n t}
$$


where these equations include terms in changes in wages  and commuting costs but not in amenities, because we assume that the workplace and bilateral components of amenities are
constant 

$$
\hat{\mathcal{B}}_{i t}^{L}=\hat{\mathcal{B}}_{n i t}^{L}=1
$$

and changes in the residential component of amenities

$$
\hat{\mathcal{B}}_{n t}^{R}}\neq=1
$$

cancel from the numerator and denominator of the fractions


The same like (19):

$$
\hat{v}_{n t} v_{n t}=\sum i \in \mathbb{N} \frac{\lambda_{n i t \mid n}^{R} \hat{w}_{i t}^{\epsilon} \hat{\kappa}_{n i t}^{-\epsilon}}{\sum_{\ell \in \mathbb{N}} \lambda_{n \ell t \mid n}^{R} \hat{w}_{\ell t}^{\epsilon} \hat{\kappa}_{n \ell t}^{-\epsilon}} \hat{w}_{i t} w_{i t}
$$

Put (18) and (19) into (17), we have (20):
$$
\begin{aligned}
\hat{\mathbb{Q}}_{n t} \mathbb{Q}_{n t}=&(1-\alpha)\left[\sum_{i \in \mathbb{N}} \frac{\lambda_{n i t \mid n}^{R} \hat{w}_{i t}^{\epsilon} \hat{\kappa}_{n i t}^{-\epsilon}}{\sum_{\ell \in \mathbb{N}} \lambda_{n \ell t \mid n}^{R} \hat{w}_{\ell t}^{\epsilon} \hat{\kappa}_{n \ell t}^{-\epsilon}} \hat{w}_{i t} w_{i t}\right] \hat{R}_{n t} R_{n t} \\
&+\frac{\beta^{H}}{\beta^{L}} \hat{w}_{n t} w_{n t}\left[\sum_{i \in \mathbb{N}} \frac{\lambda_{i n t i}^{R} \hat{w}_{n t}^{\epsilon} \hat{\kappa}_{i n t}^{-\epsilon}}{\sum_{\ell \in \mathbb{N}} \lambda_{i \ell t \mid i}^{R} \hat{w}_{\ell t}^{\epsilon} \hat{\kappa}_{i \ell t}^{-\epsilon}} \hat{R}_{i t} R_{i t}\right]
\end{aligned}
$$

*  Suppose that we observe the values of all variables in the initial equilibrium in our baseline year of t
*  Suppose also that we observe relative changes in residents and rateable values between years τ and t.
*  Given these observed variables and known values for changes in commuting costs, this combined land and commuter market-clearing condition (20) provides a system of N equations that determines unique values for the N unknown relative changes in wages in each location.

##### LEMMA 1.. Suppose that 
$$
\left(\hat{Q}_{n t}, \hat{R}_{n t}, L_{n i t}, \lambda_{n i t \mid n}^{R}, Q_{n t}, v_{n t}, R_{n t}, w_{n t}, L_{n t}\right)
$$
are known. Given known values for model parameters 
$$
\left\{\alpha, \beta^{L}\right\left.\beta^{H}, \epsilon\right\}
$$

and the change in bilateral commuting costs
$$
\left(\hat{\kappa}_{n i t}^{-\epsilon}\right)
$$

, the combined land and commuter market-clearing condition (20) determines a unique vector of relative changes in wages
$$
\left(\hat{w}_{n t}\right)
$$
in each location.

*   Using these solutions for the relative changes in wages, we can immediately recover the unique relative change in employment
$$
\left(\hat{L}_{n t}\right)
$$
from the commuter market equilibrium condition(18). 
*   We can solve for the unique relative change inaverage per capita income by residence 
$$
\left(\hat{v}_{n t}\right)
$$
from equation (19).

*   Finally, we can obtain the unique relative change in commuting flows
$$
\left(\hat{L}_{n i t}\right)
$$
using the conditional commuting probabilities (14),we have (21):
$$
\hat{L}_{n i t} L_{n i t}=\frac{\lambda_{n i t \mid n}^{R} \hat{w}_{i t}^{\epsilon} \hat{\kappa}_{n i t}^{-\epsilon}}{\sum_{\ell \in \mathbb{N}} \lambda_{n \ell t \mid n}^{R} \hat{w}_{\ell t}^{\epsilon} \hat{\kappa}_{n \ell t}^{-\epsilon}} \hat{R}_{n t} R_{n t}
$$

##### Adventages
*   Not required to make assumptions about other determinants of economic activity
*   Observed probabilities control for unobserved differences in the level of bilateral commuting costs across residence-workplace pairs
