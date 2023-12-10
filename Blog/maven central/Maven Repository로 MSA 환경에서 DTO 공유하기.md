maven central은 여러가지 dependency를 저장해 놓은 패키지 저장소이다. 프로젝트에 필요한 의존성을 import 하여 사용할 수 있다. 
## MSA 환경에서 Maven repository의 필요성 
MSA 환경에서는 DTO(Data Transfer Object)를 공유하게 되는 경우가 발생한다. 마이크로 서비스 간의 통신이나 이벤트 발생 시 데이터를 publish, consume 하는 경우 동일한 DTO를 사용해야 한다. 또한 여러 마이크로 서비스에서 공통으로 사용되는 로직이 존재한다면 maven repository를 사용해 한번의 수정으로 필요한 마이크로 서비스들에 적용할 수 있다. 
## Maven central 저장소 올리기 
maven repository를 생성하기 위해 먼저 Jira 이슈를 생성해야 한다. [sonatype](https://issues.sonatype.org/secure/Dashboard.jspa) 에 접속하여 시작한다. 
![[Screenshot 2023-12-10 at 03.55.57.png]]
위 이미지는 sonatype jira 페이지의 상단의 내용이다. OSSRH와 maven central을 위한 jira라고 한다. 
![[Screenshot 2023-12-10 at 03.57.31.png]]
상단에 `만들기` 버튼으로 jira 이슈를 생성한다. 프로젝트는 하나로 고정되어 있어 신경쓸 필요 없다. 
- 요약: jira title 
- 설명: 간단한 설명
- Group Id: io.github.<프로젝트 주소 도메인>
- project url: github repo url을 작성했다 
- scm url: 코드가 관리될 repo
- username: 사용자 이름 
위 정보를 입력하여 생성해주면 된다. 
몇 분 뒤 jira의 봇이 답변을 해준다. 답변을 잘 읽고 시키는 것을 따라하면 된다. 보통 이슈 번호에 맞는 repo를 생성하거나 group id를 수정하라고 한다. 
![[Screenshot 2023-12-10 at 04.04.42.png]]
repo를 생성하고 시키는 것을 완료하면 답변을 남겨준다. 답변은 아무렇게나 해도 괜찮은것 같다. 
![[Screenshot 2023-12-10 at 04.05.53.png]]
시키는 것을 잘 하면 위와 같이 축하와 함께 maven central에 릴리즈 할 수 있도록 공식 문서로 안내해준다. 이제 