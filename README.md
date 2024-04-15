# 📈 study_dataanalytics
- 수주 팀인, 속세팀의 데이터셋을 분석하는 개인프로젝트입니다.

## ☑ 사용기술

<img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=html5&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">


### 💻 DDA
<details>
  <summary>
    데이터 설명 및 분석가 의견
  </summary>
  
|no|Variable|Definition|Key|분석가 의견|
|--|--|--|--|--|
|1|_id|매물 각각에 대한 unique id||unique id이기에 유의미한 분석 불가|
|2|title|매물번호-매물 각각에 대한 unique id||상기동일|
|3|roomName|매물번호-매물 각각에 대한 unique id||상기동일, 위와 중복 데이터이므로 삭제|
|4|gender|매물의 성별구분 유무|공용|공용/여성전용/남성전용을 분리할 목적이었으나 '공용' 데이터만 있기에 열 삭제 가능|
|5|roomType|다인실 구분|'1인실', '그 외'|범주형 데이터 - 이후 숫자로 구분 필요|
|6|py|평수|1.99㎡~132㎡|명목형 데이터(string)이므로 ㎡ 삭제 후 float으로 변환 필요|
|7|deposit|매물의 보증금|10만원~3억만원|명목형 데이터(string)이므로 삭제 후 '만원'은 0000, '억만원'은 00000000로 변환 필요|
|8|rentFee|매물의 월세|12만원~280만원|명목형 데이터(string)이므로 '만원'을 0000으로 변환 필요|
|9|region|매물의 주소||범주형데이터|
|10|roomOption|매물의 옵션||명목형 데이터 - 옵션 별로 구분 필요
|11|url|매물 정보를 담고 있는 url||명목형데이터-유의미한 분석 불가


</details>

### 💻 EDA
<details>
  <summary>
    주요 분석 관점
  </summary>

#### 가설: 지역/평수와 월세/보증금 간에 상관 관계가 있을 것이다.
#### 설명: 지역과 평수마다 월세와 보증금 시세가 달라, 소비자마다 거주할 수 있는 최선의 지역이 있을 것이라고 예상된다. 

#### 1. 계약기간 별 월세/보증금 평균  
- 문제 정의: 서울의 구/동별 매물의 월세/보증금의 평균치를 계약기간 별로 도출한다.
- 배경: 월세/보증금의 평균치를 통해 고객의 n년 지출금액에 따라 지역을 추천하여, 고객의 매물 탐색 기간을 줄여 고객만족도를 높인다.
- 전제: py_cate ==1 or py_cate ==2 (py: 19.83-39.66 / 5.99-11.99평)인 경우 == 올라온 매물의 평수가 중위구간인 경우

#### 2. 평수/지역에 따른 월세/보증금 예측
- 문제 정의: 서울 매물의 평수/지역에 따라 월세/보증금을 예측한다.
- 배경: 고객이 매물을 구할 때 자산 및 월 수입에 따른 예상 금액을 도출하고, 그에 따른 맞춤형 매물을 추천함으로써, 고객 만족도를 높이고 매출 증대에 기여할 수 있다.

</details>


### 💻 CDA
<details>
  <summary>
    주요 분석 관점
  </summary>
  
- 지역별(범주) 매물의 평균 거주 비용(연속)의 차이가 있는지 분석
- 보증금(연속)에 따른 평균 월세(연속)의 차이가 있는지 분석 / 임의적으로 설정한 보증금구간(범주)에 따른 평균 월세구간(범주)의 차이가 있는지 분석 -> 어떤 데이터가 더 효과적일지 판단 

</details>


