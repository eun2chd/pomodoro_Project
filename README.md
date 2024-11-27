# 프로젝트명 : 뽀모도로 공부계획 웹페이지
## 기술 스택 
Front : HTML,CSS,JAVASCRIPT,Jquery<br/>
Back-end : nodejs, mysql<br/>
배포 : AWS<br/>
개발 기간 : 2주<br/>
* * *
뽀모도로 공부법은 학습뿐만 아니라 업무 등 다양한 작업에서 효율을 극대화하는 데 활용됩니다. <br/>
저희 앱은 이러한 다양한 작업 유형에 맞춰 사용자가 커스터마이징할 수 있도록 설계되었습니다.<br/>
# 주요 기능
시간을 효율적으로 관리할 수 있도록 직관적인 타이머 UI를 제공하며 뽀모도로 타이머 와 일반타이머 를 분리하여 사용자가 원하는 타이머로 공부를 진행할 수 있게끔 구현하였습니다."<br/>
사이클이 완료되면 알림음과 화면 알림으로 사용자에게 휴식 또는 집중 시간을 알려줍니다.<br/>
앱은 사용자의 집중 시간 데이터를 기록하여 일별/주별 통계를 제공합니다. 이를 통해 사용자는 자신의 학습 패턴을 분석하고 개선할 수 있습니다."<br/>
# 페이지별 기능 소개
1. 로그인 페이지 - 로그인 기능<br/>
2. 회원 가입 페이지 - 사용자 회원가입<br/>
   + 이메일 찾기<br/>
   + 비밀번호 바꾸기<br/>
3. 메인페이지 - 유저들 피드 작성 및 수정,삭제,좋아요,댓글 기능<br/>
4. 타이머 페이지 - 뽀모도로 타이머/일반 타이머 기능<br/>
5. 투두 리스트 페이지 - 해야할 일 목록 등록 달력으로 구현하여 해당 날짜에 어떤 일을 수행할 지 기록 / 해당 일정 클릭시 완료/미흡 으로 설정 기능<br/>
6. 마이 페이지 - 좋아요 한 피드목록 / 일정 / 공부 그래프 로 나의 일정을 확인가능<br/>
# 개발 과정과 목표
초기 아이디어는 팀원 중 한 명이 착안하였으며 개발 과정에서 사용자 경험(UX)을 최우선으로 고려하였습니다. 특히 간단한 인터페이스와 웹 기반 환경을 통해 누구나 설치나 복잡한 과정 없이 사용할 수 있도록 최적화하였습니다.<br/>
디자인적으로도 모바일과 PC 화면에 모두 적합하도록 반응형 디자인을 채택하여 다양한 환경에서 최상의 사용자 경험을 제공합니다.<br/>
# 기대 효과
뽀모도로 공부법의 활용은 사용자가 짧은 시간 동안 높은 집중력을 유지할 수 있도록 도와 생산성을 향상시킵니다. 장기적으로도 해야할 일 목록들을 추가하고 기록할 수 있어서 장기적인 성장과정을 한눈에 볼 수 있는 효과가 있습니다.<br/>
* * *
# 팀 구성 및 역할
### 5인 1조로 진행된 팀 프로젝트입니다.<br/>
# 저의 주요 역할<br/>
- 백엔드 처리 위주로 담당 DB 설계 및 메인페이지 API 설계 진행
- 메인페이지 피드 개발 담당
- 사용자가 오늘 하루 어떤 공부를 했는지 일상적인 피드 추가,삭제,수정 기능 구현
- 해당 피드에 대한 좋아요 기능 구현
* * *
# DB ERD
![최종ERD](https://github.com/user-attachments/assets/df0450e8-45da-44b1-8479-f2cf72a7cb6e)
1. Users 테이블 : 사용자 정보
2. Tasks 테이블 : 작업스케줄 관리
4. likes 테이블 : 좋아요한 피드목록
5. feeds 테이블 : 사용자가 글쓴 피드 정보
6. comment 테이블 : 해당 피드에 대한 댓글 정보
* * *
# 프로젝트 경험
### 피드 이미지 처리와 좋아요 기능 구현 경험
이번 프로젝트를 진행하면서 피드 이미지 처리를 어떻게 구현할지에 대해 많은 고민을 했습니다. 이미지를 데이터베이스에 직접 저장할 경우 이미지 파일의 크기가 제각각이고 사용자가 늘어날수록 DB에 큰 부담을 줄 수 있다고 판단했습니다.<br/>

이를 해결하기 위해 AWS S3 버킷을 활용하여 이미지를 저장하고 해당 이미지의 경로값만 데이터베이스에 저장하는 방식으로 구현해보았습니다. 이 접근 방식을 성공적으로 구현하면서 파일 스토리지와 데이터베이스를 효율적으로 연계하는 방법을 배울 수 있었습니다.

또한 프로젝트 중간에 좋아요 기능을 구현할 때 예상보다 복잡한 로직이 필요하다는 것을 깨달았습니다. 단순히 좋아요 버튼을 누르고 취소하는 기능만이 아니라 해당 사용자가 이전에 좋아요를 누른 상태인지 혹은 취소한 후 다시 누른 경우까지 다양한 상태를 고려해야 했습니다. 이로 인해 다양한 상황에 대한 예외 처리를 고민하고 구현하면서 작은 기능 하나를 완성하기 위해서도 세심한 설계와 구현이 필요하다는 것을 느꼈습니다.

추가적으로 좋아요 기능 구현 과정에서 코드를 효율적으로 작성할 방법이나 중복을 줄일 수 있는 최적화 방법에 대해서도 고민하게 되었습니다. 이러한 과정은 단순히 기능 구현을 넘어 효율적인 코드 작성에 대한 인사이트를 얻게 해준 값진 경험이었습니다.

마지막으로 이번 프로젝트를 통해 서버와 클라이언트 간 데이터 주고받는 흐름을 더 깊이 이해하게 되었고 페이지 오류 처리 능력도 함께 길렀습니다. 백엔드 개발자로서 한 단계 성장할 수 있었던 중요한 프로젝트였다고 생각합니다.

# 페이지 주소
http://52.78.68.95/

# 개발과정 
### 노션 URL
https://glitter-scourge-249.notion.site/pomo-1343cb019cd480e2a585f0dfa8ace4b2?pvs=4
* * *
# 부족한점
### 부족한 점 및 개선 방향
1. 타이머 시간 설정<br/>
현재 상태: 타이머 시간이 고정되어 있음.<br/>
개선 방향: 사용자가 직접 타이머 시간을 설정할 수 있도록 입력 필드나 설정 화면을 추가. <br/>
추가 아이디어: 추천 타이머 설정(예: 25분, 50분 등)을 제공하여 사용성을 높임.<br/>
2. 뽀모도로 소개 및 기능 설명<br/>
현재 상태: 로고가 직관적이지 않으며, 기능 설명이 부족.<br/>
개선 방향:<br/>
첫 접속 화면에 간략한 캐치프레이즈와 뽀모도로 방법에 대한 1~2줄 설명 추가.<br/>
주요 기능(타이머, 투두리스트, 성취감 피드백 등)을 요약한 소개 섹션 배치.<br/>
3. PC와 모바일 간 UI 차별화 부족<br/>
현재 상태: PC 사용 시 UI가 불편.<br/>
개선 방향:<br/>
PC와 모바일에 따라 레이아웃을 최적화하는 반응형 디자인 구현.<br/>
PC에서는 타이머와 투두리스트를 동시에 볼 수 있는 넓은 화면 배치 고려.<br/>
4. 홈 탭의 정체성과 차별성 부족<br/>
현재 상태: 피드가 일반적인 SNS처럼 느껴짐.<br/>
개선 방향:<br/>
뽀모도로와 연계된 성취감을 부여하는 기능 추가(예: 목표 달성 인증, 통계 대시보드)<br/>
사용자에게 성취감을 제공하는 UI(뱃지, 목표 달성 알림) 디자인 추가<br/>
5. 버튼 색상 및 디자인 개선<br/>
현재 상태: 버튼 색상이 일관되지 않음. 토마토 컨셉과 다소 어울리지 않는 컬러 사용<br/>
개선 방향:<br/>
버튼 컬러를 통일하여 붉은색 계열 중심으로 조정.<br/>
"확인" 버튼은 강조색(붉은색), "취소"는 중립색(옅은 회색)으로 설정.<br/>
안내 메시지 및 텍스트 정렬을 가운데로 조정.<br/>
6. 기능적 문제<br/>
로그인 관련 문제:<br/>
현재 상태: 로그인 후에도 로그인 페이지로 이동 가능.<br/>
개선 방향: 로그인 상태 확인 후 로그인 페이지 접근을 차단.<br/>
로그아웃 기능 추가.<br/>
투두리스트 달력:<br/>
일정이 있는 날을 시각적으로 표시.<br/>
타이머와 일정 연동:<br/>
일정 시간에 자동으로 타이머가 시작되는 기능 추가.<br/>
7. 차별점 부족<br/>
현재 상태: 기존 뽀모도로 타이머들과의 차별성이 명확하지 않음.<br/>
개선 방향:<br/>
업무와 휴식의 1사이클을 한 화면에서 직관적으로 확인할 수 있도록 UI 재구성.<br/>
사용자 습관을 학습하여 개인 맞춤형 타이머 추천(예: 휴식 시간 제안).<br/>
8. 기술적 오류<br/>
PC 화면에서 레이아웃 오류:<br/>
현재 상태: 타이머 시계 변경 시 레이아웃이 틀어짐.<br/>
개선 방향: 다양한 화면 크기에서 레이아웃이 안정적으로 보이도록 CSS 수정.<br/>
휴식 타이머 없음:<br/>
개선 방향: 업무와 휴식을 분리한 두 가지 타이머 추가.<br/>






















