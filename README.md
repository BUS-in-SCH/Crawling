## Crawling


### crawling함수
[서울메트로 사이버 메트로](http://www.seoulmetro.co.kr/kr/cyberStation.do?menuIdx=538) 지하철 시간표부분 크롤링  
crawling함수에 역코드를 입력해주면 결과값이 리턴된다.(ex. crawling(1408))

### 제공되는 정보
types : 열차의 종류(급행, 일반)  
times : 시간(시:분), 평일, 주말, 공유일이 시간순서  
weeks : 평일,주말, 공휴일  
destinations : 도착지(청량리행, 구로행, 천안행 등)  

- [역코드 검색](https://observablehq.com/@taekie/seoul_subway_station_coordinate)
	- 참고로 신창역은 1408

JSON으로 리턴되므로 JSON파싱해서 사용

