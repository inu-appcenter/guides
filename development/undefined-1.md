---
description: 모든 것은 이름값을 해야 합니다.
---

# 이름의 중요성

### 안 좋은 이름이 가진 문제들

다음과 같은 가상의 메소드가 있습니다.

```java
public String checkAdmin();
```

이 메소드는 DB의 `user` 테이블로부터 `name` 컬럼의 값이 클래스 필드의 `adminName`의 값과 같은 row를 찾아 존재하면 API 서버로 `/activateAdmin?name=admin` 요청을 보낸 뒤 `"YES"`를, 그렇지 않으면 `"NO"`를 반환합니다. 

이름과 파라미터, 반환 타입만 보고 어떤 일을 하는지 짐작하실 수 있나요? 만약 메소드가 아래와 같았다면 조금 더 이해하기 쉬웠을 것입니다.

```java
public boolean activateAdminIfUserIsAdmin(String userName);
```

위는 극단적인 예시였지만, 실제로 프로젝트 내에서 이러한 코드가 자주 발생합니다. 

다른 예시를 들어 보겠습니다. 

```javascript
return collection
    .filter((item) => !item.done)
    .map((item) => item.id)
```

주문 객체들이 담긴 배열에서 `done`이 `false`인\(=완료되지 않은\) 주문만 걸러낸 뒤 해당 주문들의 `id`만 추출해 반환하는 문입니다. 아래처럼 조금 다르게 쓸 수도 있습니다.

```javascript
return allOrders
    .filter((order) => !order.done)
    .map((completedOrder) => completedOrder.id)
```

이름에 약간의 변경만 가해주는 것으로 코드가 읽기 편해집니다.

우리가 코드를 작성할 때에 의존할 수 있는 정보는 많지 않습니다. 메소드의 파라미터와 반환 규격, 그리고 이름만 보고 해당 메소드를 사용해야 할 지 결정해야 할 때가 많습니다. 그런 상황에서 만약 메소드가 이름으로부터 기대되는 바와 다른 행동을 한다면 큰 문제로 이어질 수 있습니다.

어떠한 파일에 주어진 객체를 직렬화하여 기록하는 `writeFile(file, object)` 함수가 있다고 하겠습니다. 한 개발자가 두 객체를 파일에 순서대로 기록하기 위해 다음과 같이 호출했다고 하겠습니다.

```c
writeFile(recordFile, users[0]);
writeFile(recordFile, users[1]);
```

그런데 `writeFile`이 내부에서 파일 쓰기를 마친 뒤 파일을 닫아버리도록 구현되어 있었습니다. 따라서 두 번째 호출은 예외로 이어지게 됩니다. 이렇듯 이름에 나타나지 않은 [부작용\(side effect\)](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwiPhe2kq_vtAhWWH3AKHXgqCmQQFjAAegQIAhAC&url=https%3A%2F%2Fko.wikipedia.org%2Fwiki%2F%25EB%25B6%2580%25EC%259E%2591%25EC%259A%25A9_%28%25EC%25BB%25B4%25ED%2593%25A8%25ED%2584%25B0_%25EA%25B3%25BC%25ED%2595%2599%29&usg=AOvVaw0Hfpfl9LaCREUIy_IL1Xdh)은 실제 서비스 환경에서 예상치 못한 동작을 유발할 수 있습니다.

### 좋은 이름 짓기

클래스, 메소드, 함수, 변수의 이름은 스스로의 기능을 나타내야 합니다. 만약 이름이 길어지더라도 괜찮습니다. IDE의 자동완성 기능에 의존하더라도, 길고 명확한 이름을 쓰는 것이 짧고 불명확한 이름을 쓰는 것보다 낫습니다.

`tmp`, `check`, `flag`와 같은 모호한 이름은 최대한 피해야 합니다. `for` 루프 속의 인덱스를 나타내는 `i`와 같이 관습적으로 통용되는 경우가 아니라면 짧고 모호한 이름은 소스 코드를 알아보기 힘들게 합니다.

함수나 메소드는 항상 이름대로 행동해야 합니다. 즉, 이름과 다른 행동을 하면\(거짓말\) 안됩니다. `doA`라는 이름의 함수는 항상 `A`를 수행해야 합니다.

만약 메소드나 함수에 분기가 들어 있을 경우, 해당 내용까지 이름에 나타낼 수 있습니다. 선택적으로 `A`를 수행해야 하는 함수는 `doAIfNeeded`라고 이름 지을 수 있습니다. 이렇게 하면 해당 함수는 `A`를 수행할 수도 있고 그렇지 않을 수도 있지만, 두 경우 모두 이름으로부터 예상되는 동작이기 때문에 혼란을 피할 수 있습니다.

