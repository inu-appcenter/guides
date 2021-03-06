---
description: 그래서 뭘 쓰면 되는데...?
---

# README 쓰기: 2부

`README.md`에는 다른 개발자가 궁금해할 만한 정보를 적어 주시면 됩니다.

* 소프트웨어 자체에 대한 정보 
* 소프트웨어 운용에 필요한 정보
* 소프트웨어 개발 환경을 설정하는 데에 필요한 정보

### 소프트웨어 자체에 대한 정보

서버 애플리케이션의 경우, 모바일 앱 또는 웹 프론트엔트 개발자는 서버 API를 궁금해할 것입니다. 그런 개발자를 위해 API 문서 또는 그 문서로 향하는 링크를 남겨 주세요.

{% hint style="info" %}
서버의 API 문서에는 다음 정보를 꼭 적어주세요.

* 메소드
* 경로
* 요청 및 응답 컨텐트 타입
* 요청 본문 및 쿼리 파라미터 규격
* 응답 코드 및 본문 규격
{% endhint %}

### 소프트웨어 운용에 필요한 정보

서버 애플리케이션을 배포하고 운영하는 사람은 배포 환경에 설정되어야 하는 환경변수나 인증 파일이 궁금할 것입니다. 이 또한 문서에 적어 주세요.

{% hint style="warning" %}
토큰이나 인증 파일과 같이 민감한 정보는 GitHub에 업로드하지 말아주세요!
{% endhint %}

### 소프트웨어 개발 환경을 설정하는 데에 필요한 정보

문서에는 현재 팀원 뿐만 아니라 **미래의 팀원**을 위한 이야기도 적혀 있어야 합니다. 소스 코드를 10분만 둘러 보면 바로 알 수 있는 것이 있지만, 그렇지 않은 것들도 있습니다. 특히 개발 환경과 빌드/실행 방법은 프로젝트를 둘러보는 것 만으로는 알기 어렵습니다.

예를 들어, `ndk`와 `cmake`을 사용해 안드로이드 앱을 개발한 후에, 그것들이 설치되어 있지 않은 머신에서 빌드를 시도하면 실패할 것입니다. 

또 다른 예시로, Node.js v14.13.0 이상부터 지원하는 [기능](https://nodejs.org/api/esm.html)을 프로젝트에서 사용한 경우, 비교적 최신 버전의 Node.js 없이는 예상대로 실행되지 않을 것입니다. 

개발 환경을 구축하는 데에 꼭 필요한 정보 또한 문서에 명시하여 주세요.

> 문서를 작성할 때에는 작성자와 독자 모두에게 가장 편한 언어를 사용해 주세요. [스택오버플로](https://meta.stackexchange.com/questions/13676/do-posts-have-to-be-in-english-on-stack-exchange)와 달리, 여기서는 굳이 영어를 쓸 필요가 없습니다. '_It is guaranteed to respond in a half second with 200 status code, representing the success body in JSON format: {"Result": "Success"}_' 보다는 '_0.5초 내에 JSON 형식의  {"Result": "Success"} 내용을 담은 200 응답이 옵니다._' 가 더 보기 편합니다.



