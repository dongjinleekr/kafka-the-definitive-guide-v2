1쇄 정오표 (최종 업데이트: 2024년 6월 2일)

|쪽  |수정 전                                                                   |수정 후                                                                       |
|:-:|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
|7|프로듀서는 메시지를 파티션으로 대응시켜 주는 <ins>다름의 규칙</ins>을 가진 커스텀 파티셔너를 사용할 수도 있다.|프로듀서는 메시지를 파티션으로 대응시켜 주는 <ins>나름의 규칙</ins>을 가진 커스텀 파티셔너를 사용할 수도 있다.|
|21|<ins>cp</ins> `> /usr/local/zookeeper/conf/zoo.cfg << EOF`|<ins>cat</ins> `> /usr/local/zookeeper/conf/zoo.cfg << EOF`|
|22|주키퍼가 사용하는 <ins>부하 부산 알고리즘</ins> 때문에 앙상블은 홀수 개의 서버(예: 3개, 5개, ...)를 가지는 것이 권장된다.|주키퍼가 사용하는 <ins>부하 분산 알고리즘</ins> 때문에 앙상블은 홀수 개의 서버(예: 3개, 5개, ...)를 가지는 것이 권장된다.|
|23|<ins>정 파일</ins>의 모든 호스트명을 `localhost`로 지정하고 모든 `peerPort`, `leaderPort`에 서로 다른 포트를 할당함으로써|<ins>설정 파일</ins>의 모든 호스트명을 `localhost`로 지정하고 모든 `peerPort`, `leaderPort`에 서로 다른 포트를 할당함으로써|
|38|만약 클러스터가 10TB의 데이터를 저장해야하는데 하나의 클러스터가 저장할 수 있는 용량은 2TB라면, 클러스터의 최소 크기는 5대가 된다.|만약 클러스터에 10TB의 데이터를 저장하고 있어야 하는데 하나의 브로커가 저장할 수 있는 용량이 2TB라면, 클러스터의 최소 크기는 브로커 5대가 된다.|
|51|(그림 3-1 '카프카 프로듀서 요소 개괄' 에서 '시리얼라이저' 아래에 '프로듀서' 라고 되어 있음. 즉, 그림 안에 '프로듀서' 가 2개.)|('시리얼라이저' 아래에는 '파티셔너' 임.)|
|74|<ins>broker</ins>의 CPU 사용량을 줄인다.|<ins>브로커</ins>의 CPU 사용량을 줄인다.|
|74|(파티셔너에 접착성 처리가 있을 경우를 설명하는 오른쪽 그림에 7이 2개 있음)|(P0 오른쪽은 0, 1, 2.)|
|74|별 것 아<ins>니</ins> 것으로|별 것 아<ins>닌</ins> 것으로|
|81|주의할 점은 이 값들이 <ins>쓰기 쿼터/읽기 쿼터에 의해 발생한 스로틀링</ins> 때문에 지연된 시간을 가리킬 수도 있고, <ins>요청 쿼터</ins> 때문에 지연된 시간을 가리킬 수도 있고, 둘 다 때문에 지연된 시간을 가리킬 수도 있다는 점이다.|주의할 점은 이 값들이 <ins>쓰기 쿼터나 읽기 쿼터에 의해 발생한 스로틀링(초당 처리량 기준)</ins> 때문에 지연된 시간을 가리킬 수도 있고, <ins>요청 쿼터에 의한 스로틀링(요청을 처리하는 시간 비율 기준)</ins> 때문에 지연된 시간을 가리킬 수도 있고, 둘 다 때문에 지연된 시간을 가리킬 수도 있다는 점이다.|
|86|하지만, G2 전체를 놓고 보면 다른 컨슈머 그룹과는 상관없이 여전히 전체 메시지를 된다(그림 4-5).|하지만, G2 전체를 놓고 보면 다른 컨슈머 그룹과는 상관없이 여전히 전체 메시지를 <ins>받게</ins> 된다(그림 4-5).|
|99|일반적으로 모든 컨슈머들은 동일한 토픽들을 구독하기 때문에 RoundRobin 방식을 선택할 경우 모든 컨슈머들이 완전히 동일한 수(혹은 많아야 1개 차이)의 파티션을 할당받게 된다.|일반적으로, 만약 컨슈머 그룹 내 모든 컨슈머들이 동일한 토픽들을 구독한다면 (실제로 그런 게 보통이다) RoundRobin 방식을 선택할 경우 모든 컨슈머들이 완전히 동일한 수(혹은 많아야 1개 차이)의 파티션을 할당받게 된다.|
|101|컨슈머에 정<ins>작</ins> 그룹 멤버십 기능을 적용하기 위해 사용되는 설정으로 ...|컨슈머에 정<ins>적</ins> 그룹 멤버십 기능을 적용하기 위해 사용되는 설정으로 ...|
|160|만약 팔로워 레플리카가 10초 이상 메시지 요청을 보내지 않거나 10초 이상 가장 최근의 메시지를 가져가지 않을 경우 해당 레플리카는 동기화가 풀린 것으로 간주된다.|만약 팔로워 레플리카가 일정 시간 이상 읽기 요청을 보내지 않거나, 읽기 요청을 보내긴 했는데 가장 최근에 추가된 메시지를 따라잡지 못하는 경우 해당 레플리카는 동기화가 풀린 것으로 간주된다.|
|160|팔로워 레플리카가 아웃-오브-싱크 레플리카로 판정되기 전, 비활성 상태이거나 뒤쳐진 상태일 수 있는 시간은 replica.lag.time.max.ms 설정 매개변수에 의해 결정된다.|팔로워 레플리카가 동기화가 풀린 것으로 판정될 때까지 걸리는 시간, 즉 읽기 요청을 보내지 않거나 뒤쳐진 상태로 있을 수 있는 '일정 시간'은 replica.lag.time.max.ms 설정 매개변수에 의해 결정된다. (옮긴이 각주: replica.lag.time.max.ms의 기본값은 10초였으나 2.5.0부터 30초로 변경되었다.)|
|170|클러스터의 크기를 키우거나 줄일 때, 파티션의 위치를 다른 브로커로 옮기는 데 걸리는 시간은 파티션의 수에 따라 결정된다.|예를 들어서 클러스터의 크기를 키우거나 줄이거나 할 때, 파티션의 위치를 다른 브로커로 옮기는 데 걸리는 시간은 파티션의 크기에 따라 결정된다.|
|171|만약 파티션 0의 리더가 브로커 2에 있다면, 팔로워들은 브로커 3과 4에 배치될 수 있다. 하지만 2에 팔로워 브로커가 또 배치되거나 3에 두 개가 모두 배치될 수는 없다.|만약 파티션 0의 리더가 브로커 2에 있다면, 팔로워들은 브로커 3과 4에 배치될 수 있다. 하지만 브로커 2에 팔로워가 또 배치되거나 (즉 브로커 2에 리더와 팔로워가 하나씩 함께 배치) 브로커 3에 팔로워 두 개가 함께 배치될 수는 없다.|
|178|맵의 각 항목은 메시지 키의 16비트 해시와 같은 키값을 갖는 이전 메시지의 오프셋(8<ins>비트</ins>)으로 이루어진다.|맵의 각 항목은 메시지 키의 16바이트 해시와 같은 키값을 갖는 이전 메시지의 오프셋(<ins>8바이트</ins>)으로 이루어진다.|
|204|7.<ins>6</ins> 요약|7.<ins>7</ins> 요약|
 |266|만약 동일한 데이터셋을 여러 위치에서 비동기적으로 읽고써야 하는 문제를 해결할 방법을 찾고 있다면 이 아키텍처가 매우 권장된다.|만약 동일한 데이터셋을 여러 위치에서 비동기적으로 읽고 썼을 때 발생하는 문제점을 해결할 방법이 있다면, 이 아키텍처가 매우 권장된다.|
 |276|원본 토픽에 새 파티션이 추가될 경우, 자동으로 대상 토픽을 생성한다.|원본 토픽에 새 파티션이 추가될 경우, 자동으로 대상 토픽에 새 파티션이 생성된다.|
 |281|새로운 원본 파티션이 탐지되었을 때 토픽을 추가해주기 위한 대상 클러스터의 `Topic:Alter` 권한|원본 토픽에 새로 추가된 파티션이 탐지되었을 때 대상 클러스터 쪽에 새 파티션을 추가해주기 위한 대상 클러스터의 `Topic:Alter` 권한|
 |288|fetch.min.bytes and fetch.max.wait.ms|fetch.min.bytes, fetch.max.wait.ms|
|320|(인쇄 오류)||
|324|<ins>메시 지</ins> 암호화는 대개 AES와 같은|<ins>메시지</ins> 암호화는 대개 AES와 같은|
|324|<ins>매</ins>시지를 복호화하는 데|<ins>메</ins>시지를 복호화하는 데|
|327|`Allow|Deny`|`Allow` `|` `Deny`|
|334|(인쇄 오류)||
