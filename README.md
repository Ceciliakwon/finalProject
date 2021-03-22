# NETFLIX 추천 시스템 

## 기획 의도
- 신종 코로나바이러스 감염(코로나19) 여파로 사람들이 집에서 보내는 시간이 늘면서, 지난  1년간 온라인 스트리밍 서비스 수요가 대폭 증가함
- 대표적인 OTT 서비스 플랫폼인 NETFLIX에 등단코자 하는 신인 감독, 시나리오 작가, 영상 콘텐츠 제작사 등 관련 업계 종사자들에게 어떠한 형태, 어떤 장르의 영상을 제작하면 좋을지 방향성 제시

## 변수 설명 
- data : netflix_titles.csv
- title_c : 제목을 전처리한 후 담아놓은 리스트 변수
- html : 평점조회 URL를 들어가기 위해 필요한 제목의 고유번호를 얻기 위하여 크롤링하여 제목을 검색한 주소를 담아놓은 리스트 변수
- a : 크롤링한 영화의 고유번호를 담아놓은 리스트 변수
- All_star : 크롤링한 전체 평점을 담아놓은 리스트 변수 
- season : duration 컬럼안에 season으로 되어있는 것을 담아 놓은 리스트 변수
- time_min : 크롤링을 통해 얻은 1회당 평균시간을 담아놓은 리스트 변수
- rating : rating컬럼을 전처리하기 위한 함수
- all_genres : listed_in 컬럼을 전처리하기 위해 ',' 로 분리한 것을 담아 놓은 리스트 변수
- genres : 중복없는 all_genres의 값들
- zoer_matrix : 제로 매트릭스를 생성하기 위한 변수 
- dummies : listed_in을 원핫인코딩 하기 위한 더미변수
- data_joined : 원본데이터와 listed_in의 더미화 변수 dummies 합차기 위한 변수  
- country2 : country 컬럼에서 나라이름을 가져오기 위한 변수
- country_item : country2를 담기위한 리스트 변수
- ratings : 평점이 높은 작품들의 나라를 plotly 그래프로 그리기 위하여 만든 데이터프레임 변수 

- X : 독립변수, 전처리한 data중 All_star를 제외한 모든 컬럼
- y : 종속변수, 전처리한 data중 All_satr
- X_train_scaled : X_train을 Min-Max Normalization한 값
- X_test_scaled : X_test를 Min-Max Normalization한 값
- params : 최적의 하라미터를 구하기 위하여 파라미터를 조정할 변수
- KNN_clf : KNN 훈련 변수
- svm_clf : SVM 훈련 변수
- log_clf : LogisticRegression 훈련 변수
- cm : 정오표 변수 
- dt_clf : DecisionTree 훈련 변수 

