# 스프링 강의

## 회원 서비스 개발

* Optional을 통해 객체 형태로 수신 가능 => ifPresent 활용 가능
* return 값에서 바로 get을 쓰는 것은 권장하지 않음
* **Control + T** 단축키를 통해 별도의 함수명을 만들 수 있음
* 서비스 메서드는 비즈니스 적으로 생성하고 리포지토리는 개발에 편리하도록 생성





## 회원 서비스 개발 테스트

* **Control + Shift + T**를 통해 테스트 케이스 파일 자동 생성 가능
* 테스트 메서드는 한국어로 적어도 상관 없음
* 테스트 작성할 때는 *given*, *when*, *then* 세가지 주석으로 분리하여 활용하면 좋음
* **Control + Alt + V** : 메서드에 대한 반환 타입과 변수를 자동으로 생성
* **BeforeEach**: 각 테스트 실행 전 호출
* **AfterEach**: 각 테스트 실행 후 호출



## 컴포넌트 스캔과 자동 의존 관계 설정

* **Controller**: 외부 요청 받음
* **Service**: 비즈니스 로직 만듦
* **Repository**: 데이터 저장
* **@**를 통해 붙여놓으면 스프링이 올라올 떄 알아서 끌고옴
* **@Autowired**를 통해 자동으로 의존성 주입(Dependency Injection; DI)
* Component 같은 패키지 하위에서만 적용됨(별도로 설정 가능하긴 하지만 일반적인 상황에서 설명)
* 스프링은 스프링 컨테이너에 스프링 비을 등록할 떄 기본적으로 [싱글톤](https://cheershennah.tistory.com/223)으로 등록
* 스프링 빈이 등록되어 있지 않으면 **@Autowired** 동작하지 않음



## 데이터 베이스

* DDL 파일은 프로젝트 내에 별도의 디렉토리(sql) 등을 생성하여 관리하는 것이 유지 보수 측면에서 좋음
* 순수 JDBC 강의 부분은 참고 용도(데이터 베이스 연결 기술의 발전 확인)
* h2 DB는 ```h2.bat``` 을 실행해야 웹에서 실행할 수 있음



## 스프링 JDBC Template

* 생성자가 하나면 Autowired 생략 가능

* JDBC 사용하려면 build.gradle 파일에 의존성 추가해야 함

  ```
  dependencies {
  	implementation 'org.springframework.boot:spring-boot-starter-jdbc'
  	runtimeOnly 'com.h2database:h2'
  }
  ```

