# MVC패턴이란?

MVC란 model-view-controller의 약자로 애플리케이션을 세 가지 역할로 구분한 개발 방법론이다

# Model1 Model2
## Model1
모델1 방식은 controller영역에서 view 영역을 같이 구현하는 방식

사용자의 요청을 jsp가 전부 처리

## Model2
모델2 방식은 웹브라우저 사용자의 요청을 서블릿이 받고 서블릿은 해당 요청으로 view를 보여줄 것인지 model로 보낼 것인지 판단하여 전송

모델2 방식은 html소스와 java소스를 분리해놓았기 때문에 모델1 방식에 비해 확장 및 유지보수가 쉽다



