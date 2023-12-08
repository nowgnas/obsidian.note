## Nosql 
No sql 은 Not only SQL로 비관계형 데이터베이스 유형을 말한다. RDB와는 다른 방식으로 데이터를 저장한다. 기본적으로 key-value 방식으로 데이터를 저장하게 된다. 
## CAP Theory 
![[Pasted image 20231207235942.png]]

### Consistency (일관성)
쓰기 동작 이후 발생하는 읽기 동작은 마지막으로 쓰인 데이터를 반환해야 한다. 모든 분산 노드에서 같은 시점에 동일한 데이터를 반환해야 한다.
### Availability (가용성)
특정 노드가 장애가 나도 서비스가 가능해야 하는 것을 의미한다. 
### Partition Tolerance(내구성)
노드의 상태는 정상이어도 네트워크 문제로 노드간의 연결이 끊어진 경우에도 정상적인 서비스가 가능해야 한다는 것이다. 

데이터베이스를 선택하기 전에 CAP 이론을 확인하여 용도에 맞게 사용하는 것이 좋다고 생각한다. CAP 3가지를 모두 만족하는 경우는 불가능하다. 데이터 형식, 데이터 흐름을 고려하여 어떤 특징이 적합한지 확인하여 프로젝트에 적용하자. 

## Redis vs MongoDB
| Feature | Reids | MongbDB |
|:--|:--|:--|
|데이터 구조 | Key-value | Document| 
|확장성 | 메모리 저장 | 디스크 저장| 
|지원 쿼리 | 기본적인 Key-value 연산, 데이터 구조별 복잡한 연산 지원 | 쿼리 연산, 집계 파이프라인 지원| 
|데이터 유지 | 캐싱에 사용, 영속성을 위한 RDB/AOF 옵션 | 데이터 영속화 | 
|성능 | 메모리 기반으로 고속 데이터 처리| 메모리 매핑을 이용한 빠른 데이터 처리| 
|사용 사례 | 캐싱, 메시징, 실시간 분석, 게임 랭킹, 세션 관리 | 웹 어플리케이션, 모바일, 로그 관리|

LINE에서 알림 시스템을 Redis에서 MongoDB로 전환한 사례가 있다. 👉 [line redis to mongodb](https://engineering.linecorp.com/ko/blog/LINE-integrated-notification-center-from-redis-to-mongodb)

