# study_dataanalytics

## DDA
<details>
  <summary>
    DDA
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
