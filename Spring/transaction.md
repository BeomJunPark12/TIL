# 트랜잭션

트랜잭션은 데이터베이스의 상태를 변환시키는 하나의 논리적 기능을 수행하기 위한 작업의 단위 또는 한꺼번에 모두 수행되어야할 일련의 연산들을 의미한다.

1. A은행에서 B은행으로 돈을 계좌 이체하려고 함
2. 송금 중에 알 수 없는 오류로 A은행에서 돈은 빠져 나가고 B은행의 계좌에는 입금되지 않음

    이러한 상황을 막기 위해서 거래가 완전히 끝나야 commit하고 거래 도중에 오류가 발생하면 거래 시작 전으로 rollback을 해야 함

# 트랜잭션의 성질
## 원자성( Atomicity)
    나눌 수 없는 하나의 작업으로 다뤄져야한다.
    어느 하나라도 오류가 발생하면 트랜잭션 전부가 취소되어야한다.


## 일관성(Consistency)
    Tx 수행전과 후가 일관된 상태를 유지해야한다.

## 고립성(Isolation)
    각 Tx는 독립적으로 수행되어야한다.
    수행 중인 트랜잭션은 완전히 완료될 때까지 다른 트랜잭션에서의 수행 결과를 참조할 수 없음.

## 영속성(Durability)
    성공한 Tx의 결과는 유지되어야한다.

- 커밋(commit) - 작업 내용을 DB에 영구적으로 저장
- 롤백(rollback) - 최근 변경사항을 취소(마지막 커밋으로 복귀)
- 자동 커밋 - 명령 실행 후, 자동으로 커밋이 수행됨(rollback불가)
- 수동 커밋 - 명령 실행 후, 명시적으로 commit 또는 rollback을 입력

    