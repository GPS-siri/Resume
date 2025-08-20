# GYEONGSIL PARK - Full-Stack Developer 이력서

> 사용자와 개발자 모두가 만족할 수 있는 유지보수성 높은 코드와 명확한 로직 구현을 지향하며, 실제 사용자 니즈를 빠르게 파악하고 반영하는 개발을 강점으로 삼고 있습니다.

---

## 👤 **기본 정보**

- **Email:** [gps.siri92@gmail.com](mailto:gps.siri92@gmail.com)
- **GitHub:** [https://github.com/GPS-siri](https://github.com/GPS-siri)
- **연락처:** 010-9052-2896

- **개발철학:**
  저의 개발철학은 한마디로 "Simple is best" 입니다.
  즉, “누구나 이해할 수 있는 단순한 코드”입니다.
  물론 기능을 구현하다 보면 자연스레 코드의 복잡도가 올라가고, 특정 기능들에 대해서는 history를 알지 못하면 한번에 알아 볼 수 없는 코드들이 생길 수 있다고 생각합니다. 그럼에도 최대한 누군가가 봤을때, 혹은 미래의 내가 유지보수를 위해 다시봤을때 기능 및 로직의 흐름이 한번에 파악되는 것이 최고라고 생각합니다.
  기능을 구현하는데 꼭 알아야 하는 history가 있다면, 문서로도 정리함과 동시에 코드상에 주석을 활용해서 최대한 설명을 많이 하려고 노력하고 있습니다.
  5년이 거의 다 되어가는 시간동안 여러가지 솔루션 개발과 프로젝트에 참여하면서 가장 중요하게 깨달은 것이 있습니다. 동료와의 원활하고 긴밀한 소통과 내가 작성한 코드에 대한 리뷰, 서로에 대한 리뷰가 정말 중요하다는 것 입니다.
  어떤것이든 혼자 힘으로 만들거나, 소통이 없거나 부족한 상태에서 개발을 한다면 좋은 솔루션이나 제품이 나오기 힘들었습니다. 내가 고려하지 못했던 것을 동료가 생각해주고, 동료가 고려하지 못했던 것을 내가 채워줄 수 있는 상황이 매번 있었습니다. 항상 동료들과 소통하고 같이 결정한 내용에 맞게 한 곳을 바라보고 노력했을 때 나온 결과물들이 누가봐도 더 괜찮은, 좋은 결과물들이었습니다.
  요약하자면,

1. 필요한 경우 로직을 분리하지 않고, 한 흐름처럼 기술합니다. (가독성UP)
2. 기능에 대한 부연설명, history 설명을 위해 코드 내 주석을 많이 활용합니다.
3. 무엇보다 중요한 것은 팀원과의 긴밀한 협업과 리뷰 문화라고 생각합니다.

---

### **업무 경력 (Work Experience)**

#### 프로텍트 (2020.08.20 ~ 2025.04.30)

## **Full-Stack Developer**

- **대한항공 AICC(AI Contact Center) 구축 프로젝트**

  - 사용기술: `ypescript` / `React` / `AWS Connect` / `AWS Lambda` / `AWS DynamoDB` / `AWS Lex`
  - 대고객(고객 파일업로드/고객 결제) 화면 Frontend 개발
  - Agent의 고객 전화 연결 업무 화면 Frontend/Backend 개발
    > AWS Connect 팀에서 개발한 페이지의 iframe 안에 들어가는 고객전화 연결 화면 및 각종 Utility 화면 개발
  - 문제: 최초 로그인 후 홈화면 로딩 시간이 10초 이상 소요됨
    → iframe 내부에서 Okta 로그인 세션 및 쿠키 확인, 리디렉션 과정이 병목 원인.
    개선사항: 로그인 세션 확인 로직을 AWS CloudFront Functions로 통합 관리하도록 분리.
    성과: 홈화면 렌더링 속도 10초 → 3초 미만으로 개선 (70% 이상 단축)

    문제: AWS Connect 콘솔 로그인 상태가 iframe 내에서는 ₩유지되지 않음.
    → 부모 페이지(Okta 로그인)와 iframe간 세션 공유 문제.
    개선사항: iframe태그에 sandbox, allow-same-origin 등 iframe 옵션 추가 및 axios withCredentials 설정 적용.
    성과: 한 번의 로그인으로 모든 기능 탭(iframe)에서 로그인 상태가 유지됨.

    문제: 상담사 화면에서 기능탭(iframe)마다 메시지 알람이 중복으로 발생.
    개선사항: BroadcastChannel API를 활용해 탭 간 통신 및 기준 탭에서만 알람 표시하도록 제어.
    성과: 여러 기능 탭 사용시에도 메시지 알람이 한 번만 뜨도록 구현.

- **AI Chatbot 서비스 - AI 지혜 개발**

  - [(AI-Jihye: https://ai-jihye.com/)](https://ai-jihye.com/)
  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx` / `AWS Lex` / `Claude API` / `Mistral AI API`
  - 3명의 개발자를 리딩하여 개발을 진행. 신규 AI 챗봇 아키텍처를 설계 및 구현, 서버, LLM 관련 업무를 맡음.
  - 문제: 등록되지 않은 질문에 대해 Claude API로 실시간 응답 시, 평균 15초 이상 소요되어 사용자 경험 저하.
    개선사항: Claude API를 Mistral API로 대체하고, 질문/답변을 사전 데이터로 등록해 반복 생성 방지.
    성과: 챗봇 실시간 응답 생성 속도가 평균 15초 → 2초대로 개선되어 약 85% 성능 향상.

- **영업자 관리 CRM - Members Here 서비스 개발**

  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx`
  - 어드민 페이지 개발 참여
  - 전국적으로 미분양 발생에따른 조직분양 도입에 따라 영업자를 관리하고, 커미션을 정산하기 위하여 개발된 솔루션.

- **(주)힐러비 / 넷마블 & Coway - 구독가능 건강관리 식품&화장품 쇼핑몰**

  - 사용기술: `Typescript` / `React`
  - 넷마블에서 개발예정이었던 건강 및 뷰티 상품 구독 홈쇼핑 앱의 위에 Webview 형식으로 쇼핑몰 페이지 개발
  - React native 로 개발된 앱의 기능과 Webview 로 개발된 쇼핑몰 페이지 기능 간에 통신 및 각 iOS/Android 기기의 기능 사용을 위해, Bridge(넷마블팀에서 개발) 기능 연동 개발
  - 사용자 경험 최적화 및 반응형 웹 구현
  - 결제 시스템 연동 및 구독 관리 기능 개발

- **미분양 해결 플랫폼 - MGM Here**

  - [MGM-Here](https://www.mgm-here.com)
  - 사용기술: `Vue` / `Node`(strapi) / `MySQL5.7` / `AWS EC2` / `Nginx`
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

- **방문예약 CRM-Any Reserve 개발**
  - 사용기술: Vue / Node(strapi) / MySQL5.7 / AWS EC2 / Nginx
  - 건설사의 모델하우스에 방문예약 서비스를 제공할 목적으로 개발
  - 어드민 페이지 개발
  - 분양 CRM에 방문예약만 특화하여 운영중인 솔루션
  - 슈트패브릭

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
