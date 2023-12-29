## daemon set 
- 클러스터 전체 노드에 특정 파드를 실행할  때 사용하는 컨트롤러 ![[Screenshot 2023-12-29 at 21.21.27.png]]
- 로그 수집 용 
## stateful set
- 상태가 있는 pod을 관리 
- volume을 사용해 특정 데이터를 저장 후 pod를 재시작 했을 때 해당 데이터를 유지 
- 여러 개의 pod 사이에 순서를 지정해 실행할 수 있음 
- 업데이트 방법은 spec.updateStrategy.type 필드에 설정 
	- 기본값은 rollingUpdate
	- 템플릿 변경 시 자동으로 예전 파드 삭제하고 새로운 파드 실행 
- spec.updateStrategy.rollingUpdate.partition 필드 값을 바꾸면 스테이트풀 세트에 변경 사항이 있을 때 지정된 값보다 큰 번호를 가진 파드들을 업데이트 한다. 
- 작은 번호는 업데이트 하지 않는다. 파드가 분할되는 것 
- 