```python
import pandas as pd
import numpy as np
```


```python
a=pd.read_csv("Ecommerce Purchases")
```


```python
a
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Address</th>
      <th>Lot</th>
      <th>AM or PM</th>
      <th>Browser Info</th>
      <th>Company</th>
      <th>Credit Card</th>
      <th>CC Exp Date</th>
      <th>CC Security Code</th>
      <th>CC Provider</th>
      <th>Email</th>
      <th>Job</th>
      <th>IP Address</th>
      <th>Language</th>
      <th>Purchase Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16629 Pace Camp Apt. 448\nAlexisborough, NE 77...</td>
      <td>46 in</td>
      <td>PM</td>
      <td>Opera/9.56.(X11; Linux x86_64; sl-SI) Presto/2...</td>
      <td>Martinez-Herman</td>
      <td>6011929061123406</td>
      <td>02/20</td>
      <td>900</td>
      <td>JCB 16 digit</td>
      <td>pdunlap@yahoo.com</td>
      <td>Scientist, product/process development</td>
      <td>149.146.147.205</td>
      <td>el</td>
      <td>98.14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>9374 Jasmine Spurs Suite 508\nSouth John, TN 8...</td>
      <td>28 rn</td>
      <td>PM</td>
      <td>Opera/8.93.(Windows 98; Win 9x 4.90; en-US) Pr...</td>
      <td>Fletcher, Richards and Whitaker</td>
      <td>3337758169645356</td>
      <td>11/18</td>
      <td>561</td>
      <td>Mastercard</td>
      <td>anthony41@reed.com</td>
      <td>Drilling engineer</td>
      <td>15.160.41.51</td>
      <td>fr</td>
      <td>70.73</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Unit 0065 Box 5052\nDPO AP 27450</td>
      <td>94 vE</td>
      <td>PM</td>
      <td>Mozilla/5.0 (compatible; MSIE 9.0; Windows NT ...</td>
      <td>Simpson, Williams and Pham</td>
      <td>675957666125</td>
      <td>08/19</td>
      <td>699</td>
      <td>JCB 16 digit</td>
      <td>amymiller@morales-harrison.com</td>
      <td>Customer service manager</td>
      <td>132.207.160.22</td>
      <td>de</td>
      <td>0.95</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7780 Julia Fords\nNew Stacy, WA 45798</td>
      <td>36 vm</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_0 ...</td>
      <td>Williams, Marshall and Buchanan</td>
      <td>6011578504430710</td>
      <td>02/24</td>
      <td>384</td>
      <td>Discover</td>
      <td>brent16@olson-robinson.info</td>
      <td>Drilling engineer</td>
      <td>30.250.74.19</td>
      <td>es</td>
      <td>78.04</td>
    </tr>
    <tr>
      <th>4</th>
      <td>23012 Munoz Drive Suite 337\nNew Cynthia, TX 5...</td>
      <td>20 IE</td>
      <td>AM</td>
      <td>Opera/9.58.(X11; Linux x86_64; it-IT) Presto/2...</td>
      <td>Brown, Watson and Andrews</td>
      <td>6011456623207998</td>
      <td>10/25</td>
      <td>678</td>
      <td>Diners Club / Carte Blanche</td>
      <td>christopherwright@gmail.com</td>
      <td>Fine artist</td>
      <td>24.140.33.94</td>
      <td>es</td>
      <td>77.82</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9995</th>
      <td>966 Castaneda Locks\nWest Juliafurt, CO 96415</td>
      <td>92 XI</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Windows NT 5.1) AppleWebKit/5352 ...</td>
      <td>Randall-Sloan</td>
      <td>342945015358701</td>
      <td>03/22</td>
      <td>838</td>
      <td>JCB 15 digit</td>
      <td>iscott@wade-garner.com</td>
      <td>Printmaker</td>
      <td>29.73.197.114</td>
      <td>it</td>
      <td>82.21</td>
    </tr>
    <tr>
      <th>9996</th>
      <td>832 Curtis Dam Suite 785\nNorth Edwardburgh, T...</td>
      <td>41 JY</td>
      <td>AM</td>
      <td>Mozilla/5.0 (compatible; MSIE 9.0; Windows NT ...</td>
      <td>Hale, Collins and Wilson</td>
      <td>210033169205009</td>
      <td>07/25</td>
      <td>207</td>
      <td>JCB 16 digit</td>
      <td>mary85@hotmail.com</td>
      <td>Energy engineer</td>
      <td>121.133.168.51</td>
      <td>pt</td>
      <td>25.63</td>
    </tr>
    <tr>
      <th>9997</th>
      <td>Unit 4434 Box 6343\nDPO AE 28026-0283</td>
      <td>74 Zh</td>
      <td>AM</td>
      <td>Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_7...</td>
      <td>Anderson Ltd</td>
      <td>6011539787356311</td>
      <td>05/21</td>
      <td>1</td>
      <td>VISA 16 digit</td>
      <td>tyler16@gmail.com</td>
      <td>Veterinary surgeon</td>
      <td>156.210.0.254</td>
      <td>el</td>
      <td>83.98</td>
    </tr>
    <tr>
      <th>9998</th>
      <td>0096 English Rest\nRoystad, IA 12457</td>
      <td>74 cL</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_8;...</td>
      <td>Cook Inc</td>
      <td>180003348082930</td>
      <td>11/17</td>
      <td>987</td>
      <td>American Express</td>
      <td>elizabethmoore@reid.net</td>
      <td>Local government officer</td>
      <td>55.78.26.143</td>
      <td>es</td>
      <td>38.84</td>
    </tr>
    <tr>
      <th>9999</th>
      <td>40674 Barrett Stravenue\nGrimesville, WI 79682</td>
      <td>64 Hr</td>
      <td>AM</td>
      <td>Mozilla/5.0 (X11; Linux i686; rv:1.9.5.20) Gec...</td>
      <td>Greene Inc</td>
      <td>4139972901927273</td>
      <td>02/19</td>
      <td>302</td>
      <td>JCB 15 digit</td>
      <td>rachelford@vaughn.com</td>
      <td>Embryologist, clinical</td>
      <td>176.119.198.199</td>
      <td>el</td>
      <td>67.59</td>
    </tr>
  </tbody>
</table>
<p>10000 rows × 14 columns</p>
</div>



# 1) Display the top 10 row of dataset


```python
a.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Address</th>
      <th>Lot</th>
      <th>AM or PM</th>
      <th>Browser Info</th>
      <th>Company</th>
      <th>Credit Card</th>
      <th>CC Exp Date</th>
      <th>CC Security Code</th>
      <th>CC Provider</th>
      <th>Email</th>
      <th>Job</th>
      <th>IP Address</th>
      <th>Language</th>
      <th>Purchase Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16629 Pace Camp Apt. 448\nAlexisborough, NE 77...</td>
      <td>46 in</td>
      <td>PM</td>
      <td>Opera/9.56.(X11; Linux x86_64; sl-SI) Presto/2...</td>
      <td>Martinez-Herman</td>
      <td>6011929061123406</td>
      <td>02/20</td>
      <td>900</td>
      <td>JCB 16 digit</td>
      <td>pdunlap@yahoo.com</td>
      <td>Scientist, product/process development</td>
      <td>149.146.147.205</td>
      <td>el</td>
      <td>98.14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>9374 Jasmine Spurs Suite 508\nSouth John, TN 8...</td>
      <td>28 rn</td>
      <td>PM</td>
      <td>Opera/8.93.(Windows 98; Win 9x 4.90; en-US) Pr...</td>
      <td>Fletcher, Richards and Whitaker</td>
      <td>3337758169645356</td>
      <td>11/18</td>
      <td>561</td>
      <td>Mastercard</td>
      <td>anthony41@reed.com</td>
      <td>Drilling engineer</td>
      <td>15.160.41.51</td>
      <td>fr</td>
      <td>70.73</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Unit 0065 Box 5052\nDPO AP 27450</td>
      <td>94 vE</td>
      <td>PM</td>
      <td>Mozilla/5.0 (compatible; MSIE 9.0; Windows NT ...</td>
      <td>Simpson, Williams and Pham</td>
      <td>675957666125</td>
      <td>08/19</td>
      <td>699</td>
      <td>JCB 16 digit</td>
      <td>amymiller@morales-harrison.com</td>
      <td>Customer service manager</td>
      <td>132.207.160.22</td>
      <td>de</td>
      <td>0.95</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7780 Julia Fords\nNew Stacy, WA 45798</td>
      <td>36 vm</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_0 ...</td>
      <td>Williams, Marshall and Buchanan</td>
      <td>6011578504430710</td>
      <td>02/24</td>
      <td>384</td>
      <td>Discover</td>
      <td>brent16@olson-robinson.info</td>
      <td>Drilling engineer</td>
      <td>30.250.74.19</td>
      <td>es</td>
      <td>78.04</td>
    </tr>
    <tr>
      <th>4</th>
      <td>23012 Munoz Drive Suite 337\nNew Cynthia, TX 5...</td>
      <td>20 IE</td>
      <td>AM</td>
      <td>Opera/9.58.(X11; Linux x86_64; it-IT) Presto/2...</td>
      <td>Brown, Watson and Andrews</td>
      <td>6011456623207998</td>
      <td>10/25</td>
      <td>678</td>
      <td>Diners Club / Carte Blanche</td>
      <td>christopherwright@gmail.com</td>
      <td>Fine artist</td>
      <td>24.140.33.94</td>
      <td>es</td>
      <td>77.82</td>
    </tr>
    <tr>
      <th>5</th>
      <td>7502 Powell Mission Apt. 768\nTravisland, VA 3...</td>
      <td>21 XT</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; U; PPC Mac OS X 10_8_5...</td>
      <td>Silva-Anderson</td>
      <td>30246185196287</td>
      <td>07/25</td>
      <td>7169</td>
      <td>Discover</td>
      <td>ynguyen@gmail.com</td>
      <td>Fish farm manager</td>
      <td>55.96.152.147</td>
      <td>ru</td>
      <td>25.15</td>
    </tr>
    <tr>
      <th>6</th>
      <td>93971 Conway Causeway\nAndersonburgh, AZ 75107</td>
      <td>96 Xt</td>
      <td>AM</td>
      <td>Mozilla/5.0 (compatible; MSIE 7.0; Windows NT ...</td>
      <td>Gibson and Sons</td>
      <td>6011398782655569</td>
      <td>07/24</td>
      <td>714</td>
      <td>VISA 16 digit</td>
      <td>olivia04@yahoo.com</td>
      <td>Dancer</td>
      <td>127.252.144.18</td>
      <td>de</td>
      <td>88.56</td>
    </tr>
    <tr>
      <th>7</th>
      <td>260 Rachel Plains Suite 366\nCastroberg, WV 24...</td>
      <td>96 pG</td>
      <td>PM</td>
      <td>Mozilla/5.0 (X11; Linux i686) AppleWebKit/5350...</td>
      <td>Marshall-Collins</td>
      <td>561252141909</td>
      <td>06/25</td>
      <td>256</td>
      <td>VISA 13 digit</td>
      <td>phillip48@parks.info</td>
      <td>Event organiser</td>
      <td>224.247.97.150</td>
      <td>pt</td>
      <td>44.25</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2129 Dylan Burg\nNew Michelle, ME 28650</td>
      <td>45 JN</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_7...</td>
      <td>Galloway and Sons</td>
      <td>180041795790001</td>
      <td>04/24</td>
      <td>899</td>
      <td>JCB 16 digit</td>
      <td>kdavis@rasmussen.com</td>
      <td>Financial manager</td>
      <td>146.234.201.229</td>
      <td>ru</td>
      <td>59.54</td>
    </tr>
    <tr>
      <th>9</th>
      <td>3795 Dawson Extensions\nLake Tinafort, ID 88739</td>
      <td>15 Ug</td>
      <td>AM</td>
      <td>Mozilla/5.0 (X11; Linux i686; rv:1.9.7.20) Gec...</td>
      <td>Rivera, Buchanan and Ramirez</td>
      <td>4396283918371</td>
      <td>01/17</td>
      <td>931</td>
      <td>American Express</td>
      <td>qcoleman@hunt-huerta.com</td>
      <td>Forensic scientist</td>
      <td>236.198.199.8</td>
      <td>zh</td>
      <td>95.63</td>
    </tr>
  </tbody>
</table>
</div>



# 2) Display the last 10 row of dataset


```python
a.tail(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Address</th>
      <th>Lot</th>
      <th>AM or PM</th>
      <th>Browser Info</th>
      <th>Company</th>
      <th>Credit Card</th>
      <th>CC Exp Date</th>
      <th>CC Security Code</th>
      <th>CC Provider</th>
      <th>Email</th>
      <th>Job</th>
      <th>IP Address</th>
      <th>Language</th>
      <th>Purchase Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9990</th>
      <td>75731 Molly Springs\nWest Danielle, VT 96934-5102</td>
      <td>93 ty</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; Intel Mac OS X 10_7_4;...</td>
      <td>Pace, Vazquez and Richards</td>
      <td>869968197049750</td>
      <td>04/24</td>
      <td>877</td>
      <td>JCB 15 digit</td>
      <td>andersonmichael@sherman.biz</td>
      <td>Early years teacher</td>
      <td>54.170.3.185</td>
      <td>ru</td>
      <td>18.35</td>
    </tr>
    <tr>
      <th>9991</th>
      <td>PSC 8165, Box 8498\nAPO AP 60327-0346</td>
      <td>50 dA</td>
      <td>AM</td>
      <td>Mozilla/5.0 (compatible; MSIE 8.0; Windows NT ...</td>
      <td>Snyder Inc</td>
      <td>4221582137197481</td>
      <td>02/24</td>
      <td>969</td>
      <td>Voyager</td>
      <td>kking@wise-liu.com</td>
      <td>IT sales professional</td>
      <td>254.25.31.156</td>
      <td>el</td>
      <td>25.93</td>
    </tr>
    <tr>
      <th>9992</th>
      <td>885 Allen Mountains Apt. 230\nWallhaven, LA 16995</td>
      <td>40 vH</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; PPC Mac OS X 10_6_5) A...</td>
      <td>Wells Ltd</td>
      <td>4664825258997302</td>
      <td>10/20</td>
      <td>431</td>
      <td>Discover</td>
      <td>bberry@wright.net</td>
      <td>Set designer</td>
      <td>174.173.51.32</td>
      <td>de</td>
      <td>67.96</td>
    </tr>
    <tr>
      <th>9993</th>
      <td>7555 Larson Locks Suite 229\nEllisburgh, MA 34...</td>
      <td>72 jg</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_8...</td>
      <td>Colon and Sons</td>
      <td>30025560104631</td>
      <td>10/25</td>
      <td>629</td>
      <td>Maestro</td>
      <td>chelseawilliams@lopez.biz</td>
      <td>Designer, exhibition/display</td>
      <td>177.46.82.128</td>
      <td>el</td>
      <td>65.61</td>
    </tr>
    <tr>
      <th>9994</th>
      <td>6276 Rojas Hollow\nLake Louis, WY 56410-7837</td>
      <td>93 Ex</td>
      <td>PM</td>
      <td>Opera/9.68.(X11; Linux x86_64; sl-SI) Presto/2...</td>
      <td>Ritter-Smith</td>
      <td>3112186784121077</td>
      <td>01/25</td>
      <td>1823</td>
      <td>Maestro</td>
      <td>iroberts@gmail.com</td>
      <td>Education officer, museum</td>
      <td>242.44.112.18</td>
      <td>zh</td>
      <td>31.85</td>
    </tr>
    <tr>
      <th>9995</th>
      <td>966 Castaneda Locks\nWest Juliafurt, CO 96415</td>
      <td>92 XI</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Windows NT 5.1) AppleWebKit/5352 ...</td>
      <td>Randall-Sloan</td>
      <td>342945015358701</td>
      <td>03/22</td>
      <td>838</td>
      <td>JCB 15 digit</td>
      <td>iscott@wade-garner.com</td>
      <td>Printmaker</td>
      <td>29.73.197.114</td>
      <td>it</td>
      <td>82.21</td>
    </tr>
    <tr>
      <th>9996</th>
      <td>832 Curtis Dam Suite 785\nNorth Edwardburgh, T...</td>
      <td>41 JY</td>
      <td>AM</td>
      <td>Mozilla/5.0 (compatible; MSIE 9.0; Windows NT ...</td>
      <td>Hale, Collins and Wilson</td>
      <td>210033169205009</td>
      <td>07/25</td>
      <td>207</td>
      <td>JCB 16 digit</td>
      <td>mary85@hotmail.com</td>
      <td>Energy engineer</td>
      <td>121.133.168.51</td>
      <td>pt</td>
      <td>25.63</td>
    </tr>
    <tr>
      <th>9997</th>
      <td>Unit 4434 Box 6343\nDPO AE 28026-0283</td>
      <td>74 Zh</td>
      <td>AM</td>
      <td>Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_7...</td>
      <td>Anderson Ltd</td>
      <td>6011539787356311</td>
      <td>05/21</td>
      <td>1</td>
      <td>VISA 16 digit</td>
      <td>tyler16@gmail.com</td>
      <td>Veterinary surgeon</td>
      <td>156.210.0.254</td>
      <td>el</td>
      <td>83.98</td>
    </tr>
    <tr>
      <th>9998</th>
      <td>0096 English Rest\nRoystad, IA 12457</td>
      <td>74 cL</td>
      <td>PM</td>
      <td>Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_8;...</td>
      <td>Cook Inc</td>
      <td>180003348082930</td>
      <td>11/17</td>
      <td>987</td>
      <td>American Express</td>
      <td>elizabethmoore@reid.net</td>
      <td>Local government officer</td>
      <td>55.78.26.143</td>
      <td>es</td>
      <td>38.84</td>
    </tr>
    <tr>
      <th>9999</th>
      <td>40674 Barrett Stravenue\nGrimesville, WI 79682</td>
      <td>64 Hr</td>
      <td>AM</td>
      <td>Mozilla/5.0 (X11; Linux i686; rv:1.9.5.20) Gec...</td>
      <td>Greene Inc</td>
      <td>4139972901927273</td>
      <td>02/19</td>
      <td>302</td>
      <td>JCB 15 digit</td>
      <td>rachelford@vaughn.com</td>
      <td>Embryologist, clinical</td>
      <td>176.119.198.199</td>
      <td>el</td>
      <td>67.59</td>
    </tr>
  </tbody>
</table>
</div>



# 3) Check datatypes of each columns


```python
a.columns
```




    Index(['Address', 'Lot', 'AM or PM', 'Browser Info', 'Company', 'Credit Card',
           'CC Exp Date', 'CC Security Code', 'CC Provider', 'Email', 'Job',
           'IP Address', 'Language', 'Purchase Price'],
          dtype='object')




```python
a.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 10000 entries, 0 to 9999
    Data columns (total 14 columns):
     #   Column            Non-Null Count  Dtype  
    ---  ------            --------------  -----  
     0   Address           10000 non-null  object 
     1   Lot               10000 non-null  object 
     2   AM or PM          10000 non-null  object 
     3   Browser Info      10000 non-null  object 
     4   Company           10000 non-null  object 
     5   Credit Card       10000 non-null  int64  
     6   CC Exp Date       10000 non-null  object 
     7   CC Security Code  10000 non-null  int64  
     8   CC Provider       10000 non-null  object 
     9   Email             10000 non-null  object 
     10  Job               10000 non-null  object 
     11  IP Address        10000 non-null  object 
     12  Language          10000 non-null  object 
     13  Purchase Price    10000 non-null  float64
    dtypes: float64(1), int64(2), object(11)
    memory usage: 1.1+ MB
    


```python
a.dtypes
```




    Address              object
    Lot                  object
    AM or PM             object
    Browser Info         object
    Company              object
    Credit Card           int64
    CC Exp Date          object
    CC Security Code      int64
    CC Provider          object
    Email                object
    Job                  object
    IP Address           object
    Language             object
    Purchase Price      float64
    dtype: object



# 4)Check null values in the dataset


```python
a.isnull().sum()
```




    Address             0
    Lot                 0
    AM or PM            0
    Browser Info        0
    Company             0
    Credit Card         0
    CC Exp Date         0
    CC Security Code    0
    CC Provider         0
    Email               0
    Job                 0
    IP Address          0
    Language            0
    Purchase Price      0
    dtype: int64



# 5) How many rows & columns in our dataset


```python
a.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 10000 entries, 0 to 9999
    Data columns (total 14 columns):
     #   Column            Non-Null Count  Dtype  
    ---  ------            --------------  -----  
     0   Address           10000 non-null  object 
     1   Lot               10000 non-null  object 
     2   AM or PM          10000 non-null  object 
     3   Browser Info      10000 non-null  object 
     4   Company           10000 non-null  object 
     5   Credit Card       10000 non-null  int64  
     6   CC Exp Date       10000 non-null  object 
     7   CC Security Code  10000 non-null  int64  
     8   CC Provider       10000 non-null  object 
     9   Email             10000 non-null  object 
     10  Job               10000 non-null  object 
     11  IP Address        10000 non-null  object 
     12  Language          10000 non-null  object 
     13  Purchase Price    10000 non-null  float64
    dtypes: float64(1), int64(2), object(11)
    memory usage: 1.1+ MB
    


```python
a.shape
```




    (10000, 14)



# 5) Highest & lowest purchase prices


```python
a["Purchase Price"].max()
```




    99.99




```python
a["Purchase Price"].min()
```




    0.0




```python
a["Purchase Price"].sum()
```




    503473.02




```python
a["Purchase Price"].count()
```




    10000




```python
503473.02/10000
```




    50.347302



**Second way**


```python
a["Purchase Price"].sum()/len(a["Purchase Price"])
```




    50.347302



**Third way**


```python
a["Purchase Price"].mean()
```




    50.347302



# 6) How many people have french fr as their language


```python
len(a[a["Language"]=='fr'])
```




    1097



# 7) Job title contains engineer


```python
len(a[a["Job"].str.contains('engineer',case=False)])
```




    984



# 8) Find the email of the person with the following IP address:
132.207.160.22


```python
a[a["IP Address"]=="132.207.160.22"]["Email"]
```




    2    amymiller@morales-harrison.com
    Name: Email, dtype: object



# 9) How many people have mastercard as their credit card provider and made a purchase above 50?


```python
len(a[(a["CC Provider"]=="Mastercard") & (a["Purchase Price"]>50)])
```




    405



# 10) Find the email of the person with the following credit card number :¶
4664825258997302


```python
a[a["Credit Card"]==4664825258997302]["Email"]
```




    9992    bberry@wright.net
    Name: Email, dtype: object



# 11) How many purchase during the AM and How many purchase during the PM


```python
len(a[a["AM or PM"]=="AM"])
```




    4932




```python
len(a[a["AM or PM"]=="PM"])
```




    5068



**Second way**"



```python
a["AM or PM"].value_counts()
```




    PM    5068
    AM    4932
    Name: AM or PM, dtype: int64



# 12) How many people have credit card that expires in 2020? 


```python
len(a[a["CC Exp Date"].apply(lambda X:X[3:]=='20')])
```




    988




```python

```




    0       02/20
    1       11/18
    2       08/19
    3       02/24
    4       10/25
            ...  
    9995    03/22
    9996    07/25
    9997    05/21
    9998    11/17
    9999    02/19
    Name: CC Exp Date, Length: 10000, dtype: object



# 13) Top 5 most popular email service


```python
a['Email'].apply(lambda X:X.split('@')[1]).value_counts().head(5)
```




    hotmail.com     1638
    yahoo.com       1616
    gmail.com       1605
    smith.com         42
    williams.com      37
    Name: Email, dtype: int64




```python

```
