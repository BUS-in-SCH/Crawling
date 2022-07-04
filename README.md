## Crawling


### crawling함수
[서울메트로 사이버스테이션](http://www.seoulmetro.co.kr/kr/cyberStation.do?menuIdx=538) 지하철 시간표부분 크롤링  
crawling함수에 역코드를 입력해주면 결과값이 리턴된다.(ex. crawling(1408))

### real_time_subway_location 
[서울열린 데이터 광장 지하철 실시간 도착 정보](https://data.seoul.go.kr/dataList/OA-12764/F/1/datasetView.do) API 사용  
real_time_subway_location함수에 도착역을 입력하면 결과값이 리던 된다.(ex. real_time_subway_location(신창))



### 제공되는 정보

⭕ crawling
types : 열차의 종류(급행, 일반)  
times : 시간(시:분), 평일, 주말, 공유일이 시간순서  
weeks : 평일,주말, 공휴일  
destinations : 도착지(청량리행, 구로행, 천안행 등)  
- [역코드 검색](https://observablehq.com/@taekie/seoul_subway_station_coordinate)
	- 참고로 신창역은 1408

⭕ real_time_subway_location
updnline : 상행, 하행
bstatnNm : 도착역
cur_loc : 현재위치
arvlCd : 현재 열차의 상태(0:진입, 1:도착, 2:출발, 3:전역출발, 4:전역진입, 5:전역도착, 99:운행중)



JSON으로 리턴되므로 JSON파싱해서 사용
main_json함수로 저장되는데 main_json함수 호출  
- main_json함수에는 crawling, real_time_subway_location 두개가 같이 들어가 있음  
ex.) json.loads(main_json[1]) <br># 두번째 함수(real_time_subway_location) 호출</br>

