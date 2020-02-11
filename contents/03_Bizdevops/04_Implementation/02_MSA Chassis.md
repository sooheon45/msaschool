# MSA Chassis

MSA Chassis 라는 말은 마이크로 서비스를 구축할때 필요한 주변 요소들을 일컫는다. 마치 ‘창틀처럼 이것저것 끼워
넣는다’로 해석할 수도 있다. 위에 설명한 헥사고날 아키텍처로 설계를 하여 비지니스 로직에 영향이 없는 개발을
맨땅에서 하려면 많은 공수가 필요하다. 이에 많은 프레임워크들이 이와 같은 패턴들을 구성해 놓고 제공중이다.

Java 계열에서 가장 선두주자인 Spring 프레임워크에서 마이크로 서비스에 적합한 spring-boot 프레임워크를 내어
놓았고, 이에 여러가지 어뎁터들에 해당하는 프로젝트들이 존재한다. 아래 그림은 헥사고날 아키텍쳐에 spring-boot
를 기반으로 한 MSA Chassis 를 입힌 모형이다. Spring-Data-Rest 를 사용하여 Data 를 외부와 Rest
방식으로 연결시키고 , String-Cloud-Stream 으로 메세지 처리를 하는 로직을 구현하여 특정 브로커에 종속적이지
않은 adapter 패턴으로 구현된 모형이다.

![스크린샷%202019-11-27%20오후%202](/img/03_Bizdevops/04/02/image89.png)