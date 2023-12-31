
## ✅프로젝트 구조

![image](https://blog.kakaocdn.net/dn/YsoF8/btq0ulDzW7m/Giuuy8FhFQgf4uLWJbyikk/img.png)


## ✅개발 환경

RESTful API 기반 Web Application

- IntelliJ Community Edition
- Springboot - 2.1.7
- Gradle - 4.10.2
- JUnit4
- Github
- H2
- lombok
- JPA
- OAuth2.0
- Mustache
- Bootstrap
- javascript
- AWS EC2 (Amazon Linux AMI 2)
- AWS RDS (MariaDB 10.6)
- AWS S3
- Putty
- HeidiSQL
- Travis CI
- Nginx






## ✅프로젝트 구성

#### 프로젝트 환경 설정

- 버전 관리를 쉽게하기 위해서 **Spring boot starter** 사용
- 아직 많은 기업에서 JUnit4를 사용한다는 점, 교재에 따라 JUnit5대신 **JUnit4** 사용
- JUnit의 버전에 따라 빌드 도구는 **Gradle의 4버전**
- 테스트용 Database로 배포할 때마다 초기화되는 **H2** 사용
- 쿼리문에 신경쓰지 않고, 객체 지향적인 코딩을 위해 **JPA** 사용
- 심플하고 View의 역할과 서버의 역할을 분리할 수 있는 **Mustache** 사용








## ✅ API 제작 과정

MVC 패턴으로 Dto, Service, Controller 클래스와 JpaRepository를 상속받은 Repository를 활용



1. Domain 패키지
   - Domain 패키지는 Database와 직접적으로 관련된 클래스들을 다룬다. 예를 들어 Entity와 Repository가 해당된다.
   - 굳이 패키지를 분리하는 이유는 Web Layer별로 역할을 철저히 나누며 테스트를 쉽게 하기 위해서입니다. 
2. 생성자로 Bean 주입
   - 생성자로 Bean을 주입하면 순환 참조와 같은 문제가 있을 때, 사전에 오류를 발견할 수 있다.
   - 해당 클래스의 의존성 관계가 변경될 때마다 생성자 코드를 수정할 필요가 없다.
   - 다른 방식과 다르게 필드를 final로 선언할 수 있다. 이는 런타임 환경에서 객체가 변경되는 상황을 사전에 방지할 수 있으며, @RequiredArgsConstructor로 생성자를 만들 수 있다.
3. Dto를 역할에 따라 분리
   - Posts Dto로 API를 처리할 수 있지만, request/response용 Dto를 따로 구현했다.
   - Posts Dto는 Entity 클래스로 Database로 맞닿아 있다. 즉, Entity 클래스는 Database의 Table과 맵핑되는 역할을 하므로, Entity 클래스의 잦은 변경에는 고려해야할 점이 많다.
4. 테스트 코드 작성
   - 기능이 많은 어플리케이션의 경우, 테스트 코드는 프로젝트의 완벽함을 입증한다.
   - 가령, 특정 코드를 변경한 후,  기존 코드들이 정상적으로 작동하는지 확인하려면 어플리케이션을 직접 구동해서 하나하나 실행해봐야 한다.
   - 하지만, 테스트 코드는 이러한 번거로움을 해결할 수 있으며, CI/CD를 활용하는 경우에는 프로젝트의 빌드를 성공적으로 다룬다.

## ✅프로젝트 산출물
1. Proejct 시작
  - [Spring boot로 변환하기](https://candoit.tistory.com/77)
  - [Controller 작성 및 테스트](https://candoit.tistory.com/78)
  - [JPA 사용하기](https://candoit.tistory.com/79)
  - [API 만들기(h2 웹 콘솔 사용)](https://candoit.tistory.com/80)

2. Mustache와 화면 구성
  - [Mustache](https://candoit.tistory.com/82)
  - [게시글 등록 화면](https://candoit.tistory.com/83)
  - [게시글 조회 화면](https://candoit.tistory.com/84)
   

3. OAuth 2
  - [구글 로그인 연동](https://candoit.tistory.com/85)
  - [네이버 로그인 연동](https://candoit.tistory.com/86)
   
4. Spring Security 
  - [테스트에 시큐리티 적용하기](https://candoit.tistory.com/87)



## ✅발생했던 이슈 사항

추후 추가 예정
