# MVC, MVC2

## MVC 패턴이란?

<img width="334" alt="6" src="https://github.com/Newsujin/42gg-onboarding-be-01/assets/104690611/bb321806-b160-4a4b-b21b-12c8956a0f7d">



- 모델-뷰-컨트롤러(model–view–controller, MVC)는 소프트웨어 공학에서 사용되는 소프트웨어 디자인 패턴이다.
- `디자인 패턴`
    - 소프트웨어 디자인에서 **자주 발생하는 문제를 해결하기 위한** 일련의 솔루션을 포괄하는 반복적인 **디자인 원칙의 모음**
    - 장점
        1. **코드 재사용**: 디자인 패턴은 일반적인 문제 해결책 제공 → 비슷한 상황에서 동일한 패턴 재사용 가능
        2. **유지보수성**: 패턴을 따르는 코드는 일관성 유지함 → 변경 및 유지보수가 쉬워짐
        3. **가독성**: 패턴을 사용하면 코드 구조가 명확해짐 → 다른 개발자들이 코드를 이해하기 쉬워짐
        4. **확장성**: 패턴은 시스템을 쉽게 확장하고 변경할 수 있도록 해줌
        5. **유연성**: 디자인 패턴은 시스템을 보다 유연하게 만듦 → 새로운 요구사항에 대응하기 쉬움

## Model, View, Controller

### Model

- **Data**와 애플리케이션이 **무엇**을 할 것인지를 정의하는 부분으로, **내부 비즈니스 로직을 처리하기 위한 역할**
- 즉, 컨트롤러가 호출을 하면 **데이터와 연관된 비즈니스 로직을 처리하는 역할**
- 데이터의 CRUD(Create, Read, Update, Delete) 작업 수행

### View

- 사용자에게 보여주는 **화면(UI)**
- **사용자와 상호작용** 하며 컨트롤러로부터 받은 모델의 결과값을 사용자에게 화면으로 출력하는 일
- MVC에서는 여러 개의 View 존재 가능
- Model에서 받은 데이터는 별도로 저장 X

### Controller

- **Model과 View 사이를 이어주는 인터페이스 역할**
- 즉, **Model이 데이터를 어떻게 처리할지 알려주는 역할**
- Model이나 View에 대해서 알고 있어야 함

## MVC 패턴의 장점

- 서로 분리되어 각자의 역할에 집중 가능
- MVC 패턴을 사용하면 데이터(모델), 사용자 인터페이스(뷰), 비즈니스 로직(컨트롤러)이 서로 **독립적으로** 작동 → 애플리케이션을 보다 **구조화**하고 **유지보수**하기 쉽게 만들 수 있다.
- **수정이나 확장**이 필요할 때, 한 부분을 변경해도 **다른 부분에 영향을 주지 않도록 보장된다.**

## MVC 패턴의 예

1. 웹 애플리케이션
    1. Python 및 Django
    2. JavaScript 및 Angular
2. 데스크톱 애플리케이션
    1. Java 및 JavaFX
3. 모바일 애플리케이션
    1. Swift 및 iOS

## MVC 모델 1

<img width="621" alt="7" src="https://github.com/Newsujin/42gg-onboarding-be-01/assets/104690611/bfba8581-e444-4744-9a9a-b4e587667d81">


- MVC 모델 1은 **뷰와 컨트롤러의 역할이 합쳐져 있다.**
- 흔히 웹 개발을 하면 Jsp가 뷰 역할을 하는데, MVC 1에서 Jsp는 뷰와 컨트롤러의 역할을 모두 감당한다.
- 장점
    - 상대적으로 설계가 간단함
    - 개발 속도가 빠름 → 작은 프로젝트에 알맞음
- 단점
    - Jsp가 뷰와 컨트롤러 역할을 모두 수행 → Jsp에 Java 코드와 Html, css 등의 코드가 섞여 있어, 소스가 복잡해지고 읽기가 어려워짐 → 유지보수 힘듦

## MVC 모델 2


<img width="621" alt="8" src="https://github.com/Newsujin/42gg-onboarding-be-01/assets/104690611/4d9da7b3-0715-4686-8c0e-72ef7f1d47af">


- MVC 1에서 유지보수가 힘들다는 단점을 보완하기 위해 나온 모델
- JSP는 뷰의 역할만 하게 하고, 대신 컨트롤러 역할을 Servlet이 수행한다.
- Jsp는 Java 코드를 안 쓰는 대신 JSTL을 사용하여 결과 화면을 보여준다.
- 장점
    - Html과 Java 코드 분리됨 → 확장에 용이하고 유지보수가 수월해진다.
- 단점
    - 초기 설계단계에 비용이 많이 든다.
    - 개발 시간이 오래 걸린다.
