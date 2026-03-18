SQL Injection - Login Bypass

1. 문제
로그인 기능에서 SQL Injection 취약점 존재

2. 목표
administrator 계정으로 로그인

3. 시도 과정
' OR 1=1 -- → Internal Server Error 발생
administrator-- → 로그인 성공

4. 결과
비밀번호 없이 관리자 계정 로그인 성공

5. 원리
입력값이 SQL 쿼리에 그대로 사용됨
-- 주석을 이용해 비밀번호 검증을 무시함

6. 배운 점
입력값 검증이 없으면 인증이 우회될 수 있음
SQL Injection은 로그인 기능에서도 발생함
