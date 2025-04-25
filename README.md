# 병원 예약 어플리케이션

</br>

### 👥 팀원

<table>
  <tr align="center">
    <td><img src="https://github.com/SSan0613.png" width="100" height="100"/></td>
    <td><img src="https://github.com/goodperiodt.png" width="100" height="100"/></td>
    <td><img src="https://github.com/dominic-yoon.png" width="100" height="100"/></td>
    <td><img src="https://github.com/sojinnuna.png" width="100" height="100"/></td>
  </tr>
  <tr align="center">
    <td><a href="https://github.com/SSan0613">차상준</a></td>
    <td><a href="https://github.com/goodperiodt">박성주</a></td>
    <td><a href="https://github.com/dominic-yoon">윤관</a></td>
    <td><a href="https://github.com/sojinnuna">김소진</a></td>
  </tr>
  <tr align="center">
    <td><img src="https://img.shields.io/badge/GitHub-SSan0613-black?style=social&logo=github"/></td>
    <td><img src="https://img.shields.io/badge/GitHub-goodperiodt-black?style=social&logo=github"/></td>
    <td><img src="https://img.shields.io/badge/GitHub-dominic--yoon-black?style=social&logo=github"/></td>
    <td><img src="https://img.shields.io/badge/GitHub-sojinnuna-black?style=social&logo=github"/></td>
  </tr>
</table>

</br>
---

</br>

### ⏰ 프로젝트 기간  
📅 **2025-04-03 ~ 2025-04-25**

</br>

---
</br>

### 📝 목차
- 프로젝트 소개
- 사용한 기술 스택
- 프로젝트 아키텍처
- 도메인 및 마이크로서비스 구성

</br>
---

</br>

### ⚙ 프로젝트 소개

**대용량 트래픽 환경에서도 병원 예약의 정확성과 안정성을 보장하는 MSA 기반 시스템**

본 프로젝트는 병원 예약 서비스를 MSA(Microservices Architecture) 구조로 설계하여, 안정성과 확장성을 극대화한 헬스케어 플랫폼입니다.

- **서버 이중화 및 로드 밸런싱**을 통해 급격한 트래픽 증가에도 안정적인 서비스 제공합니다.
- **Redisson 기반 분산 락** 적용으로 동시 예약 상황에서도 **데이터 정합성과 일관성**을 확보했습니다.  
- 각 기능을 **독립적인 마이크로서비스**로 분리하여 **유지보수성과 유연한 확장성** 제공합니다.

</br>
--- 
</br>

### ⚒️ 사용한 기술 스택

- **Language:** Java  
- **Framework:** Spring Boot  
- **Build Tool:** Gradle  
- **Database:** PostgreSQL  
- **ORM:** Spring Data JPA  
- **Security:** Spring Security, JWT  
- **Cloud & Infrastructure:**  
  - AWS (EC2, RDS)  
  - Spring Cloud (Eureka, Gateway, Config Server 등)  
- **Monitoring:** Prometheus

</br>

### 📝 Technologies & Tools 📝
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=flat&logo=jsonwebtokens&logoColor=white)
![Spring Cloud Gateway](https://img.shields.io/badge/Spring%20Cloud%20Gateway-6DB33F?style=flat)
![Eureka](https://img.shields.io/badge/Eureka-6DB33F?style=flat)
![Spring Cloud Config](https://img.shields.io/badge/Config%20Server-6DB33F?style=flat&logo=spring&logoColor=white)
![Feign Client](https://img.shields.io/badge/FeignClient-000000?style=flat)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000?style=flat&logo=intellijidea&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat&logo=notion&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=flat&logo=slack&logoColor=white)

</br>
---
</br>

### 🛠️ 프로젝트 아키텍쳐
  
- 인프라 설계도
  ![project3-서비스 흐름도(도식) drawio](https://github.com/user-attachments/assets/aec947b0-67a2-464c-b138-5551e4ef9d07)

</br>

- ERD
  ![2열7열 (1)](https://github.com/user-attachments/assets/c6659c1a-1c5b-41fc-8d55-74fb8f190d25)

</br>

---

</br>

### 🧩 도메인 및 마이크로서비스 구성

본 프로젝트는 **MSA(Microservices Architecture)** 기반으로 각 도메인을 독립된 서비스로 분리하여 개발하였습니다.  
각 서비스는 명확한 책임을 가지며, **Spring Cloud Gateway**를 통해 라우팅되고, **JWT 기반 인증/인가**가 적용됩니다.

</br>

#### 🧱 서비스 정보

- **eureka-server**  
  - 각 마이크로서비스를 등록하고 관리하는 서비스 레지스트리
  - 마이크로서비스 간 통신을 위한 서비스 디스커버리 기능 제공

- **gateway-service**  
  - 모든 클라이언트 요청의 진입점  
  - 요청을 적절한 마이크로서비스로 라우팅  
  - 인증, 로깅 등의 공통 필터 처리

- **common-module**  
  - 모든 마이크로서비스의 공통 설정 관리  
  - 공통 예외 처리, `BaseEntity`, `UserInfo` 등의 공용 클래스 제공

- **user-service**  
  - 사용자 회원가입, 로그인 처리  
  - JWT 기반 인증/인가 기능 제공

- **hospital-service**  
  - 병원 등록 기능  
  - 병원 정보 조회, 수정, 삭제 관리

- **reservation-service**  
  - 예약 생성 및 관리  
  - 예약 조회, 수정, 삭제 기능 제공

- **notification-service**  
  - 예약 생성/삭제 시 사용자에게 알림 전송 기능 제공

- **review-service**  
  - 리뷰 작성, 조회, 수정, 삭제 기능 제공

</br>
