## 테이블 1

테이블명: users

설명: 서비스를 사용하는 사용자 정보를 저장한다.

컬럼:

[id]: 정수(integer), PK, 자동 증가, not null

[name]: 문자열(text), not null

[email]: 문자열(text), not null

[created_at]: 날짜/시간(datetime), not null, 기본값 현재 시간

관계:

* 연결되는 테이블이 없다면 '없음'이라고 적는다.

## 테이블 2

테이블명: todos

설명: 사용자가 작성한 할 일 정보를 저장한다.

컬럼:

[id]: 정수(integer), PK, 자동 증가, not null

[title]: 문자열(text), not null

[content]: 문자열(text), not null

[due_date]: 날짜/시간(datetime), not null

[priority]: 문자열(text), not null

[is_completed]: 정수(integer), not null

[user_id]: 정수(integer), not null, FK -> users(id)

[created_at]: 날짜/시간(datetime), not null, 기본값 현재 시간

관계:

* 이 테이블의 [user_id]는 users의 [id]를 가리킨다.
