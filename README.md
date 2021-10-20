# munhwa_bigdata

문화관광 빅 데이터 분석대회(2020) 최우수상 수상작(http://www.tourbigdata.kr/award.asp)

주제 : 유사도 기반 국내 관광지 추천 시스템

## 사용 데이터

신한카드 데이터(카드 사용 로그)

"${여행지} + 여행"을 키워드로 검색한 네이버 블로그 포스팅 결과 크롤링

## 코드 설명

- [POS_konlpy.ipynb](https://github.com/GyuhoonK/munhwa_bigdata/blob/master/POS_konlpy.ipynb)
  - konlpy 패키지를 이용하여 형태소 분석 진행
- [Making_StopWords.ipynb](https://github.com/GyuhoonK/munhwa_bigdata/blob/master/Making_StopWords.ipynb)
  - 형태소 분석 결과를 바탕으로 불용어(stopword)를 결정

- [shinhan.ipynb](https://github.com/GyuhoonK/munhwa_bigdata/blob/master/shinhan.ipynb)
  - 여행소비(고객 거주지와 소비 장소가 다른 경우) 추출
  - 여행지별 소비 카테고리 비율 계산

- [tf_idf.ipynb](https://github.com/GyuhoonK/munhwa_bigdata/blob/master/tf_idf.ipynb)
  - 형태소 분석 이후 각 등장빈도 상위 250개 단어를 바탕으로 tf-idf matrix를 생성합니다
  - 여행지를 document, 단어를 term으로 취급하여 각 여행지에 벡터 부여
  - 각 여행지에 부여된 벡터를 바탕으로 K-means Clustering 적용
  - 여행지 소비 패턴 + 입력 여행지와 유사한 소비패턴을 보이는 비유명 여행지 추천, 추천근거 제시(소비패턴, 유사 키워드)

