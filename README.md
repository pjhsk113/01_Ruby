# Ruby on rails란 ?
- ### Ruby프로그래밍 언어로 이루어진 오픈소스 웹 프레임워크
- ### 강력하고 탄탄한 웹 어플리케이션을 빠르게 개발할 수 있음
# Ruby on rails의 특징
- ### MVC 아키텍처 구조
- ### 관습적이지 않은 면만 정의(CoC)
    - 관습적이지 않은 부분만 코드를 작성하면 작동하도록 기본값을 설정하는 패러다임
- ### 똑같은 것을 반복하지 않는 구조(DRY)
    - 코드의 반복을 줄이는 원칙, 반복되는 부분을 묶어서 다룸
# 1. 구름 IDE로 RAILS Page 생성하기
1. rails 프로젝트 생성
1. 컨테이너 접속 후 컨트롤러 생성
    - 터미널에 rails g controller home 입력 --> home이라는 이름의 controller 생성
1. views로 이동
   - views 폴더를 확인해보면 만들어준 controller의 이름으로 폴더가 생성됨
   - 우클릭 - 새로만들기 - index.html.erb 라는 이름으로 index 생성 (erb: Embeded RuBy)
1. config의 routes.rb파일로 이동하여 전송방식 및 접속 url 명시
```ruby 
# get방식, /home로 접속 시 home_controller의 index 함수 실행
get '/home', to: 'home#index'
```
1. Contorller에 함수 작성
```ruby
def index
  @x =1001
end
```
1. index.html.erb에 controller에 선언한 변수 x를 받아옴
```ruby
<h1> <%= @x %> </h1>
```
1. 실행 --> 할당 된 URL로 접속 --> /home으로 접속
    - 정상적으로 실행되었다면 1001이 출력됨
# 2. Ruby on rails - 간단한 게시판 만들어보기
