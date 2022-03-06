# Surfs Up

## Project Overview

### Purpose
I would like to open a Surf n’Shake shop serving surfboards and ice cream in Hawaii to locals and tourists. To get some financial supports from real investors, I reached out W. Avy who is famous for his love of surfing. W. Avy was satisfied with my current business plan but the weather raised extremely concern. As W. Avy's request, I will analyze on a weather dataset he has from the very island where I’d like to open my shop: the beautiful Oahu, mainly focusing on temperatire trends  

## Results
After run some analysis on temperature data for the months of June and December in Oahu, I can get the basic temperature statistic results for the two months.  

#### Temperature in June 
<p align="center">
 <img src="https://github.com/Jarviniazh/Module-9-Challenge-Surfs-Up/blob/main/Resources/june_temp.png?raw=true" alt="june_temp"/>
</p> 

1. There are 1,700 weather records of June from 2010 to 2017. And the average temperature during the seven years is 75°F.
2. The highest temperature in June is 85°F and the coldest weather is 64°F.
3. The standard deviation of temperature in June is 3.26, then we can get the coefficient of variation of temperature in June is 4.35% (std / mean * 100%), not a large number. In other word, the temperature trend in June does not fluctuate a lot.

#### Temperature in December

<p align="center">
 <img src="https://github.com/Jarviniazh/Module-9-Challenge-Surfs-Up/blob/main/Resources/dec_temp.png?raw=true" alt="dec_temp"/>
</p> 

1. There are 1,517 weather records of December from 2010 to 2016. And the average temperature during the six years is 71°F. Comparing other states, it is obviously a quite warm place to stay during the winter.
2. The warmest temperature in December is 83°F and the lowest weather is 56°F.
3. The standard deviation of temperature in December is 3.75, then we can get the coefficient of variation of temperature in December is 5.27%, still not a very large number. However, comparing with the temperature trend in June, variability of the temperature trend in December is a little bit larger.

## Summary
#### Conclusion
- According to the analysis, Oahu is a great choice for the surf and ice cream business. There is an enjoyable average temperature. Moreover, I analyzed the general temperature trends over the past seven years of June and December. The average weather in summer seems very stable. And though winter weather turned volatile since 2014, the average number also above 69°F. Meanwhile, the global warming impact the Oahu too, so the average temperature in June increase about 2°F (but still not too hot to stay) and 1°F in December. The more pleasant temperature. there will be enjoyable temperature for people to come and use the surf shop.
<p align="center">
 <img src="https://github.com/Jarviniazh/Module-9-Challenge-Surfs-Up/blob/main/Resources/Avg_tem_in_june%26dec.png?raw=true" alt="Avg_tem_in_june&26dec"/>
</p> 

- However, we should expect may serve less surfers than June because of the weather differences. Our business focus then should switch to tourist who come to spend their holidays with families.  

#### Recommendation
1. To better understand the weather in Oahu, we should also analyze the amount of precipitation. There needs to be enough rain to keep everything green, but not so much that we might lose out on that ideal surfing and ice cream weather. 
- **Precipitation in June**
 ```
 # The precipitation data of June
 june_prcp_results = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == "06").all()
 june_prcp_df = pd.DataFrame(june_prcp_results, columns=["June Precipitation"])
 june_prcp_df.describe()
 ```
<p align="center">
 <img src="https://github.com/Jarviniazh/Module-9-Challenge-Surfs-Up/blob/main/Resources/June_prcp.png?raw=true" alt="June_prcp"/>
</p> 

- **Precipitation in December**
 ```
 # The precipitation data of December
 dec_prcp_results = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == "12").all()
 dec_prcp_df = pd.DataFrame(dec_prcp_results, columns=["December Precipitation"])
 dec_prcp_df.describe()
 ```
 <p align="center">
  <img src="https://github.com/Jarviniazh/Module-9-Challenge-Surfs-Up/blob/main/Resources/dec_prcp.png?raw=true" alt="dec_prcp"/>
 </p> 
 
2. In addition, wind and wave also play a such significant role in surfing. If possible, we should get wind and wave data in Oahh to pick the best location for the Surf n’Shake shop. It will help W.Avy and I predict customer trends, as well as I could enjoy surfing. 
