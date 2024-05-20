* 장고 설정 
    * .env-example 을 .env로 바꾸고 시크릿키 넣기 
    * venv 켜기
    * pip install -r requirements.txt 
    * python3 manage.py createsuperuser
        * 시원의 패스워드 아이디는
        * siwonkim
        * 12341234 
    * python manage.py runserver 켜서 admin 페이지 입장
    * Categorys ,  Servers , Channels 순으로 인스턴스 생성 
    * 서버 종료후 유비콘 서버 실행
        * uvicorn djchat.asgi:application --port 8000 --workers 4 --log-level debug --reload
        * command.md 에 있음 
    * 이제 프론트에서 채팅이 가능!!  
* 리액트 설정
    * npm i 
    * npm run dev
    * MessageInterface.tsx


* 프로젝트 설명
    * Uvicorn is an ASGI web server implementation for Python.
    * 웹소켓 요청은 다르게 처리해야한다!!
    * 프로토콜에 따른 분리를 Protocol Type Router 가 해준다
        * asgi.py 에 있음
        * import 안되는 에러가 있으면 인터프리터 경로 복붙
        * urls.py 에 websocket_urlpatterns 로 url 분리되어있음
