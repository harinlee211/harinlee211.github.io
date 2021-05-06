```python
#파이썬에 엑셀 데이터 불러오기 
import pandas as pd

kto_201901 =pd.read_excel('c:/ProgramData/datasalon-master/4_Tourists_Event/files/kto_201901.xlsx',
                         header=1, 
                         usecols ='A:G',
                         skipfooter=4)
kto_201901.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>아시아주</td>
      <td>765082</td>
      <td>10837</td>
      <td>1423</td>
      <td>14087</td>
      <td>125521</td>
      <td>916950</td>
    </tr>
    <tr>
      <th>1</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
    </tr>
    <tr>
      <th>2</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
    </tr>
    <tr>
      <th>3</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
    </tr>
    <tr>
      <th>4</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901.tail()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>62</th>
      <td>아프리카 기타</td>
      <td>768</td>
      <td>718</td>
      <td>90</td>
      <td>206</td>
      <td>908</td>
      <td>2690</td>
    </tr>
    <tr>
      <th>63</th>
      <td>기타대륙</td>
      <td>33</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>54</td>
    </tr>
    <tr>
      <th>64</th>
      <td>국적미상</td>
      <td>33</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>54</td>
    </tr>
    <tr>
      <th>65</th>
      <td>교포소계</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
    </tr>
    <tr>
      <th>66</th>
      <td>교포</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
    </tr>
  </tbody>
</table>
</div>




```python
#데이터탐색
kto_201901.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 67 entries, 0 to 66
    Data columns (total 7 columns):
     #   Column  Non-Null Count  Dtype 
    ---  ------  --------------  ----- 
     0   국적      67 non-null     object
     1   관광      67 non-null     int64 
     2   상용      67 non-null     int64 
     3   공용      67 non-null     int64 
     4   유학/연수   67 non-null     int64 
     5   기타      67 non-null     int64 
     6   계       67 non-null     int64 
    dtypes: int64(6), object(1)
    memory usage: 3.8+ KB
    


```python
kto_201901.describe()
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
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>67.00000</td>
      <td>67.000000</td>
      <td>67.000000</td>
      <td>67.000000</td>
      <td>67.000000</td>
      <td>67.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>26396.80597</td>
      <td>408.208955</td>
      <td>132.507463</td>
      <td>477.462687</td>
      <td>5564.208955</td>
      <td>32979.194030</td>
    </tr>
    <tr>
      <th>std</th>
      <td>102954.04969</td>
      <td>1416.040302</td>
      <td>474.406339</td>
      <td>2009.484800</td>
      <td>17209.438418</td>
      <td>122821.369969</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>16.000000</td>
      <td>54.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>505.00000</td>
      <td>14.500000</td>
      <td>2.500000</td>
      <td>17.500000</td>
      <td>260.000000</td>
      <td>927.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1304.00000</td>
      <td>45.000000</td>
      <td>14.000000</td>
      <td>43.000000</td>
      <td>912.000000</td>
      <td>2695.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>8365.00000</td>
      <td>176.500000</td>
      <td>38.000000</td>
      <td>182.000000</td>
      <td>2824.500000</td>
      <td>14905.500000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>765082.00000</td>
      <td>10837.000000</td>
      <td>2657.000000</td>
      <td>14087.000000</td>
      <td>125521.000000</td>
      <td>916950.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
condition = (kto_201901['관광']==0) | (kto_201901['상용']==0) | (kto_201901['공용']==0) |(kto_201901['유학/연수']==0)

kto_201901[condition]
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
    </tr>
    <tr>
      <th>20</th>
      <td>이스라엘</td>
      <td>727</td>
      <td>12</td>
      <td>0</td>
      <td>9</td>
      <td>57</td>
      <td>805</td>
    </tr>
    <tr>
      <th>22</th>
      <td>우즈베키스탄</td>
      <td>1958</td>
      <td>561</td>
      <td>0</td>
      <td>407</td>
      <td>2828</td>
      <td>5754</td>
    </tr>
    <tr>
      <th>38</th>
      <td>스위스</td>
      <td>613</td>
      <td>18</td>
      <td>0</td>
      <td>19</td>
      <td>97</td>
      <td>747</td>
    </tr>
    <tr>
      <th>45</th>
      <td>그리스</td>
      <td>481</td>
      <td>17</td>
      <td>4</td>
      <td>0</td>
      <td>273</td>
      <td>775</td>
    </tr>
    <tr>
      <th>46</th>
      <td>포르투갈</td>
      <td>416</td>
      <td>14</td>
      <td>0</td>
      <td>13</td>
      <td>121</td>
      <td>564</td>
    </tr>
    <tr>
      <th>51</th>
      <td>크로아티아</td>
      <td>226</td>
      <td>12</td>
      <td>0</td>
      <td>3</td>
      <td>250</td>
      <td>491</td>
    </tr>
    <tr>
      <th>54</th>
      <td>폴란드</td>
      <td>713</td>
      <td>10</td>
      <td>0</td>
      <td>27</td>
      <td>574</td>
      <td>1324</td>
    </tr>
    <tr>
      <th>59</th>
      <td>대양주 기타</td>
      <td>555</td>
      <td>3</td>
      <td>4</td>
      <td>0</td>
      <td>52</td>
      <td>614</td>
    </tr>
    <tr>
      <th>63</th>
      <td>기타대륙</td>
      <td>33</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>54</td>
    </tr>
    <tr>
      <th>64</th>
      <td>국적미상</td>
      <td>33</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>54</td>
    </tr>
    <tr>
      <th>65</th>
      <td>교포소계</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
    </tr>
    <tr>
      <th>66</th>
      <td>교포</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
    </tr>
  </tbody>
</table>
</div>




```python
#데이터 프레임에 기준년월 추가 
kto_201901['기준년월'] ='2019-01'
kto_201901.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>아시아주</td>
      <td>765082</td>
      <td>10837</td>
      <td>1423</td>
      <td>14087</td>
      <td>125521</td>
      <td>916950</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901['국적'].unique()
```




    array(['아시아주', '일본', '대만', '홍콩', '마카오', '태국', '말레이시아', '필리핀', '인도네시아',
           '싱가포르', '미얀마', '베트남', '인도', '스리랑카', '파키스탄', '방글라데시', '캄보디아', '몽골',
           '중국', '이란', '이스라엘', '터키', '우즈베키스탄', '카자흐스탄', 'GCC', '아시아 기타', '미주',
           '미국', '캐나다', '멕시코', '브라질', '미주 기타', '구주', '영국', '독일', '프랑스',
           '네덜란드', '스웨덴', '스위스', '이탈리아', '덴마크', '노르웨이', '벨기에', '오스트리아', '스페인',
           '그리스', '포르투갈', '핀란드', '아일랜드', '우크라이나', '러시아', '크로아티아', '루마니아',
           '불가리아', '폴란드', '구주 기타', '대양주', '오스트레일리아', '뉴질랜드', '대양주 기타',
           '아프리카주', '남아프리카공화국', '아프리카 기타', '기타대륙', '국적미상', '교포소계', '교포'],
          dtype=object)




```python
continents_list = ['아시아주','미주','구주','대양주', '아프리카주', '기타대륙','교포소계']
continents_list
```




    ['아시아주', '미주', '구주', '대양주', '아프리카주', '기타대륙', '교포소계']




```python
condition = (kto_201901.국적.isin(continents_list) ==False)
kto_201901_country =kto_201901[condition]
kto_201901_country['국적'].unique()
```




    array(['일본', '대만', '홍콩', '마카오', '태국', '말레이시아', '필리핀', '인도네시아', '싱가포르',
           '미얀마', '베트남', '인도', '스리랑카', '파키스탄', '방글라데시', '캄보디아', '몽골', '중국',
           '이란', '이스라엘', '터키', '우즈베키스탄', '카자흐스탄', 'GCC', '아시아 기타', '미국',
           '캐나다', '멕시코', '브라질', '미주 기타', '영국', '독일', '프랑스', '네덜란드', '스웨덴',
           '스위스', '이탈리아', '덴마크', '노르웨이', '벨기에', '오스트리아', '스페인', '그리스', '포르투갈',
           '핀란드', '아일랜드', '우크라이나', '러시아', '크로아티아', '루마니아', '불가리아', '폴란드',
           '구주 기타', '오스트레일리아', '뉴질랜드', '대양주 기타', '남아프리카공화국', '아프리카 기타',
           '국적미상', '교포'], dtype=object)




```python
kto_201901_country.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>5</th>
      <td>태국</td>
      <td>34004</td>
      <td>37</td>
      <td>199</td>
      <td>96</td>
      <td>6998</td>
      <td>41334</td>
      <td>2019-01</td>
    </tr>
  </tbody>
</table>
</div>




```python
#인덱스 재설정, 기존 데이터의 원래 번호 남아있음 
kto_201901_country_newindex = kto_201901_country.reset_index(drop =True)
kto_201901_country_newindex.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>34004</td>
      <td>37</td>
      <td>199</td>
      <td>96</td>
      <td>6998</td>
      <td>41334</td>
      <td>2019-01</td>
    </tr>
  </tbody>
</table>
</div>




```python
continents = ['아시아']*25 +['아메리카']*5 +['유럽']*23+['오세아니아']*3+['아프리카']*2+['기타대륙']+['교포']
print(continents)
```

    ['아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아시아', '아메리카', '아메리카', '아메리카', '아메리카', '아메리카', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '유럽', '오세아니아', '오세아니아', '오세아니아', '아프리카', '아프리카', '기타대륙', '교포']
    


```python
kto_201901_country_newindex['대륙']= continents
kto_201901_country_newindex.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
      <td>아시아</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
      <td>아시아</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
      <td>아시아</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
      <td>아시아</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>34004</td>
      <td>37</td>
      <td>199</td>
      <td>96</td>
      <td>6998</td>
      <td>41334</td>
      <td>2019-01</td>
      <td>아시아</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex.tail()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>55</th>
      <td>대양주 기타</td>
      <td>555</td>
      <td>3</td>
      <td>4</td>
      <td>0</td>
      <td>52</td>
      <td>614</td>
      <td>2019-01</td>
      <td>오세아니아</td>
    </tr>
    <tr>
      <th>56</th>
      <td>남아프리카공화국</td>
      <td>368</td>
      <td>9</td>
      <td>1</td>
      <td>6</td>
      <td>616</td>
      <td>1000</td>
      <td>2019-01</td>
      <td>아프리카</td>
    </tr>
    <tr>
      <th>57</th>
      <td>아프리카 기타</td>
      <td>768</td>
      <td>718</td>
      <td>90</td>
      <td>206</td>
      <td>908</td>
      <td>2690</td>
      <td>2019-01</td>
      <td>아프리카</td>
    </tr>
    <tr>
      <th>58</th>
      <td>국적미상</td>
      <td>33</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>54</td>
      <td>2019-01</td>
      <td>기타대륙</td>
    </tr>
    <tr>
      <th>59</th>
      <td>교포</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
      <td>2019-01</td>
      <td>교포</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex['관광객비율(%)'] = round(kto_201901_country_newindex['관광']/kto_201901_country_newindex['계']*100,1)
kto_201901_country_newindex.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>98.2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>97.5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>34004</td>
      <td>37</td>
      <td>199</td>
      <td>96</td>
      <td>6998</td>
      <td>41334</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>82.3</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex.sort_values(by='관광객비율(%)', ascending =False).head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>98.2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>97.5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.5</td>
    </tr>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.3</td>
    </tr>
    <tr>
      <th>55</th>
      <td>대양주 기타</td>
      <td>555</td>
      <td>3</td>
      <td>4</td>
      <td>0</td>
      <td>52</td>
      <td>614</td>
      <td>2019-01</td>
      <td>오세아니아</td>
      <td>90.4</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex.sort_values(by='관광객비율(%)', ascending =True).head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>59</th>
      <td>교포</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15526</td>
      <td>15526</td>
      <td>2019-01</td>
      <td>교포</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>방글라데시</td>
      <td>149</td>
      <td>126</td>
      <td>27</td>
      <td>97</td>
      <td>848</td>
      <td>1247</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>11.9</td>
    </tr>
    <tr>
      <th>12</th>
      <td>스리랑카</td>
      <td>157</td>
      <td>54</td>
      <td>5</td>
      <td>28</td>
      <td>1043</td>
      <td>1287</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>12.2</td>
    </tr>
    <tr>
      <th>13</th>
      <td>파키스탄</td>
      <td>238</td>
      <td>178</td>
      <td>10</td>
      <td>193</td>
      <td>413</td>
      <td>1032</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>23.1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>캄보디아</td>
      <td>635</td>
      <td>39</td>
      <td>55</td>
      <td>51</td>
      <td>1915</td>
      <td>2695</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>23.6</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex.pivot_table(values = '관광객비율(%)',
                                       index= '대륙',
                                       aggfunc='mean')
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
      <th>관광객비율(%)</th>
    </tr>
    <tr>
      <th>대륙</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>교포</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>기타대륙</th>
      <td>61.100000</td>
    </tr>
    <tr>
      <th>아메리카</th>
      <td>68.200000</td>
    </tr>
    <tr>
      <th>아시아</th>
      <td>59.624000</td>
    </tr>
    <tr>
      <th>아프리카</th>
      <td>32.700000</td>
    </tr>
    <tr>
      <th>오세아니아</th>
      <td>84.833333</td>
    </tr>
    <tr>
      <th>유럽</th>
      <td>63.826087</td>
    </tr>
  </tbody>
</table>
</div>




```python
condition =(kto_201901_country_newindex.국적 == '중국')
kto_201901_country_newindex[condition]
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>17</th>
      <td>중국</td>
      <td>320113</td>
      <td>2993</td>
      <td>138</td>
      <td>8793</td>
      <td>60777</td>
      <td>392814</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>81.5</td>
    </tr>
  </tbody>
</table>
</div>




```python
#전체 외국인 관광객 수
tourist_sum =sum(kto_201901_country_newindex['관광'])
tourist_sum
```




    884293




```python
tourist_sum =sum(kto_201901_country_newindex.관광)
tourist_sum
```




    884293




```python
kto_201901_country_newindex['전체 비율(%)']= round(kto_201901_country_newindex['관광']/tourist_sum*100,1)
kto_201901_country_newindex.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.3</td>
      <td>22.5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>98.2</td>
      <td>9.8</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.5</td>
      <td>3.9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>2506</td>
      <td>2</td>
      <td>0</td>
      <td>17</td>
      <td>45</td>
      <td>2570</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>97.5</td>
      <td>0.3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>34004</td>
      <td>37</td>
      <td>199</td>
      <td>96</td>
      <td>6998</td>
      <td>41334</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>82.3</td>
      <td>3.8</td>
    </tr>
  </tbody>
</table>
</div>




```python
kto_201901_country_newindex.sort_values('전체 비율(%)', ascending =False).head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>17</th>
      <td>중국</td>
      <td>320113</td>
      <td>2993</td>
      <td>138</td>
      <td>8793</td>
      <td>60777</td>
      <td>392814</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>81.5</td>
      <td>36.2</td>
    </tr>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>198805</td>
      <td>2233</td>
      <td>127</td>
      <td>785</td>
      <td>4576</td>
      <td>206526</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.3</td>
      <td>22.5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>86393</td>
      <td>74</td>
      <td>22</td>
      <td>180</td>
      <td>1285</td>
      <td>87954</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>98.2</td>
      <td>9.8</td>
    </tr>
    <tr>
      <th>25</th>
      <td>미국</td>
      <td>42989</td>
      <td>418</td>
      <td>2578</td>
      <td>229</td>
      <td>16523</td>
      <td>62737</td>
      <td>2019-01</td>
      <td>아메리카</td>
      <td>68.5</td>
      <td>4.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>34653</td>
      <td>59</td>
      <td>2</td>
      <td>90</td>
      <td>1092</td>
      <td>35896</td>
      <td>2019-01</td>
      <td>아시아</td>
      <td>96.5</td>
      <td>3.9</td>
    </tr>
  </tbody>
</table>
</div>




```python
def create_kto_data(yy,mm):
    file_path = 'c:/ProgramData/datasalon-master/4_Tourists_Event/files/kto_{}{}.xlsx'.format(yy,mm)
    
    df= pd.read_excel(file_path, header=1, skipfooter=4, usecols ='A:G')
    
    df['기준년월'] = '{}-{}'.format(yy,mm)
    
    ignore_list = ['아시아주','미주','구주','대양주', '아프리카주', '기타대륙','교포소계']
    condition = (df['국적'].isin(ignore_list)== False)
    df_country =df[condition].reset_index(drop= True)
    
    continents = ['아시아']*25 +['아메리카']*5 +['유럽']*23+['오세아니아']*3+['아프리카']*2+['기타대륙']+['교포']
    df_country['대륙'] = continents
    
    df_country['관광객비율(%)']=round(df_country.관광/df_country.계*100,1)
    
    tourist_sum = sum(df_country['관광'])
    df_country['전체 비율(%)']= round(df_country.관광/tourist_sum*100,1)
    
    return(df_country)

```


```python
kto_test = create_kto_data(2018, 12)
kto_test.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>252461</td>
      <td>1698</td>
      <td>161</td>
      <td>608</td>
      <td>3593</td>
      <td>258521</td>
      <td>2018-12</td>
      <td>아시아</td>
      <td>97.7</td>
      <td>22.7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>85697</td>
      <td>71</td>
      <td>22</td>
      <td>266</td>
      <td>1252</td>
      <td>87308</td>
      <td>2018-12</td>
      <td>아시아</td>
      <td>98.2</td>
      <td>7.7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>58355</td>
      <td>41</td>
      <td>3</td>
      <td>208</td>
      <td>939</td>
      <td>59546</td>
      <td>2018-12</td>
      <td>아시아</td>
      <td>98.0</td>
      <td>5.2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>6766</td>
      <td>0</td>
      <td>1</td>
      <td>20</td>
      <td>36</td>
      <td>6823</td>
      <td>2018-12</td>
      <td>아시아</td>
      <td>99.2</td>
      <td>0.6</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>47242</td>
      <td>42</td>
      <td>302</td>
      <td>58</td>
      <td>6382</td>
      <td>54026</td>
      <td>2018-12</td>
      <td>아시아</td>
      <td>87.4</td>
      <td>4.2</td>
    </tr>
  </tbody>
</table>
</div>




```python
for yy in range(2010,2020):
    for mm in range(1, 13):
        yymm = '{}{}'.format(yy,mm)
        print(yymm)
        
    
```

    20101
    20102
    20103
    20104
    20105
    20106
    20107
    20108
    20109
    201010
    201011
    201012
    20111
    20112
    20113
    20114
    20115
    20116
    20117
    20118
    20119
    201110
    201111
    201112
    20121
    20122
    20123
    20124
    20125
    20126
    20127
    20128
    20129
    201210
    201211
    201212
    20131
    20132
    20133
    20134
    20135
    20136
    20137
    20138
    20139
    201310
    201311
    201312
    20141
    20142
    20143
    20144
    20145
    20146
    20147
    20148
    20149
    201410
    201411
    201412
    20151
    20152
    20153
    20154
    20155
    20156
    20157
    20158
    20159
    201510
    201511
    201512
    20161
    20162
    20163
    20164
    20165
    20166
    20167
    20168
    20169
    201610
    201611
    201612
    20171
    20172
    20173
    20174
    20175
    20176
    20177
    20178
    20179
    201710
    201711
    201712
    20181
    20182
    20183
    20184
    20185
    20186
    20187
    20188
    20189
    201810
    201811
    201812
    20191
    20192
    20193
    20194
    20195
    20196
    20197
    20198
    20199
    201910
    201911
    201912
    


```python
for yy in range(2010,2020):
    for mm in range(1, 13):
        mm_str= str(mm).zfill(2)
        yymm = '{}{}'.format(yy,mm_str)
        print(yymm)
```

    201001
    201002
    201003
    201004
    201005
    201006
    201007
    201008
    201009
    201010
    201011
    201012
    201101
    201102
    201103
    201104
    201105
    201106
    201107
    201108
    201109
    201110
    201111
    201112
    201201
    201202
    201203
    201204
    201205
    201206
    201207
    201208
    201209
    201210
    201211
    201212
    201301
    201302
    201303
    201304
    201305
    201306
    201307
    201308
    201309
    201310
    201311
    201312
    201401
    201402
    201403
    201404
    201405
    201406
    201407
    201408
    201409
    201410
    201411
    201412
    201501
    201502
    201503
    201504
    201505
    201506
    201507
    201508
    201509
    201510
    201511
    201512
    201601
    201602
    201603
    201604
    201605
    201606
    201607
    201608
    201609
    201610
    201611
    201612
    201701
    201702
    201703
    201704
    201705
    201706
    201707
    201708
    201709
    201710
    201711
    201712
    201801
    201802
    201803
    201804
    201805
    201806
    201807
    201808
    201809
    201810
    201811
    201812
    201901
    201902
    201903
    201904
    201905
    201906
    201907
    201908
    201909
    201910
    201911
    201912
    


```python
df = pd.DataFrame()
```


```python
for yy in range(2010,2020):
    for mm in range(1, 13):
        temp= create_kto_data(str(yy),str(mm).zfill(2))
        df= df.append(temp, ignore_index=True)
```


```python
df.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>202825</td>
      <td>1750</td>
      <td>89</td>
      <td>549</td>
      <td>3971</td>
      <td>209184</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>97.0</td>
      <td>50.6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>35788</td>
      <td>41</td>
      <td>17</td>
      <td>37</td>
      <td>516</td>
      <td>36399</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>98.3</td>
      <td>8.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>13874</td>
      <td>55</td>
      <td>0</td>
      <td>21</td>
      <td>595</td>
      <td>14545</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>95.4</td>
      <td>3.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>554</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>554</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>100.0</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>13374</td>
      <td>39</td>
      <td>13</td>
      <td>53</td>
      <td>4335</td>
      <td>17814</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>75.1</td>
      <td>3.3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>202825</td>
      <td>1750</td>
      <td>89</td>
      <td>549</td>
      <td>3971</td>
      <td>209184</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>97.0</td>
      <td>50.6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>35788</td>
      <td>41</td>
      <td>17</td>
      <td>37</td>
      <td>516</td>
      <td>36399</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>98.3</td>
      <td>8.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>13874</td>
      <td>55</td>
      <td>0</td>
      <td>21</td>
      <td>595</td>
      <td>14545</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>95.4</td>
      <td>3.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>554</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>554</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>100.0</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>13374</td>
      <td>39</td>
      <td>13</td>
      <td>53</td>
      <td>4335</td>
      <td>17814</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>75.1</td>
      <td>3.3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.tail()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7195</th>
      <td>대양주 기타</td>
      <td>154</td>
      <td>2</td>
      <td>4</td>
      <td>0</td>
      <td>92</td>
      <td>252</td>
      <td>2019-12</td>
      <td>오세아니아</td>
      <td>61.1</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7196</th>
      <td>남아프리카공화국</td>
      <td>665</td>
      <td>3</td>
      <td>0</td>
      <td>3</td>
      <td>251</td>
      <td>922</td>
      <td>2019-12</td>
      <td>아프리카</td>
      <td>72.1</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>7197</th>
      <td>아프리카 기타</td>
      <td>1273</td>
      <td>644</td>
      <td>66</td>
      <td>93</td>
      <td>1002</td>
      <td>3078</td>
      <td>2019-12</td>
      <td>아프리카</td>
      <td>41.4</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>7198</th>
      <td>국적미상</td>
      <td>36</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>10</td>
      <td>47</td>
      <td>2019-12</td>
      <td>기타대륙</td>
      <td>76.6</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7199</th>
      <td>교포</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5281</td>
      <td>5281</td>
      <td>2019-12</td>
      <td>교포</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
for yy in range(2010,2020):
    for mm in range(1, 13):
        try:
            temp= create_kto_data(str(yy),str(mm).zfill(2))
            df= df.append(temp, ignore_index=True)
        except:
            pass
```


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 14400 entries, 0 to 14399
    Data columns (total 11 columns):
     #   Column    Non-Null Count  Dtype  
    ---  ------    --------------  -----  
     0   국적        14400 non-null  object 
     1   관광        14400 non-null  int64  
     2   상용        14400 non-null  int64  
     3   공용        14400 non-null  int64  
     4   유학/연수     14400 non-null  int64  
     5   기타        14400 non-null  int64  
     6   계         14400 non-null  int64  
     7   기준년월      14400 non-null  object 
     8   대륙        14400 non-null  object 
     9   관광객비율(%)  14400 non-null  float64
     10  전체 비율(%)  14400 non-null  float64
    dtypes: float64(2), int64(6), object(3)
    memory usage: 1.2+ MB
    


```python
df.to_excel('c:/ProgramData/datasalon-master/4_Tourists_Event/files/kto_total.xlsx', index=False)
```


```python
import pandas as pd
df = pd.read_excel('c:/ProgramData/datasalon-master/4_Tourists_Event/files/kto_total.xlsx')
df.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>202825</td>
      <td>1750</td>
      <td>89</td>
      <td>549</td>
      <td>3971</td>
      <td>209184</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>97.0</td>
      <td>50.6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>35788</td>
      <td>41</td>
      <td>17</td>
      <td>37</td>
      <td>516</td>
      <td>36399</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>98.3</td>
      <td>8.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>13874</td>
      <td>55</td>
      <td>0</td>
      <td>21</td>
      <td>595</td>
      <td>14545</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>95.4</td>
      <td>3.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>554</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>554</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>100.0</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>13374</td>
      <td>39</td>
      <td>13</td>
      <td>53</td>
      <td>4335</td>
      <td>17814</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>75.1</td>
      <td>3.3</td>
    </tr>
  </tbody>
</table>
</div>




```python
#그래프에서 한글을 표기하기 위한 코드, 붙여넣기해서 사용함
from matplotlib import font_manager, rc
import platform

if platform.system() == 'Windows':
    path ='c:/Windows/Fonts/malgun.ttf'
    font_name = font_manager.FontProperties(fname =path).get_name()
    rc('font', family =font_name)
elif platform.system() =='Darwin':
    rc('font',family='AppleGothic')
else:
    print('Check your OS system')
```


```python
import matplotlib.pyplot as plt
```


```python
condition = (df['국적']=='중국')
df_filter =df[condition]
df_filter.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>17</th>
      <td>중국</td>
      <td>40425</td>
      <td>11930</td>
      <td>55</td>
      <td>2751</td>
      <td>36091</td>
      <td>91252</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>44.3</td>
      <td>10.1</td>
    </tr>
    <tr>
      <th>77</th>
      <td>중국</td>
      <td>60590</td>
      <td>7907</td>
      <td>68</td>
      <td>29546</td>
      <td>42460</td>
      <td>140571</td>
      <td>2010-02</td>
      <td>아시아</td>
      <td>43.1</td>
      <td>13.6</td>
    </tr>
    <tr>
      <th>137</th>
      <td>중국</td>
      <td>50330</td>
      <td>13549</td>
      <td>174</td>
      <td>14924</td>
      <td>62480</td>
      <td>141457</td>
      <td>2010-03</td>
      <td>아시아</td>
      <td>35.6</td>
      <td>9.2</td>
    </tr>
    <tr>
      <th>197</th>
      <td>중국</td>
      <td>84252</td>
      <td>13306</td>
      <td>212</td>
      <td>2199</td>
      <td>47711</td>
      <td>147680</td>
      <td>2010-04</td>
      <td>아시아</td>
      <td>57.1</td>
      <td>15.5</td>
    </tr>
    <tr>
      <th>257</th>
      <td>중국</td>
      <td>89056</td>
      <td>12325</td>
      <td>360</td>
      <td>2931</td>
      <td>49394</td>
      <td>154066</td>
      <td>2010-05</td>
      <td>아시아</td>
      <td>57.8</td>
      <td>17.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.plot(df_filter['기준년월'],df_filter['관광'])
plt.show()
```


    
![png](output_39_0.png)
    



```python
plt.figure(figsize= (12,4))

plt.plot(df_filter['기준년월'],df_filter['관광'])

plt.title('중국 국적의 관광객 추이')
plt.xlabel('기준년월')
plt.ylabel('관광객수')

plt.xticks(['2010-01','2011-01','2012-01','2013-01','2014-01','2015-01','2016-01','2017-01','2018-01','2019-01'])

plt.show()
```


    
![png](output_40_0.png)
    



```python
cntry_list =['중국','일본','대만','미국','홍콩']
```


```python
for cntry in cntry_list:
    condition= (df['국적'] == cntry)
    df_filter =df[condition]
    
    plt.figure(figsize=(12,4))
    
    plt.plot(df_filter['기준년월'],df_filter['관광'])
    
    plt.title('{} 국적의 관광객 추이'.format(cntry))
    plt.xlabel('기준년월')
    plt.ylabel('관광객수')
    
    plt.xticks(['2010-01','2011-01','2012-01','2013-01','2014-01','2015-01','2016-01','2017-01','2018-01','2019-01'])

    plt.show()
```


    
![png](output_42_0.png)
    



    
![png](output_42_1.png)
    



    
![png](output_42_2.png)
    



    
![png](output_42_3.png)
    



    
![png](output_42_4.png)
    



```python
df['년도']=df['기준년월'].str.slice(0,4)
df['월']=df['기준년월'].str.slice(5,7)
df.head()
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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
      <th>년도</th>
      <th>월</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>일본</td>
      <td>202825</td>
      <td>1750</td>
      <td>89</td>
      <td>549</td>
      <td>3971</td>
      <td>209184</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>97.0</td>
      <td>50.6</td>
      <td>2010</td>
      <td>01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>대만</td>
      <td>35788</td>
      <td>41</td>
      <td>17</td>
      <td>37</td>
      <td>516</td>
      <td>36399</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>98.3</td>
      <td>8.9</td>
      <td>2010</td>
      <td>01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>홍콩</td>
      <td>13874</td>
      <td>55</td>
      <td>0</td>
      <td>21</td>
      <td>595</td>
      <td>14545</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>95.4</td>
      <td>3.5</td>
      <td>2010</td>
      <td>01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>마카오</td>
      <td>554</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>554</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>100.0</td>
      <td>0.1</td>
      <td>2010</td>
      <td>01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>태국</td>
      <td>13374</td>
      <td>39</td>
      <td>13</td>
      <td>53</td>
      <td>4335</td>
      <td>17814</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>75.1</td>
      <td>3.3</td>
      <td>2010</td>
      <td>01</td>
    </tr>
  </tbody>
</table>
</div>




```python
condition = (df['국적']=='중국')
df_filter =df[condition]
df_filter.head()

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
      <th>국적</th>
      <th>관광</th>
      <th>상용</th>
      <th>공용</th>
      <th>유학/연수</th>
      <th>기타</th>
      <th>계</th>
      <th>기준년월</th>
      <th>대륙</th>
      <th>관광객비율(%)</th>
      <th>전체 비율(%)</th>
      <th>년도</th>
      <th>월</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>17</th>
      <td>중국</td>
      <td>40425</td>
      <td>11930</td>
      <td>55</td>
      <td>2751</td>
      <td>36091</td>
      <td>91252</td>
      <td>2010-01</td>
      <td>아시아</td>
      <td>44.3</td>
      <td>10.1</td>
      <td>2010</td>
      <td>01</td>
    </tr>
    <tr>
      <th>77</th>
      <td>중국</td>
      <td>60590</td>
      <td>7907</td>
      <td>68</td>
      <td>29546</td>
      <td>42460</td>
      <td>140571</td>
      <td>2010-02</td>
      <td>아시아</td>
      <td>43.1</td>
      <td>13.6</td>
      <td>2010</td>
      <td>02</td>
    </tr>
    <tr>
      <th>137</th>
      <td>중국</td>
      <td>50330</td>
      <td>13549</td>
      <td>174</td>
      <td>14924</td>
      <td>62480</td>
      <td>141457</td>
      <td>2010-03</td>
      <td>아시아</td>
      <td>35.6</td>
      <td>9.2</td>
      <td>2010</td>
      <td>03</td>
    </tr>
    <tr>
      <th>197</th>
      <td>중국</td>
      <td>84252</td>
      <td>13306</td>
      <td>212</td>
      <td>2199</td>
      <td>47711</td>
      <td>147680</td>
      <td>2010-04</td>
      <td>아시아</td>
      <td>57.1</td>
      <td>15.5</td>
      <td>2010</td>
      <td>04</td>
    </tr>
    <tr>
      <th>257</th>
      <td>중국</td>
      <td>89056</td>
      <td>12325</td>
      <td>360</td>
      <td>2931</td>
      <td>49394</td>
      <td>154066</td>
      <td>2010-05</td>
      <td>아시아</td>
      <td>57.8</td>
      <td>17.0</td>
      <td>2010</td>
      <td>05</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_pivot =df_filter.pivot_table(values ='관광',
                               index='년도',
                               columns='월')
df_pivot
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
      <th>월</th>
      <th>01</th>
      <th>02</th>
      <th>03</th>
      <th>04</th>
      <th>05</th>
      <th>06</th>
      <th>07</th>
      <th>08</th>
      <th>09</th>
      <th>10</th>
      <th>11</th>
      <th>12</th>
    </tr>
    <tr>
      <th>년도</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2010</th>
      <td>40425</td>
      <td>60590</td>
      <td>50330</td>
      <td>84252</td>
      <td>89056</td>
      <td>87080</td>
      <td>122432</td>
      <td>142180</td>
      <td>93545</td>
      <td>107237</td>
      <td>75686</td>
      <td>58987</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>55070</td>
      <td>53863</td>
      <td>72003</td>
      <td>86397</td>
      <td>85668</td>
      <td>108060</td>
      <td>170524</td>
      <td>178937</td>
      <td>144704</td>
      <td>141824</td>
      <td>113856</td>
      <td>101605</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>106606</td>
      <td>74895</td>
      <td>110965</td>
      <td>166843</td>
      <td>154841</td>
      <td>179074</td>
      <td>258907</td>
      <td>268988</td>
      <td>203857</td>
      <td>204866</td>
      <td>155503</td>
      <td>148320</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>148118</td>
      <td>169395</td>
      <td>182850</td>
      <td>250549</td>
      <td>196306</td>
      <td>280319</td>
      <td>417991</td>
      <td>472005</td>
      <td>353359</td>
      <td>249850</td>
      <td>208175</td>
      <td>210950</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>230706</td>
      <td>219533</td>
      <td>313400</td>
      <td>429419</td>
      <td>410971</td>
      <td>429991</td>
      <td>540683</td>
      <td>588181</td>
      <td>423133</td>
      <td>459708</td>
      <td>381118</td>
      <td>345957</td>
    </tr>
    <tr>
      <th>2015</th>
      <td>327225</td>
      <td>413096</td>
      <td>386386</td>
      <td>536428</td>
      <td>517154</td>
      <td>223101</td>
      <td>172075</td>
      <td>372990</td>
      <td>453670</td>
      <td>518651</td>
      <td>409635</td>
      <td>381722</td>
    </tr>
    <tr>
      <th>2016</th>
      <td>456636</td>
      <td>424232</td>
      <td>500018</td>
      <td>601460</td>
      <td>614636</td>
      <td>671493</td>
      <td>823016</td>
      <td>747818</td>
      <td>611538</td>
      <td>588561</td>
      <td>452082</td>
      <td>456882</td>
    </tr>
    <tr>
      <th>2017</th>
      <td>489256</td>
      <td>458952</td>
      <td>263788</td>
      <td>158784</td>
      <td>172527</td>
      <td>181507</td>
      <td>207099</td>
      <td>226153</td>
      <td>229172</td>
      <td>244541</td>
      <td>223743</td>
      <td>260983</td>
    </tr>
    <tr>
      <th>2018</th>
      <td>236825</td>
      <td>237075</td>
      <td>281020</td>
      <td>283533</td>
      <td>284317</td>
      <td>303405</td>
      <td>332657</td>
      <td>360982</td>
      <td>326438</td>
      <td>382922</td>
      <td>327664</td>
      <td>345135</td>
    </tr>
    <tr>
      <th>2019</th>
      <td>320113</td>
      <td>324291</td>
      <td>369165</td>
      <td>410542</td>
      <td>413949</td>
      <td>395196</td>
      <td>439699</td>
      <td>451570</td>
      <td>432018</td>
      <td>476460</td>
      <td>426849</td>
      <td>433577</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
plt.figure(figsize=(16,10))

sns.heatmap(df_pivot, annot=True, fmt='.0f',cmap='rocket_r')
#(데이터를 지정, 히트맵 그래프에 실제값을 지정함, 숫자 형태를 소수점 없는 실수로, 그래프의 색 조합 지정)

plt.title('중국 관광객 히트맵')

plt.show()
```


    
![png](output_47_0.png)
    



```python
for cntry in cntry_list:
    condition =(df['국적']==cntry)
    df_filter =df[condition]
    
    df_pivot =df_filter.pivot_table(values ='관광',
                               index='년도',
                               columns='월')
    
    plt.figure(figsize=(16,10))

    sns.heatmap(df_pivot, annot=True, fmt='.0f',cmap='rocket_r')
#(데이터를 지정, 히트맵 그래프에 실제값을 지정함, 숫자 형태를 소수점 없는 실수로, 그래프의 색 조합 지정)

    plt.title('{} 관광객 히트맵'.format(cntry))

    plt.show()
```


    
![png](output_48_0.png)
    



    
![png](output_48_1.png)
    



    
![png](output_48_2.png)
    



    
![png](output_48_3.png)
    



    
![png](output_48_4.png)
    



```python

```
