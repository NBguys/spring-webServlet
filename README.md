# 웹 서버와 서블릿 컨테이너
![screenshot](src/main/resources/img/서블릿%20스프링%20컨테이너%20설정%20그림.png)

* 현재 등록된 서블릿 다음과 같다.
  * / = dispatcherV3
  * /spring/* = dispatcherV2
  * /hello-servlet = helloServlet
  * /test = TestServlet
  * 이런 경우 우선순위는 더 구체적인 것이 먼저 실행된다.

참고
* 여기서는 이해를 돕기 위해 디스패처 서블릿도 2개 만들고, 스프링 컨테이너도 2개 만들었다.
* 일반적으로는 스프링 컨테이너를 하나 만들고, 디스패처 서블릿도 하나만 만든다. 그리고 디스패처 서블릿의 경로 매핑도 / 로 해서 하나의 디스패처 서블릿을 통해서 모든 것을 처리하도록 한다