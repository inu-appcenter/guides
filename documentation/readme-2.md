---
description: 그래서 뭘 쓰면 되는데...?
---

# README 쓰기: 2부

`README.md`에는 다른 개발자가 궁금해할 만한 정보를 적어 주시면 됩니다.

예를 들어 서버 애플리케이션의 경우, 모바일 앱 또는 웹 프론트엔트 개발자는 서버 API를 궁금해할 것입니다. 그런 개발자를 위해 API 문서 또는 그 문서로 향하는 링크를 남겨 주세요. 서버 애플리케이션을 배포하고 운영하는 사람은 배포 환경에 설정되어야 하는 환경변수나 인증 파일이 궁금할 것입니다. 이 또한 문서에 적어 주세요.

문서에는 현재 팀원 뿐만 아니라 **미래의 팀원**을 위한 이야기도 적혀 있어야 합니다. 소스 코드를 10분만 둘러 보면 바로 알 수 있는 것이 있지만, 그렇지 않은 것들도 있습니다. 예를 들어, `ndk`와 `cmake`을 사용해 안드로이드 앱을 개발한 후에, 그것들이 설치되어 있지 않은 머신에서 빌드를 시도하면 실패할 것입니다. 개발에 처음 참여하는 팀원이 해당 sdk로 개발해 본 경험이 없다면 해결에 어려움을 겪을 것입니다.

문서를 작성할 때에는 작성자와 독자 모두에게 가장 편한 언어를 사용해 주세요. [스택오버플로](https://meta.stackexchange.com/questions/13676/do-posts-have-to-be-in-english-on-stack-exchange)와 달리, 여기서는 굳이 영어를 쓸 필요가 없습니다. 예를 들어, '_It is guaranteed to respond in a half second with 200 status code, representing the success body in JSON format: {"Result": "Success"}_' 보다는 '_0.5초 내에 JSON 형식의  {"Result": "Success"} 내용을 담은 200 응답이 옵니다.'_ 가 더 보기 편합니다.

