# 쿠키(Cookie)
<!-- content -->
1. Http의 일종으로 사용자가 어떠한 웹사이트를 방문 할 때 그 사이트가 사용하고 있는 서버에서 사용자의 컴퓨터로 저장하는 작은 기록 정보 파일이다.
2. Http에서 클라이언트의 상태 정보를 클라이언트 컴퓨터에 저장하고 필요시 정보를 참조하거나 재사용 할 수 있다.
- 사용 예시
    1. 로그인 할 때, "아이디와 비밀번호를 저장하시겠습니까?"
    2. 팝업창, "오늘 이 창을 다시 보지않기"

# 세션(Session)
<!-- content -->
1. 일정 시간 동안 같은 사용자로부터 들어오는 요구를 하나의 상태로 보고, 그 상태를 유지시키는 기술이다.
2. 여기서 일정 시간은 사용자가 웹 브라우저를 방문했을 때 접속한 시점부터 종료하여 연결을 끝내는 시점을 말한다.
3. 즉 방문자가 웹 서버에 접속해 있는 상태를 하나의 단위로 보고 이것을 세션이라고 한다.
- 사용 예시
    - 화면을 이동해도 로그인이 풀리지않고 로그아웃전까지 유지

# 쿠키와 세션 차이

|쿠키|세션|
|---|---|
|브라우저에 저장|서버에 저장|
|서버 부담 x|서버 부담 O|
|보안에 불리|보안에 유리|
|서버 다중화에 유리|서버 다중화에 불리|

# Q. 세션을 사용하면 좋은데 왜 쿠키를 사용할까?
- 세션이 쿠키에 비해 보안은 좋지만 쿠키를 사용하는 이유는 세션은 서버에 저장되고 서버의 자원을 사용하기에 서버에 한계가 있어서 속도가 느려질 수 있다. 
- 그래서 자원관리 차원에서 쿠키와 세션을 적절한 요소 및 기능에 병행 사용하여 서버 자원 낭비를 막고 서버의 속도를 높일 수 있다.