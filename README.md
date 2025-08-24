# GYEONGSIL PARK - Full-Stack Developer 이력서

> 사용자와 개발자 모두가 만족할 수 있는 유지보수성 높은 코드와 명확한 로직 구현을 지향하며, 실제 사용자 니즈를 빠르게 파악하고 반영하는 개발을 강점으로 삼고 있습니다.

---

## 👤 **기본 정보**

- **Email:** [gps.siri92@gmail.com](mailto:gps.siri92@gmail.com)
- **GitHub:** [https://github.com/GPS-siri](https://github.com/GPS-siri)
- **연락처:** 010-9052-2896

- **개발철학:**

  - 급하다고 하드 코딩 하지 않는다.

    > 급할수록 돌아가라. 라는 말이 여기에 딱 들어 맞는 말인 것 같습니다. 그렇다고 너무 돌아가면 안되겠지만, 어떤 기능이든 충분한 의견 검토와 검증이 있은 후에 개발을 진행하는 것이 추후에 다른 기능을 추가함에 있어서도, 유지/보수에 있어서도 더 빠른 길이 된다고 생각합니다.

  - 코드 흐름에 대한 가독성을 중시 한다.
    > 코드의 가독성을 위해 함수를 길게 작성하고 따로 분리하지 않는 경우가 있습니다. 코드가 좀 중복 되더라도, 코드를 나중에 다시 재사용 하기 힘들게 되더라도, 기능/로직의 흐름을 한번에 쉽게 이해할 수 있게 코드가 작성 되었다면 좋은 코드라고 생각합니다.

  -팀원과의 긴밀한 협업과 리뷰를 충실히 한다.

  > 어떻게 보면 굉장히 당연한 소리입니다. 혼자서 하는 일에는 한계가 더 빨리 찾아오고, 충분한 완성도가 나올 수 없다고 생각합니다. 내가 고려하지 못했던 것을 동료가 생각해주고, 동료가 고려하지 못했던 것을 내가 채워줄 수 있는 상황이 정말 많았습니다.

---

### **업무 경력 (Work Experience)**

#### 프로텍트 (2020.08.20 ~ 2025.04.30)

## **Full-Stack Developer**

- **대한항공 AICC(AI Contact Center) 구축 프로젝트**

  - 사용기술: `ypescript` / `React` / `AWS Connect` / `AWS Lambda` / `AWS DynamoDB` / `AWS Lex`
  - 대고객(고객 파일업로드/고객 결제) 화면 Frontend 개발
  - Agent의 고객 전화 연결 업무 화면 Frontend/Backend 개발
    > AWS Connect 팀에서 개발한 페이지의 iframe 안에 들어가는 고객전화 연결 화면 및 각종 Utility 화면 개발
  - Okta 로그인 세션 및 쿠키 확인, 리디렉션 과정에서의 병목 현상 해결, 로그인 로직 CloudFront Functions 로 통합 관리하여, 페이지의 최초 렌더링 과정 단축

    > 성과: 홈화면 렌더링 속도 10초 → 3초 미만으로 개선 (70% 이상 단축)

  - AWS Connect 콘솔 로그인(Okta 로그인) 세션이 다수의 iframe 내에서 유지되지 않는 현상 해결
    iframe 태그내에 sandbox, allow-same-origin 등 옵션 추가 & axios에 withCredentials 설정 적용

    > 성과: AWS Connect 콘솔에서 한 번의 로그인으로 모든 기능 탭(iframe)에서 로그인 세션 공유/유지 가능

  - 브라우저의 BroadcastChannel API를 활용해, 각 기능 탭(iframe) 간 통신 기능 개발
    > 성과: 각 기능 탭 사이에 특정기능(알람기능)에서 메세지를 전달하도록 해, 특정 기능들의 실행 상태를 공유하도록 기능 개선

- **AI Chatbot 서비스 - AI 지혜 개발**

  - [(AI-Jihye: https://ai-jihye.com/)](https://ai-jihye.com/)
  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx` / `AWS Lex` / `Claude API` / `Mistral AI API`
  - 3명의 개발자를 리딩하여 개발을 진행. 신규 AI 챗봇 아키텍처를 설계 및 구현, 서버, 커스텀 경량 NLP 관련 업무를 맡음
  - 전체 질문/답변 로직에 사전 데이터 셋 생성하는 기능 추가 & 생성형 AI API 기능 연동 로직 담당 작업 - Cladue API를 Mistral AI API로 대체
    > 성과: 챗봇 실시간 응답 생성 속도가 평균 15초 → 2초대로 개선되어 약 85% 성능 향상

- **영업자 관리 CRM - Members Here 서비스 개발**

  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx`
  - 어드민 페이지 개발 참여
  - 전국적으로 미분양 발생에따른 조직분양 도입에 따라 영업자를 관리하고, 커미션을 정산하기 위하여 개발된 솔루션

- **(주)힐러비 / 넷마블 & Coway - 구독가능 건강관리 식품&화장품 쇼핑몰**

  - 사용기술: `Typescript` / `React`
  - 넷마블에서 개발예정이었던 건강 및 뷰티 상품 구독 홈쇼핑 앱의 위에 Webview 형식으로 쇼핑몰 페이지 개발
  - React native 로 개발된 앱의 기능과 Webview 로 개발된 쇼핑몰 페이지 기능 간에 통신 및 각 iOS/Android 기기의 기능 사용을 위해, Bridge(넷마블팀에서 개발) 기능 연동 개발
  - 사용자 경험 최적화 및 반응형 웹 구현
  - 결제 시스템 연동 및 구독 관리 기능 개발
  - 의사&약사 화상 상담 기능 개발 주도
    > 센드버드의 화상통화 솔루션 연동

- **미분양 해결 플랫폼 - MGM Here**

  - [MGM-Here](https://www.mgm-here.com)
  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx`
  - 기존에 엑셀로 하던 리스트 작업들을 시스템화 하여, 간단하고 획일화되고 중앙집중적으로 관리하게 해주는 솔루션
  - 분양대행사가 지역공인 중개사와 협동하여, 고객을 유치하고 커미션을 받는 구조의 미분양 해결 솔루션 개발
  - 삼일산업, 푸르지오 납품

- **삼성멀티캠퍼스 통합로그인 시스템 개발**

  - 사용기술: `Vue`
  - 멀티캠퍼스 & 한국지식 교육협회 SSO 시스템 Frontend 개발
  - 학습 커리큘럼 코스 기능 추가 개발

- **LG전자 상업용 세탁기 관리자 페이지 개발**

  - 사용기술: `Vue`
  - 세탁기 운영 현황 모니터링 시스템 구축 개발
  - Chart.js 라이브러리 활용한 대시보드 화면 개발

- **분양 CRM-Here 서비스 개발**

  - [CRM-Here](https://here.re.kr)
  - 사용기술: `Vue` / `Node`(Strapi) / `MySQL5.7` / `AWS EC2` / `Nginx`
  - 건설사의 분양 CRM(Admin 페이지 포함) 서비스 개발
  - 카카오톡 전송 기능 개발
  - 원패스 QR 시스템 개발
  - GS건설(자이), 자이에스앤디(자이르네), 삼성물산(레미안)에 솔루션 납품
  - [Here Service Overview](https://here.re.kr/here_service_211105.pdf)
    > 부동산을 원하는 고객의 데이터를 원하는 대로 설계하여 수집하고 카카오친구톡 or 단체 문자를 통하여 계약율을 올리는 솔루션. 사전영업, 방문예약, 워킹고객, 상담고객등의 데이터를 수집 할수 있고, 데이터 수집 비용과 마케팅 비용을 효과적으로 줄여주는 효과 제공.
  - 모델하우스 상담사 시스템 개발
    > 모델하우스 내에 상주하는 상담사가 사용하는 시스템으로, 아파트 구매에 관심이 있는 고객에게 분양 상품을 소개하고 판매하기 위해 사용하는 영업 전문가용 시스템. 계약 잠정 고객들의 데이터를 모아, 어드민 사이트 내 대시보드 페이지에 중요 데이터(설문 데이터 등)를 디스플레이하는 시스템

---

### **보유 기술 (Skills)**

#### Frontend

- `React`: 컴포넌트 기반 개발, Hooks, Redux등 상태관리 활용 (3년+)
- `Vue`: Vuex 활용 (3년+)
- `JavaScript`: ES6+
- `HTML/CSS`: 반응형 웹, Cross-browser 호환성
- `Apollo GraphQL`

#### Backend

- `Node.js`: RESTful API 설계 및 구현 (2년+)
- `AWS LEX`: AI 챗봇 서비스 연동 및 개발
- `AWS Lambda`, `API gateway`

#### DevOps & Cloud & Infrastructure

- AWS: `EC2`, `S3`, `Auto Scaling` 구성 및 운영
- 모니터링: `Google Analytics`, 서버 부하 테스트, `PM2`, `Grafana`

#### Database

- `MySQL`, `Redis`
- `AWS Dynamo DB`

---

### **학력 (Education)**

#### 대구한의대학교 IT의료산업학과 (2011.02 ~ 2022.02)

- 학점: 3.79 / 4.5

---
