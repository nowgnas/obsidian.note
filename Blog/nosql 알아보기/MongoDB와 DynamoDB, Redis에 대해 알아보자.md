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
## DynamoDB vs MongoDB
| Feature | DynamoDB | MongoDB |
|:--:|:--:|:--:|
|Database Type | Nosql, document| Nosql, document |
|Data Model | Key-Value | document|

