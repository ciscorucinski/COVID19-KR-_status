# 코로나19 한국 감염통계 CSV추출(시/도별, 일별, 전체 포함)
# COVID19 Korea Infection Statistics to CSV(including city/province, daily and total)

## 코로나19의 한국내 감염 데이터를 CSV형태로 만들어주는 파이썬 스크립트입니다. 목적에 맞도록 대충 짰습니다. 잘 굴러가긴 합니다. Python 3버전용입니다.
## This is small Python script that makes Corona 19's infection data in Korea in CSV format. It's a rough plan for the purpose. It's for Python 3.

### 1. 먼저 공공데이터 포털에 가입하여 하기 API Key를 받아주세요.
### 1. Please sign up for the PublicDataPortal(the Korean government site for public data) and receive the API key below.(site is in Korean)
### https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15043378

### 2. 소스의 11번째줄의 MY APK KEY에 받은 키를 넣어주세요
### 2. write your key on the MY APK KEY in the 11th row of the source file.

### 3. 실행하면 처음 데이터는 3월 3일부터 현재까지의 데이터를 한번에 받아오기 시작합니다.
### 3. When you run the script, the data will begin to be received at once from March 3rd to the present day.

### 4. 만들어진 covid19kr.txt를 엑셀로 열어서 다듬어서 쓰시면 됩니다.
### 4. Open the covid19kr.txt with excel and enjoy.

공공데이터 포털 매뉴얼을 보시면 아래처럼 다른 데이터도 뽑을 수 있으니. 참고하셔요. 대신 대소문자가 안맞는 경우가 많아서, 하나 대충 호출하셔서 XML파일을 보시고 명확하게 지정하시는 것이 좋습니다.
당장 확진자 누적수인 defCnt가 매뉴얼에는 DEF_CNT로 되어있습니다.

  resultCode	결과코드	2	1	00	결과코드
  resultMsg	결과메세지	50	1	NORMAL SERVICE	결과메시지
  numOfRows	한 페이지 결과 수	4	1	10	한 페이지당 표출 데이터 수
  pageNo	페이지 수	4	1	1	페이지 수
  totalCount	전체 결과 수	4	1	2	전체 결과 수
  SEQ	게시글번호(국내 시도별 발생현황 고유값)	30	1	1014	게시글번호(국내 시도별 발생현황 고유값)
  CREATE_DT	등록일시분초	30	1	2020-04-10 11:17:34.589	등록일시분초
  DEATH_CNT	사망자 수	15	1	0	사망자 수
  GUBUN	시도명(한글)	30	1	검역	시도명(한글)
  GUBUN_CN	시도명(중국어)	30	1	隔離區	시도명(중국어)
  GUBUN_EN	시도명(영어)	30	1	Lazaretto	시도명(영어)
  INC_DEC	전일대비 증감 수	15	1	4	전일대비 증감 수
  ISOL_CLEAR_CNT	격리 해제 수	15	1	349	격리 해제 수
  QUR_RATE	10만명당 발생률	30	1	-	10만명당 발생률
  STD_DAY	기준일시	30	1	2020년 04월 10일 00시	기준일시
  UPDATE_DT	수정일시분초 	30	1	null	수정일시분초 
  DEF_CNT	확진자 수	15	1	13561	확진자 수
  ISOL_ING_CNT	격리중 환자수	15	1	9	격리중 환자수
  OVER_FLOW_CNT	해외유입 수	15	1	14	해외유입 수
  LOCAL_OCC_CNT	지역발생 수 	15	1	7	지역발생 수 
