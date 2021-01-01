---
description: ppt나 워드 같은 건가..? 그게 왜 필요하죠
---

# 문서란

소스 코드를 작성하는 프로그래머로서 문서라는 존재가 낯설게 다가올 수 있습니다. _이미 소스 코드에 다 써 놓았고, 주석도 달아 놓았는데 문서까지 써야 한다고? 뭐 어떻게 쓰는건데?_ 라고 생각하실 수 있습니다.

그런데 다르게 생각해 볼 수도 있습니다. 우리가 특정한 기능이 필요해서 구글에서 어떤 라이브러리를 찾았다고 해보겠습니다. 이 라이브러리를 사용하면 원하는 기능이 구현될 것은 알겠습니다. 그런데 설치는 어떻게 할하는지, 함수는 어떻게 호출해야 하는지, 반환값의 타입은 무엇인지는 모릅니다.

우리는 보통 구현 과정에서 구글과 구글이 안내해주는 수많은 블로그 포스트나 스택 오버플로의 답변들을 참고합니다. 그리고 이들은 모두 해당 소프트웨어의 **공식 문서**에 기반합니다. 구글 검색 없이 공식 문서 사이트로 들어가면 더 정확하고 빠르게 답을 얻을 수 있을 때도 있습니다.

이렇듯 우리는 늘 다른 사람들이 써놓은 문서의 도움을 받고 있습니다. 문서는 소스코드\(적게는 수천-많게는 수십만 줄\) 전체를 모두 해독하지 않고도 구현에 필요한 내용을 바로 알 수 있게 도와주는 존재입니다. _코드를 깔끔하게 쓰면 문서가 필요없지 않나?_ 라고 하실 수도 있습니다만, 아무리 깔끔하고 완벽하게 짜여진 라이브러리라도 문서가 없으면 쓰기 싫어지실 것입니다.

우리가 만약 소스 코드를 혼자 작성하고 혼자 사용하며, 그 소프트웨어가 사용되는 기간 동안 꾸준히 관리할 수 있고, 시간이 얼마가 지나든 소프트웨어의 모든 것을 전부 기억해낼 수 있다면 문서를 작성하지 않아도 됩니다. 하지만 그렇지 않은 경우, 서로를 위해 문서를 써 주세요. 아래는 우리가 문서를 반드시 작성해야 하는 경우입니다. 

* 1인 이상 참여하는 프로젝트
* 6개월 이상 작동해야 하는 소프트웨어를 만드는 프로젝트
* 널리 배포되어 실제로 소비자가 사용할 소프트웨어를 만드는 프로젝트
* 개발과 운영 과정을 통틀어 팀 인원이 변경될 가능성이 단 1%라도 있는 프로젝트

하나라도 포함된다면 문서를 써 주세요 :\)

> 기억해주세요, 소프트웨어 개발의 산출물은 소스 코드와 바이너리, 그리고 문서입니다.
