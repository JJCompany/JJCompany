---
category: Sql
path: '/SQL'
title: 'SQL initialize-auto_increment'
type: 'POST'
layout: nil
---
### MYSQL initialize auto_incremnet(MYSQL자동증가 값 초기화)
MYSQL에서 자동증가값은 많은 부분에서 쓰이게 된다. 그런데 이 값이 너무 증가하여 초기화가 필요한 시점이 올수도 있다.
int(11) auto_increment으로 설정을 하게 되면, 최대 4294967295까지 사용이 가능하고 그 다음 번호부터는 오류가 발생.

MYSQL자동증가 값 초기화 방법
* 초기화 예정인 테이블 자료 백업
* 테이블 자료 삭제 ```delete from 'tablename'```
* auto_increment 초기화 alter ```table 'tablename' auto_increment=1```
* 백업한 데이터 인서트
