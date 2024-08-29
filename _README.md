<p align='center'>
<h1 align='center'>Hi, I am Kwangmin Kim<img src="https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif" height="25px"></h2>
<p align='center'>Software Engineer  | Backend Developer  | DevOps </h4>
</p>

I'm a backend developer with 8 years of experience, currently working on a large-scale multi-tenancy web builder platform. I'm specialized in designing scalable systems with large traffics.

📄 [My Resume](https://thegrid-labs.com/resume) | 🌐 [My Website](https://thegrid-labs.com) | <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/medium.svg" alt="480kyle" height="20px" width="30px" /> [My Writings](https://medium.com/@kyle.kim0305)

## 🚀 Projects
<!-- - **ShopOS**: Developed a customizable headless commerce backend operating system using Nest.js.
- **Multilingual System Improvement**: Streamlined translation processes and eliminated over 30,000 lines of PHP code.
- **Order Payments System**: Built a new API in a high-traffic MSA environment using TypeScript, Nest.js, and AWS services.
- **Legacy System Migration**: Led migration project implementing CQRS pattern with BullMQ.
- **E-commerce Platforms**: Developed platforms for various industries including fashion, art, furniture, and F&B. -->

- ShopOS
  - What problem, And what did you?
    - 고정된 플랫폼을 사용하는 상점 관리자들이 비즈니스가 성장할수록 축적된 데이터를 활용하여 새로운 기능을 개발하려하는 니즈를 해소하는 프로젝트 입니다. 개발자, 디자이너 등 이커머스 사이트 전문 사용자들에 의해 커스텀이 가능한 Operating System 개념을 구현할 수 있는 SaaS를 만들고자 했습니다.
    - NPM을 통해 설치가 가능한 Nest.js 기반의 이커머스 프레임워크 프로젝트
    - 이커머스 백엔드 비즈니스 로직, 데이터 레포지토리, OpenAPI, Administration UI, GraphQL 플레이그라운드 포함
    - ORM 개념 차용, 사용자가 UI에서 커스텀된 데이터 모델을 추가하면 그에 맞는 GraphQL API를 서빙하는 eCommerce Operating System

  - How solve/develop?
    - 고정된 컬럼 이외의 커스텀 필드를 사용할 수 있는 데이터 구조를 GraphQL 형태로 서빙하는 API를 만들었습니다.
    - 어드민 페이지를 만들어 커스텀 필드를 쉽게 설정할 수 있도록 하였습니다.
    - 코어 서비스를 만들고 어드민에서 커스텀된 데이터 필드를 GraphQL로 즉각 서브할 수 있게 구현하였습니다.
    - 프론트엔드 개발 패키지를 npm으로 제공함으로써 즉각적인 API 연동을 할 수 있게 구현하였습니다.
    - 구조적으로는 커넥터를 통해 규격을 맞추면 PG 프로바이더 등 3P 프로바이더를 원하는 방식으로 구현하여 사용할 수 있도록 하였습니다.
  - What you achieved?/Or what you can do with this result?
    - Scalable APIs
    - Reliable business backends
    - Efficient and effective data repositories
    - Well-lit external service connectors
    - Custumizable Headless Commerce Backend Operating System
- i18n 시스템 개선 프로젝트
  - What problem, And what did you?
    - 15000 라인 이상의 IDE에 로드가 불가능한 거대한 php 파일 3개로 총 30000 라인 이상의 다국어 코드
    - 다국어 코드가 발생할 때마다 추가되던 코드에 맞춘 함수
    - 450만 DAU가 호출할 때마다 발생하는 다국어DB 호출 쿼리
    - 배포시에 배포서버에서 실행되던 php 코드로 만들어진 전체 파일 탐색 및 파일 수정
    - php파일과 데이터베이스, 레디스 캐시를 통해 동적 생성 하는 다국어 시스템 개선 프로젝트
  - How solve/develop?
    - po파일을 사용하는 다국어 관리 시스템으로 변경
    - 번역가가 사용하는 po파일 관리 시스템은 Weblate 오픈소스를 on-demand에서 커스텀 후 사용
    - 다국어 코드 배포시 php 코드를 통해 실제 파일을 변경하는 절차가 존재하였으나 다국어를 검색하기 위해 4중 루프를 사용하여 모든 범위를 검사하였다. 변경된 프로세스는 4중 루프를 포함하는 php 파일 변경 코드를 없애고 다국어 코드와 php 코드 배포 프로세스를 분리한 뒤 프로덕션 서버에 올리기 전 GHA(Github Actions)를 통해 L2 메모리에 저장되어 있는 다국어 코드로 치환 되도록 작성함. 이전에는 배포되는 모든 파일을 검사했다면 바뀐 프로세스에서는 GHA API를 통해 변경이 존재하는 파일만 검사하기 때문에 프로세스가 단축되었다.
    - php 기반으로 렌더링되던 다국어 시스템 구현 방식을 UNIX 기반의 gettext 함수로 변경
    - 업데이트 된 po 파일을 mo 파일로 변환 후 각 서버의 L2 메모리에 저장하는 방식 사용
  - What you achieved?/Or what you can do with this result?
    - 15000 라인 이상의 거대한 php 파일 3개로 총 30000 라인 이상의 코드로 관리되던 기존 시스템 완전 제거
    - 4중 루프로 생성하는 로직을 제거하여 다국어 파일 생성시간 5분 -> 5초 단축
    - 다국어 변경시 코드를 변경하여 레포지토리 업데이트를 하던 프로세스 제거 
    - 개발자가 직접 다국어 코드를 생성하고 문구 변경시 요청되던 개발자 리소스 제거
    - 번역 외주가 가능해져서 운영팀의 번역지원 업무가 사라짐

- Order/Payment Management System
  - What problem, And what did you?
    - 기존의 모놀리식 시스템에서는 쌓여있는 레거시 이슈가 다량 발생하고, 대규모 트래픽이 특정 시간/이벤트에 몰리는 상황에서 크리티컬한 중복 주문(동일한 주문 번호가 발급되어 개인정보유출 등 문제를 발생 시킴) 등 심각한 이슈가 발생하여 모던 스택을 사용하는 새로운 주문 결제 시스템을 개발하였습니다. 저는 이 프로젝트에서 주문, 결제와 관련된 부분을 설계, 적용하는 역할을 맡아 수행하였고, 전략 패턴, 상태 관리 패턴 등을 적용하여 AOP(Aspect-Oriented Programming)가 가능한 어플리케이션을 제작하고 동료에게 공유하였습니다.
    - 하나의 상점이 복수 PG를 사용하여 결제를 할 수 있습니다.(비율로 설정 가능)
      - 매출 볼륨이 큰 고객에게 PG사보다 우위에 있게 하는 경쟁력을 주는 것
    - 하나의 주문이 여러 섹션으로 관리되어 별도의 주문 건으로 처리가 가능하게 되지만 각각의 아이템이 상태를 가지면서 여러 주문 처럼 상태를 관리 할 수 있는 것.
    - 주문 flow 의 최소 단위를 SKU 단위 재설계 하는 것 
      - SKU 단위의 주문들을 자유롭게 묶고/풀고/취소/교환/반품 하는 것
      - 리얼 월드의 주문 처리 요구사항이 반영 되는 것(like Amazon)
    - 한번의 주문에 여러 결제 방법을 섞는 복합 결제, 분할 결제를 만드는 것 (오프라인 상점에서 결제하는 것처럼 카드 + 가상계좌 등)
    - 주문 하위 섹션 단위로 분리하여 어드민 화면에서 새로운 상품 추가 및 결제 요청이 가능하도록 하는 것
    - 주문 섹션 별로 별도의 배송지로 배송이 가능하도록 하는 것

  - How solve/develop?
    - AOP가 가능한 프레임워크 Nest.js를 사용하여 기본 설계를 하고 주문 및 결제 기능의 Interface를 만들어 REST API를 작성할 수 있도록 동료들과 컨벤션을 정하고 각각의 담당 개발자를 지정했습니다.
    - TypeScript, Nest.js, AWS EKS, AWS Aurora, BullMQ 환경을 적용할 수 있게 되면서 환경적으로 해결되지 못하던 이슈가 최신 기술로 빠르게 해결될 수 있는 환경이 갖춰졌습니다.
    - 개발자가 기능 구현에 집중할 수 있도록 git-flow 정책에 의해 자동 배포될 수 있도록 인프라를 구성하였습니다.
      - CI/CD: Jest, Github Action
      - Infra: AWS - EKS, ECR, Aurora 3 Serverless, Elasticache, S3, ALB, CF
    - Datadog을 통해 모니터링할 수 있도록 구성하였습니다.
    - Data Analyst, DBA와 스키마 설계를 같이하여 데이터 분석이 가능하도록 하였습니다.
    - state 개념을 사용하여 주문 데이터 변경시 관련 데이터가 변경될 수 있도록 함
    - BullMQ를 활용한 CQRS 패턴 적용

  - What you achieved?/Or what you can do with this result?
    - 기본 4.5m+ MAU에서 SLA(Service Level Agreement) 96% -> 99.9819%
    - 고객 주문 프로세스에 주문 번호 중복 방지, 대규모 트래픽 상황에서 서버 확장 등 안정성이 더해졌습니다.
    - EC2 고정 서버에서 수동으로 rsync를 실행하여 배포하던 배포 프로세스가 일으키던 파일 복사 실패 문제를 개선하여 Docker Image 동시 배포가 가능하고 Blue-Green 배포가 가능해졌습니다.
    - 배포 상황과 배포 버전을 알 수 없던 문제를 개선하여 EKS 모니터링이 가능해졌습니다.
    - 각 서비스 로직이 분리되면서 기능 단위 역할 분리와 빠른 유지 보수가 가능해졌습니다.
    - 주문 하위 주문 섹션으로 분리가 가능해지면서 반품, 환불, 재주문의 프로세스가 많은 브랜드에서 실제적으로 직면한 운영 문제를 해결할 수 있게 되었습니다.
    - 주문 State를 감지할 수 있게되면서 바뀐 데이터를 감지하여 로깅할 수 있도록함

- EKS 마이그레이션 및 스테이징 서버 구축
  - What problem, And what did you?
    - staging서버, 로컬 환경 없이 ftp를 사용하여 로컬 개발을 대체하고 있었음
    - 리눅스의 rsync cli를 사용하여 파일 복사로 배포를 실행하였음
    - 라이브 중인 다수의 서버에 대량 파일을 배포할 때 필연적으로 발생하는 에러 상황
    - 정상적으로 배포가 완료되었는지 알 수 없음
    - EC2에 설치된 네이티브 NGINX, PHP-FPM과 각종 모듈로 인해 Scalable 확장이 불가능
    - 웜업부터 서버 구동까지 10분이 소요되는 상황
  - How solve/develop?
    - 레거시 코드베이스 도커라이징
    - 각 서비스 별 코드베이스 분리
    - 8G의 거대한 코드베이스를 500MB까지 코어 서비스 분리 
    - 고정된 서버에 파일 복사로 수동 배포되던 방식 개선 
    - 네이티브로 설치되어 있던 모듈을 모두 분석하여 도커 파일에 명시하여 표준화함
  - What you achieved?/Or what you can do with this result?
    - 도커이미지를 Cold Start로 Blue-Green 방식의 배포 방법으로 최대 30분의 배포 시간을 3분으로 1/10 시간 단축 
    - 구축 불가능하던 스테이징 서버 구축 성과 
    - 급격하게 증가하는 대규모 트래픽 상황에 대해 Scale-out 서버 증설 전략 적용 가능 
    - ingress-controller를 사용하여 Load Balancer 자동 관리
    - 스팟 인스턴스와 예약 인스턴스를 사용할 수 있게되어 인프라 비용이 절감됨
    - 10분이 소모되던 콜드스타트가 50초 이내로 감축되어 즉각적인 서버 확장이 가능해짐
    - 분당 2,000만 트래픽 소화
    - 카나리 배포, 자동 롤백 가능
    - SLA 96% -> 99.9819%
    - CI/CD 자동화
    - 도커 이미지를 통으로 사용하여 에러 원인 분석 가능

- 판매 채널 통합 연동 API 
  - What problem, And what did you?
    - 자사몰에서 관리하는 상품을 타 채널에 연동하고 주문을 통합관리 하려는 목적
    - 지그재그, 네이버쇼핑에 연동할 수 있는 판매 채널 연동 엔진 작성
    - 타 채널의 상품 및 주문 데이터와 자사몰의 주문데이터가 구조가 다름
    - 자사몰 운영에 영향을 미치지 않고 비동기로 백그라운드에서 동작해야함
    - 서비스가 다운되어도 핵심 서비스는 동작해야함
    - 자사몰 상품의 Payload가 너무 커서 한번에 처리할 수 있는 데이터의 크기가 작음
  - How solve/develop?
    - 비즈니스 로직을 포함한 채널 엔진, 작업을 요청하는 Rest API, Queue에 적재된 내용을 로드하여 작업을 수행하는 Worker 등 MSA 구조로 설계
    - Stateless API로 해시키를 통해 중복 작업 방지 매커니즘 내장
    - 타 채널에 연동할 수 있는 엔진 베이스를 만들고 채널에 맞는 각 엔진을 구현하여 프로바이더로 제공하는 방식 사용
    - BullMQ를 사용하여 비동기 작업 처리 후 요청에 포함된 webhook URL을 통해 callback을 트리거 하는 구조 
    - 자사몰과 타 채널의 데이터 스키마를 구현하고 이것을 매핑하는 구조를 만듬
    - BullMQ(Redis)를 사용하여 큐를 구현함
    - 데이터베이스 사용 없이 서버에서 job을 큐에 등록하고 Scalable한 Consumer가 job은 consume하는 방식
    - 작업이 완료되면 Queue에 등록된 job을 제거하고 webhook을 발송하여 완료 처리
    - CLI 구현하여 개발자의 채널 엔진 확장을 도움
  - What you achieved?/Or what you can do with this result?
    - 자사몰에 등록한 상품을 클릭 한 번으로 타 채널에 연동할 수 있게 함
    - 타 채널에서 판매된 주문을 자사몰에 연동하여 사용할 수 있게 함
    - 자사몰에서 타 채널의 주문을 통합적으로 관리할 수 있게 함
    - Scalable한 consumer구성으로 대량 데이터 동시 연동이 가능함

- PROXMOX 셀프 호스팅 프로젝트
  - What problem, And what did you?
    - 사내에서 K8S를 운영하기 위한 고가용성 학습이 필요함
    - 서버를 직접 여러대 설치할 수 없음
  - How solve/develop?
    - ThinkPad 랩탑을 구매하여 서버 환경을 구성함
    - 하이퍼바이저인 Proxmox를 사용하여 가상 환경을 구성함
    - NAT 네트워크를 구성하여 서버를 확장함
    - 마스터1대, 워커 2대를 위해 총 3대의 vm을 만듬
    - Debian에 쿠버네티스를 설치, 3대의 노드를 통해 쿠버네티스 클러스터를 구축
    - 사내에서 사용하는 스택을 구성하여 yml로 만듬
    - ingress 도입하여 로드밸런싱과 함께 외부 접속으로 서비스 노출
  - What you achieved?/Or what you can do with this result?
    - 클라우드 네트워크에 대한 이해를 통해 고가용성을 가지는 서버를 운영할 수 있게 됨
    - 대규모 트래픽 상황에 대응할 수 있는 인프라 구성에 대해 이해도가 높아짐
    - 클라우드에 익숙한 환경에서 벗어나 베어메탈에 대한 보안 구조를 학습함
- 자체 인증서 생성 프로젝트
  - What problem, And what did you?
    - 사내에서 사용할 서비스에 대한 SSL인증이 필요함
  - How solve/develop?
    - 네트워크 핸드쉐이킹에 대한 이해와 암호화/복호화에 대한 학습
    - OpenSSL 모듈을 통해 자체적으로 서명된 SSL 인증서를 서버에 설치
    - 서명한 RootCA 인증서를 사내 사용자에게 배포
  - What you achieved?/Or what you can do with this result?
    - 사내 인증서를 구매하는데 필요한 월 300만원의 비용을 절감
    - 네트워킹에 대한 이해도를 높여 호스팅 서비스를 하는 비즈니스 성장에 기여함
    - 수동으로 기간마다 구매하던 SSL 인증서 구매 서비스 프로세스 개선하여 자동 결제 및 연장이 가능하도록 함
- 네이버페이 PG연동
  - What problem, And what did you?
    - 라이브 중인 서비스에 새로운 PG사를 연동함
    - 새로운 PG사는 한국에서 가장 결제가 많은 서비스이기 때문에 배포 즉시 결제가 발생함
    - 기존 결제 프로세스 변경 없이 안정적인 서비스 구현이 필요
    - 대규모 트래픽 상황에서 정상적 결제가 동작해야함
  - How solve/develop?
    - 기존 프로세스 분석 후 PG 전략 패턴 적용
    - 결제 완료 프로세스는 별도로 분리 후 동작하도록 구현
    - 결제 완료 후 리다이렉트 되는 프로세스에서 결제 서버에 의도된 결제가 맞는지 주문서와 결제 데이터 검증 프로세스 추가
  - What you achieved?/Or what you can do with this result?
    - 타 PG사 결제에 대해 결제 금액이 변경되는 어뷰징이 일어났을 때 네이버페이 PG는 어뷰징을 할 수 없었음
    - 대규모 트래픽 상황에서도 정상적인 결제가 일어남
    - 자사몰에서 사용하는 쿠폰, 할인 등 가격 정책 적용이 가능함
- Notification API(Email, SMS, Kakaotalk, App Push)
  - What problem, And what did you?
    - php로 각각 작성된 발송 서비스 로직이 정상 수행되지 않을 경우 핵심 로직을 방해
    - 핵심 로직과 관계 없이 비동기로 동작해야함
    - 호출부에서는 한번의 Notification 호출로 각각의 서비스를 실행해야함
    - 발송한 App Push가 24시간까지 소요됨
  - How solve/develop?
    - CQRS 패턴을 적용하여 핵심 로직에서 Notification 메소드를 실행할 경우 Queue에 작업이 등록됨
    - 같은 내용을 여러번 발송하는 것을 방지하기 위해 발송 데이터 전체를 해싱하여 비교함
    - 별도의 발송 서버를 구성하여 동시 대량 발송을 위한 확장이 가능함
    - Consumer를 순간적 확장하여 발송한 알림이 장기간 체류되는 것을 방지함
  - What you achieved?/Or what you can do with this result?
    - 고객이 사이트 운영자가 발송한 알림을 즉시 확인하고 즉각 반응함
    - 같은 내용이 여러번 발송되어 소모되던 고객의 발송 비용 크레딧(SMS, Kakaotalk, App Push) 소모가 30% 감소함
    - 알림 반응으로 인해 마케팅적인 접근이 가능해짐
    - 알림 발송 로직이 핵심 로직을 방해하지 않아 서버의 다운타임이 방지됨
- 테스팅 환경 개선 프로젝트
  - What problem, And what did you?
    - 기존 환경에서 전무하던 테스팅 프로세스
    - 테스팅이 없어서 발생하는 소스코드의 비대화 - 한 파일에 객체화를 하지 않은 프로세스만 3000라인 이상
  - How solve/develop?
    - 주문, 결제 프로세스에서 600개의 테스트 케이스를 정립하여 서비스의 가장 핵심인 50개 케이스에 대한 테스트 생성
    - 로컬 환경이 없어 phpUnit이 동작할 수 있는 self-hosted에 GitHub Actions를 수행함
    - 마스터에 머지할 경우 수행 되도록 구현함
  - What you achieved?/Or what you can do with this result?
    - 테스트 케이스가 존재하는 로직에 대해 배포 후 롤백이 30% 감소함
    - 로직의 실행 여부에 대한 코드 리뷰가 사라짐
- 타입스크립트, 함수형 프로그래밍 스터디
  - What problem, And what did you?
    - 새로운 기능 개발 및 모던 MSA 스택 전향을 위한 타입스크립트 사용이 사내 표준화 되었음
    - 기존의 php, jQuery를 사용하는 스택에서 비즈니스 전략상 빠른 전환이 필요함
  - How solve/develop?
    - 관심있는 동료를 모집하여 4주짜리 사내 스터디를 만듬
    - 주 내용은 타입스크립트의 동작 방식, iterator, generator, Promise, Async/Await, 모나드 등
  - What you achieved?/Or what you can do with this result?
    - 3년차 미만 주니어로 구성된 팀의 프로그래밍 이해도가 향상됨
    - 타입스크립트 사용간 커뮤니케이션 비용이 감소함
    - 기본적인 Promise 동작 방식에 대한 이해로 팀의 비동기 프로그래밍이 가능해짐
- 클린아키텍쳐 스터디
  - What problem, And what did you?
    - MSA를 표준 구조로 하면서 소프트웨어 엔지니어링 방식에 팀 전체의 컨센서스가 필요함
  - How solve/develop?
    - [클린아키텍쳐](https://www.amazon.com/Hands-Dirty-Clean-Architecture-hands-ebook/dp/B07YFS3DNF)를 교재로 사용하여 직접 만드는 형태로 학습
  - What you achieved?/Or what you can do with this result?
    - 새로 만들어진 MSA에 도메인 분리가 철저하게 되고 개발자간 커뮤니케이션 리소스가 감소함
    - 팀 내에서 이와 관련한 논의가 활발하게 진행되어 초기 설계에 반영되었음
    - 3년차 미만 주니어 개발자의 어플리케이션 구조 이해도가 높아져 온보딩이 빠르게 가능했음
- CI/CD 자동화 프로젝트(git-flow)
  - What problem, And what did you?
  - How solve/develop?
  - What you achieved?/Or what you can do with this result?
- 데이터독 페이먼트 이벤트 대시보드 PG사 8개, 고객사 8만
  - What problem, And what did you?
    - EC2가 여러개 파일 복사 배포, 데이터독 데몬이 관리 안되고 있음, 반이 꺼짐
  - How solve/develop?
  - What you achieved?/Or what you can do with this result?
- SQS 마이그레이션
  - What problem, And what did you?
    - 디비를 큐로 사용하고 있었고 정합성을 확인할 수 없어 오류가 발생하는 상황
    - 디비 부하가 너무 심해 다른 서비스에서 쿼리가 불가능한 상황
    - mysql 기능 의존성이 강하게 결합되어 인덱스를 다시 서치하는 등의 기능이 있어 부하를 가중시킴
    - 빠른 작업 처리를 위해 여러개의 프로세스가 생성될 경우 중복처리 되는 현상
    - 프로세스에서 에러가 발생하였으나 강제 종료로 인해 작업이 누락되는 현상
  - How solve/develop?
    - 큐를 쌓고 consume하는 메소드를 sqs를 사용하도록 변경함
    - mysql 기능에 의존하는 메소드를 제거하고 큐 방식을 사용하는 모든 로직을 검사함
    - 강제 종료 발생시 미처리 큐로 분류하여 다시 실행될 수 있도록 조치
    - order by, select 등 특정 상황을 만들어내는 로직을 제거
  - What you achieved?/Or what you can do with this result?
    - 배치잡 처리를 위해 다른 서비스가 희생되는 현상을 제거
    - SQS 뿐만 아니라 RabbitMQ, Kafka 등 다른 큐를 사용할 수 있는 프로바이더 작성
    - 특정 메소드 설정에 따라 등록된 배치잡을 consume하는 결과가 다른 것을 방지하고 서비스가 안정적으로 동작하는 것에 기여
    - 모든 서비스에서 큐를 쌓고 다시 배치로 분배하는 과정이 있었으나 제거하여 프로세스 처리속도 향상
- 스타일 가이드 작성(php, js, ts, pr, commit)
  - What problem, And what did you?
    - 30명의 개발자가 각기 다른 스타일로 각 개발 언어를 사용함
    - 리뷰시, 유지보수시 한번에 파악할 수 없고 각 개발자의 스타일을 파악하는데 시간이 걸림
    - 에러 발생시 즉각적인 롤백이 불가함
  - How solve/develop?
    - 사내 스타일 가이드 커미티를 발족하여 사용하는 개발언어와 PR(규모 포함), Commit 스타일 가이드를 작성함(영어, 한국어)
  - What you achieved?/Or what you can do with this result?
    - PR과 리뷰가 활발해지고 리뷰시에 스타일 관련한 논의가 사라짐
    - 리뷰에 평균 하루가 소요되었으나 1시간 이내로 단축됨
- Oauth 2.0
  - What problem, And what did you?
    - 새로운 MSA 구조에서 메인 코드베이스와 공유할 로그인 인증 부재
    - 메인 시스템에서 로그인 할 경우 OAuth2.0인증을 통해 MSA에서 사용할 수 있는 토큰 발행
  - How solve/develop?
    - accounts 서버에 앱을 등록하여 API를 발행
    - 고객 브라우저에서 고객이 로그인 할 때 1회용 code를 발급
    - 발급된 code를 가지고, 다시 액세스 토큰을 받아 액세스 토큰으로 API 요청
  - What you achieved?/Or what you can do with this result?
    - 여러 스쿼드로 구성된 서비스 운영 상황에서 각 스쿼드 별 MSA 개발 및 배포가 가능해짐
    - 고객이 로그인하는 이벤트를 통해 각 MSA 작동의 모든 권한이 부여됨

- 이조커넥션 IMS(Inbound Management System, ERP)
  - What problem, And what did you?
    - 병원, 제약회사에서 실행하는 임상 실험 참가자 모집을 위한 각 프로젝트 관리 시스템
    - 설문 조사 컴포넌트 빌더 시스템, 게시물-연구-설문조사 연동 기능, 설문조사인바운드 관리, 인사 관리, 광고 스케쥴 관리, 상담리스트엑셀추출 - 10만 Row, 직급별 권한 관리
  - How solve/develop?
    - 실시간 관리가 불가능한 환경에서 운영을 하는 상황에 대처하기 위해 서버 관리 자동화
    - 서버를 상태를 실시간으로 체크하고 오류가 발생할 경우 자동 재부팅
    - Inbound Management System으로 의학연구 상담 플랫폼을 포함하는 소규모 ERP 설계 및 구현
    - Express.js, Angular2+, MySql, Redis 환경으로 작성하여 운영
    - 무중단 운영이 가능하도록 도커라이징 후 nginx를 통해 round-robin 방식으로 로드밸런싱
    - 도커 컨테이너를 통한 blue-green배포
    - PM2환경에서 단일 프로세스로 제공되던 API를 마이그레이션 및 도커라이징을 통해 MSA 환경으로 운영
    - 매일 데이터베이스 전체를 백업하여 클라우드 서버 및 오피스에 보유한 NAS에 이중화 관리하는 시스템을 구축
  - What you achieved?/Or what you can do with this result?
    - 회사에서 수행하는 업무에 대한 자동관리
    - 동일 업무에 대해 데이터 입력 및 생성 시간이 6시간 이상이었으나 30분으로 단축됨
    - 직원별 권한을 분리하여 각 직책에 맞는 업무가 가능해짐
    - 개발자 상주없이 서버 운용이 가능해짐
    - Google Form으로 매번 작성하던 설문조사를 어플리케이션에 통합하여 자체 빌더를 통해 설문지를 작성하고 고객 정보를 수집함
    - 카테고리별 광고 스케쥴 관리가 가능하여 효율적인 업무 운영이 가능해짐
    - 대량 데이터 엑셀 추출의 경우 스트리밍을 사용하여 생성시마다 파일이 생성되는 것을 방지

- 이커머스 보일러 플레이트 제작
  - What problem, And what did you?
    - 패션, 아트, 고급가구, 식음료 등 다수의 이커머스 제작
    - 다수의 사이트를 제작할 경우 비슷한 니즈가 발생하나 작업시마다 서버를 셋팅하고 별도의 프로그래밍 작업이 필요
    - 구현 후 개발자가 없는 경우 비전문가가 운영을 하기 어려움
    - 서버 관리가 어려움
  - How solve/develop?
    - 니즈를 만족시키는 이커머스 기능을 모아 보일러 플레이트를 제작
    - Node.js Module을 활용하여 cli로 설치하는 프레임워크 제작
    - 초기에는 모델 파일이 cli로 복사되는 형태였지만 추후에는 SaaS로 발전
    - 각각의 서비스가 별도로 격리되어야 하기 때문에 도커라이징 후 격리 서버 운영
    - 디자이너가 활용할 수 있도록 웹빌더 형식의 서버 설치형 보일러 플레이트 제작
  - What you achieved?/Or what you can do with this result?
    - 서버 셋업, 기본 기능 구현 등에 소요되던 시간이 7일 -> 30초로 단축
    - 격리된 서버 운영으로 ftp 제공 가능
    - 웹사이트 구현 후 비전문가가 운영 가능
    - Scalable한 아키텍쳐로 접속자 수 급증시 트래픽 자동 감지 후 10초내에 서버 증설 가능
  
- 채율
  - What problem, And what did you?
    - 1000년 역사의 나전칠기 전통 공예 장인들이 만드는 한국 전통 가구, 조 바이든, 빈 살만 등이 소장한 VIP 의전용 기념품 브랜드
    - 여러 지점에서 발주되는 물량을 관리해야함
    - 전통 패턴 관리 시스템이 부재하여 수기로 관리
    - 1만개의 제품 관리를 위한 카테고라이징이 필요
    - 웹사이트 관리자 시스템이 필요
    - 고객별 커스터마이징 카탈로그 생성 시스템 필요
    - VIP 고객 취향 추천 시스템
    - 관리자의 UX를 고려하지않은 관리자 시스템
    - html 파일로 하드코딩 된 웹사이트
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 58개의 카테고리로 나눈 전통 문양 관리 시스템
    - 정확한 카테고리 분류를 통해 구매한 고객의 데이터를 분석하여 알맞은 상품을 추천할 수 있게 함
    - 전 지점의 재고 관리 시스템
    - 장인들이 작품을 디자인 하기 전 분석된 판매 데이터를 통해 전통 문양 패턴 디자인을 제작하는데 도움을 줌
    - 1만개의 제품 리스트를 속도 제한 없이 관리(인덱싱)
    - 고객 맞춤형 카탈로그를 관리자가 제작할 수 있는 시스템 적용
    - 모바일 친화적 환경 구축
  - What you achieved?/Or what you can do with this result?
    - 패턴을 저장하고 잘팔리는 패턴 조합을 만들어서 디자인에 활용했다는 얘기
    - 1만개의 상품과 전통 문양 데이터베이스를 58개 카테고리로 나누고 태그를 활용하여 고객 맞춤형 카탈로그 제작 가능
    - 이전과는 다르게 모바일 환경 친화적으로 변경되어 간단한 링크 공유로 카탈로그 조회 가능
    - 다국어 관리 시스템을 통합하여 관리자에 의해 컨텐츠에 대한 번역관리가 이루어짐
    - 애널리틱스 데이터를 통합하여 광고 관리, 노출 관리가 가능하게 함
- 레아주
  - What problem, And what did you?
    - 전화로 운영하던 환자 수기 예약 시스템
    - 고객 문의 채팅 상담 솔루션
    - 환자 관리 시스템
    - 일본, 중국 환자를 위한 멀티랭귀지 시스템
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 캘린더를 통합한 환자 예약 시스템 구현
    - 환자가 직접 예약을 할 수 있고 예약 별 Quota 부여를 통해 예약 진행시 홀딩 되도록 설계
    - 예약이 몰릴 경우엔 먼저 접속한 사용자가 Quota를 할당 받음
    - Web Socket을 사용하여 채팅 예약 상담 구현
    - 예약 일자 임박의 경우 자동 알림 발송 구현
    - 관리자가 예약을 관리할 수 있는 어드민 시스템 구축
    - 환자 정보와 연동
    - 공지, 예약 등 모든 컨텐츠에 적용되는 멀티랭귀지 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 피부과 진료 환자와 예약을 관리할 수 있음
    - 자동 알림 발송으로 환자가 지속적으로 방문할 수 있도록 함
    - 환자 정보와 연동하여 예약을 관리할 수 있음
    - 알림 시스템으로 아웃바운드 영업이 가능함
    - 일본, 중국 환자 예약률 160% 증가

- 공동체 세움 - 사회법인 로컬커뮤니티 활성화 사업을 위한 공공기관
  - What problem, And what did you?
    - 세분화된 업무 분장으로 인한 부서별 권한관리
    - 후원고객 개인 정보 관리
    - 이미지 용량 및 퀄리티 최적화
    - 후원관리 프로그램
    - 사업 제안서 작성 프로그램
  - How solve/develop?
    - 계정별, 계정 그룹별 스코프 세분화를 구현하여 우선 순위에 따른 계정 권한 관리 시스템 구현
    - 권한이 있는 경우만 개인 정보를 조회하거나 마스킹을 통해 일부 조회되도록 구현
    - 이미지 업로드 시 원본 이미지를 웹용으로 압축하는 과정을 거치고 엣지 서버를 통해 빠른 서브가 가능하도록 구현
    - 공공기관에서 사용하는 도큐먼트 템플릿을 적용하여 간편하게 제안서 작성이 가능한 시스템 구현
    - 후원 고객의 경우 별도의 권한을 부여하여 전용 컨텐츠를 열람할 수 있도록 구현
  - What you achieved?/Or what you can do with this result?
    - 개발자 없이 각 담당부서에서 홈페이지 유지 보수
    - 공공기관 개인정보 운영 정책 통과
    - 별도의 조작없이 고용량 이미지 업로드 및 관리
- 베터솔랩
  - What problem, And what did you?
    - ESG 컨설팅 프로그램
    - 기업 이밸류에이션 시스템 & 데이터 구축
    - 기업 컨설팅 분석자료 자동생성
    - 컨설팅 인보이스 관리 시스템
    - 멤버쉽 구독 컨텐츠
  - How solve/develop?
    - 정기 구독 결제 커머스 구현
    - 컨설팅 항목을 입력하면 자동으로 구성되어 이메일로 발송되는 인보이스 관리 시스템 구현
    - 미리 입력된 가중치로 평가되는 항목을 기입하면 기업의 ESG 점수가 평가되는 시스템 구현
    - 연구원이 입력한 자료를 통해 분석자료 자동 생성
  - What you achieved?/Or what you can do with this result?
    - 수기로 작성되던 연구원의 분석 자료와 개인차가 발생하던 criteria를 표준화함
    - 항목에 따른 컨설팅 인보이스 자동 발행으로 컨설팅 업무 간소화
    - 안정적인 멤버쉽 구독 서비스 적용으로 멤버쉽 전용 컨텐츠 발행
- 아티켈 - Material을 주제로 하는 패션 브랜드 이커머스
  - What problem, And what did you?
    - 관리자가 구현 이후에 사용이 가능한 커스터마이저블 디자인 이커머스
    - Notion-like 블로그 편집기
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 웹빌더와 함께 적용이 가능한 notion-like 텍스트 에디더 제작
  - What you achieved?/Or what you can do with this result?
    - 개발자 없이 각 담당부서에서 홈페이지 유지 보수
    - 쉬운 블로깅 시스템 운영
- 윈도우00 - 센트럴 세인트 마틴 출신 졸업생 3명이 만든 패션 디자인 포트폴리오, 디자인 펀딩 시스템
  - What problem, And what did you?
    - 관리자가 구현 이후에 사용이 가능한 커스터마이저블 디자인 이커머스
    - 온라인 카탈로그 시스템
    - 디자인 펀딩 및 bidding 시스템
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 목표 금액을 설정할 수 있는 상품을 구현하고 구매 프로세스로 목표 금액에 도달할 수 있는 이커머스 구현
    - 가장 높은 금액에 상품을 낙찰할 수 있는 시스템 구현
    - bidding 시스템은 상품이 먼저 구매된 후 경매가 끝나면 낙찰자를 제외한 모두가 환불 되는 구조
  - What you achieved?/Or what you can do with this result?
    - 개발자 없이 홈페이지 디자인 및 상품 관리
    - 온라인 카탈로그 시스템
    - 디자인 펀딩 및 bidding 시스템
- portrait-report - 한국 1위 패션 그룹 출신 디자이너들이 모여 만든 패션 브랜드
  - What problem, And what did you?
    - 여러 화폐, 환율 계산기를 사용하는 글로벌 이커머스 시스템
    - 다국어 관리 시스템
    - 재고관리 시스템
    - 배송관리 시스템
    - 납품 관리 시스템
    - 온라인 재고와 연동된 오프라인 POS 시스템
    - 시즌 오픈 동시 주문 초당 1000건
    - 매출 관리 애널리틱스
    - 방문자 관리 애널리틱스
  - How solve/develop?
    - 도커라이징을 통한 소스코드 가상화와 주문 Queue, 마스터-슬레이브 구조의 데이터베이스를 통한 Scalable한 인프라 구성
    - 번역가 및 운영자가 관리 가능한 멀티 랭귀지 시스템 적용
    - SKU를 기반으로 주문, 배송과 연동되는 재고관리 시스템 구현
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 오프라인 POS 시스템 구현
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 광고 채널 분석이 가능한 방문자 애널리틱스 통합
  - What you achieved?/Or what you can do with this result?
    - 초당 동시 접속 1000건 이상을 소화할 수 있는 이커머스 시스템 구현
    - 관리자 1명이 한 눈에 파악할 수 있는 어드민 시스템 구현
    - 여러 국가에서 사용이 가능한 멀티랭귀지 시스템 구현
- 20DDD - 온라인 피트니스 프로그램
  - What problem, And what did you?
    - 피트니스 프로그램 및 영상 관리
    - 회원 건강정보 데이터 수집 및 트래킹
    - 멤버쉽 관리
    - 피트니스 프로그램 고객용 모바일 어플리케이션
  - How solve/develop?
    - 비메오를 통합하여 유료 멤버쉽 및 각 기수별 영상 접근 권한 제어 구현
    - 개인 건강 정보를 통한 개인 성과 측정
    - 정기 결제 멤버쉽 이커머스 구현
    - 웹뷰 패키징을 통한 모바일 어플리케이션 배포
    - 트레이너가 멤버의 건강 분석 정보를 파악하여 매일 코칭할 수 있는 어드민 프로그램 구현
  - What you achieved?/Or what you can do with this result?
    - 기수별 멤버쉽 정기 결제 구현
    - 프로그램 종료 후 정기 관리 프로그램 커머스 구현
    - 모바일 어플리케이션에서 간편하게 이용이 가능하여 참가율 95% 이상 달성
    - 건강 정보 데이터 분석을 통한 맞춤형 피트니스 프로그램 추천
    - 빠르고 정확한 피트니스 코칭
- 미나손스튜디오 - London College of Fashion 출신 사진작가 포트폴리오 웹사이트
  - What problem, And what did you?
    - 포토 포트폴리오 관리 시스템
    - 포트폴리오 커스터마이징 및 발송 시스템
    - 고해상도 고용량 사진 포트폴리오 관리
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 이미지 업로드 시 원본 이미지를 웹용으로 압축하는 과정을 거치고 엣지 서버를 통해 빠른 서브가 가능하도록 구현
    - 포트폴리오 발행 어드민 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 쉽고 빠르게 포트폴리오를 구성하여 대상 고객에게 발송 가능
    - 고해상도 이미지 업로드시에도 서버 용량이 자동 관리되며 빠른 웹사이트 로딩이 가능
    - 별도의 개발없이 관리가 가능한 포트폴리오 웹사이트
- 센트앤센티먼트 - 프래그런스 발주 시스템
  - What problem, And what did you?
    - 베이스노트, 미들노트, 탑노트로 나뉘어지는 향기를 고객이 커스터마이징할 수 있는 주문 시스템
    - 조합에 따른 대량의 옵션 설정 및 관리
    - 향기 옵션별 SKU 부여 및 관리
    - 옵션별 재고관리 시스템
    - 배송관리 시스템
    - 납품 관리 시스템
    - 매출 관리 애널리틱스
    - 새로운 향기 조합 자동 추천
  - How solve/develop?
    - Visitor 패턴 사용으로 Depth 제한이 없는 루프 구현으로 옵션 출력
    - SKU를 기반으로 주문, 배송과 연동되는 재고관리 시스템 구현
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 카테고리 분석을 통해 어울리는 향기에 가중치를 부여하고 결과값이 높은 향기를 추천
  - What you achieved?/Or what you can do with this result?
    - 유저의 자유로운 향기 조합 주문
    - 복잡한 판매 옵션을 한눈에 파악하여 납품이 가능한 어드민 시스템 구현
    - 주문에 따른 옵션별 재고 관리
    - 새로운 향기 조합 상품화
- 유지 - 디자인 이커머스
  - What problem, And what did you?
    - 디자인 이커머스
    - 다수의 납품 채널
    - 재고관리 시스템
    - 배송관리 시스템
    - 납품 관리 시스템
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - SKU를 기반으로 주문, 배송과 연동되는 재고관리 시스템 구현
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 광고 채널 분석이 가능한 방문자 애널리틱스 통합
  - What you achieved?/Or what you can do with this result?
    - 초당 동시 접속 1000건 이상을 소화할 수 있는 이커머스 시스템 구현
    - 관리자 1명이 한 눈에 파악할 수 있는 어드민 시스템 구현
    - 여러 국가에서 사용이 가능한 멀티랭귀지 시스템 구현
- 레이블리스 - 디자인 이커머스, 앱 제작
  - What problem, And what did you?
    - 디자인 이커머스
    - 다수의 납품 채널
    - 재고관리 시스템
    - 배송관리 시스템
    - 납품 관리 시스템
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - SKU를 기반으로 주문, 배송과 연동되는 재고관리 시스템 구현
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 광고 채널 분석이 가능한 방문자 애널리틱스 통합
  - What you achieved?/Or what you can do with this result?
    - 초당 동시 접속 1000건 이상을 소화할 수 있는 이커머스 시스템 구현
    - 관리자 1명이 한 눈에 파악할 수 있는 어드민 시스템 구현
    - 여러 국가에서 사용이 가능한 멀티랭귀지 시스템 구현
- 우트 - 키즈 편집샵, 예치금 시스템
  - What problem, And what did you?
    - 디자인 이커머스
    - 다수의 브랜드 채널
    - 브랜드별 매출 관리 시스템
    - 예치금 월렛 시스템
  - How solve/develop?
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 광고 채널 분석이 가능한 방문자 애널리틱스 통합
    - 예치금 로그 및 입출금 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 브랜드별 담당자가 관리 가능한 매출 관리 시스템 및 매출 통합 분석
    - 복잡한 예치금을 관리자가 손쉽게 관리 가능
- 바고클로딩
  - What problem, And what did you?
    - 디자인 이커머스
    - 다수의 납품 채널
    - 재고관리 시스템
    - 배송관리 시스템
    - 납품 관리 시스템
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - SKU를 기반으로 주문, 배송과 연동되는 재고관리 시스템 구현
    - 다수의 판매 채널에 납품을 관리할 수 있는 관리자 시스템 구현
    - 송장 자동 발급, 송장 추적 시스템 통합
    - 판매 채널, 온라인 판매, 오프라인 POS 판매를 통합한 매출 분석 애널리틱스 구현
    - 광고 채널 분석이 가능한 방문자 애널리틱스 통합
  - What you achieved?/Or what you can do with this result?
    - 초당 동시 접속 1000건 이상을 소화할 수 있는 이커머스 시스템 구현
    - 관리자 1명이 한 눈에 파악할 수 있는 어드민 시스템 구현
    - 여러 국가에서 사용이 가능한 멀티랭귀지 시스템 구현
- MTG-SHOP
  - What problem, And what did you?
    - 예치금 월렛 시스템
    - 온라인 와인 커머스
    - 와인 추천
    - 고객 데이터 분석 및 추천 시스템
    - 오프라인 POS프로그램
    - 주류 판매는 법적인 챌린지가 필요했음
      - 온라인 판매시 대면 신분증 확인 및 기록
      - 온라인 구매 배송시 전체 주문 금액 중 음식 가액 50%이상
      - 가입시 모바일 본인 인증 필수
    - 15개 이상 와인 수입사 납품 및 정산 관리
  - How solve/develop?
    - 웹빌더 시스템을 적용하여 추후 디자인을 손쉽게 유지보수 할 수 있도록 구현
    - 예치금 로그 및 입출금 시스템 구현
    - 와인 카테고라이징 시스템 구현
    - 고객 구매 정보 데이터 분석 시스템 구현
    - 바코드로 관리하는 재고 관리 시스템 구현
    - 15개 이상의 와인 수입사에서 납품하는 모든 와인 데이터베이스 구성
    - 이커머스의 데이터를 사용하는 오프라인 POS 시스템 구현
    - 주류 판매 법적 요건을 충족하는 주문 Validation 시스템
    - 배송 주문 케이스의 경우 신분증 등록 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 법적인 주류 온라인 판매 요건을 충족하는 이커머스 시스템 구현
    - 와인 데이터와 고객 데이터를 분석하여 어려운 와인을 쉽게 추천하는 시스템 적용
    - 오프라인 매장에 납품되는 와인을 관리하고 정산 및 순이익을 계산할 수 있는 커머스 시스템 구현
    - 예치금을 통해 원클릭 결제가 가능한 이커머스 구현
- 건강검진병원관리시스템
  - What problem, And what did you?
    - 건강검진 예약 시스템
    - 병의원 연동 환자정보
    - 위치기반 병원 검색 시스템
    - 병의원결제분납시스템
  - How solve/develop?
    - 고객이 PG사를 통해 결제하면 분납금이 자동으로 계산되고, 병의원에 결제할 금액이 계산되어 정산금을 확인할 수 있는 시스템 구현
    - 건강검진 예약 시스템 구현
    - 브라우저 GPS 정보 기반 병원 검색 구현
    - 병원에서 사용하는 검진 예약 어드민 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 고객이 건강 검진 상품을 골라 가까운 병원을 검색하고 예약할 수 있는 시스템을 구현
    - 예약된 정보는 병원에서 어드민을 통해 확인하는 시스템
    - 종합 건강 검진은 비용이 크지만 분할 납부 시스템을 통해 병원에 비용 선지급 후 건강 검진을 받고 고객은 금액을 분할하여 납부
- 가찌스튜디오 - 한국예술종합대학 출신 건축디자이너 그룹
  - What problem, And what did you?
    - 건축 설계는 규모가 큰 작업이기 때문에 인보이스 발행에 시간이 많이 소요됨
    - 물리 하드디스크 드라이브 및 하드 프린트 카피로 관리되던 도면의 버전 관리 필요성
    - 건축 디자인 포트폴리오 웹사이트
  - How solve/develop?
    - 표준화된 인보이스 자동 발행 및 관리 시스템 구현
    - 클라우드 드라이브 업로드 통한 도면 파일 버전 관리 시스템 구현
    - 건축 디자인 포트폴리오 웹사이트 및 카탈로그 시스템 구현
  - What you achieved?/Or what you can do with this result?
    - 표준화된 인보이스 발송 시스템을 사용하여 건축주에게 견적이 발송되고 수정된 이력을 관리할 수 있는 시스템 구현
    - 도면 오출력 및 미스커뮤니케이션을 방지하고 최신화된 도면 파일을 확인 가능
    - 건축 디자인 포트폴리오를 건축가가 직접 구성하여 웹사이트에 게시 가능
    - 건축주가 원하는 포트폴리오를 카탈로그로 구성하여 발송 가능
- 이웃집한의원
  - What problem, And what did you?
    - 신장전문 한의원 환자정보 관리 시스템
    - 검진 예약 시스템
    - 환자 정보 관리
    - 한의사가 직접 발행하는 멤버쉽 컨텐츠 구독
  - How solve/develop?
    - 검진 예약 시스템 구현
    - 병원에서 사용하는 검진 예약 어드민 시스템 구현
    - 환자 치료 정보 관리 시스템
    - 정기 결제 멤버쉽 이커머스 구현
  - What you achieved?/Or what you can do with this result?
    - 고객이 검진 빠르게 예약할 수 있는 시스템을 구현
    - 예약된 정보는 병원에서 어드민을 통해 확인하는 시스템
    - 한의사가 직접 발행한 정보를 가입된 멤버쉽을 통해 구독할 수 있는 시스템 구현
- 다원efr
  - What problem, And what did you?
    - First Aid Training 교육 및 네트워크 마케팅
    - 강사 스케쥴 및 예약 시스템
    - 관련 용품 판매 관리 시스템
    - 강사용 안드로이드 앱 패키지 제작
  - How solve/develop?
    - 
  - What you achieved?/Or what you can do with this result?
    - 

- 서울시 BIS(Bus Information System) - bus.go.kr, Open API, 서울시 대중교통 앱
  - What problem, And what did you?
    - 서울시 전체에서 운영되는 버스 운행 기록 관리 및 Open API 제공
  - How solve/develop?
    - 실시간으로 동작하는 비즈니스 로직의 효율성 검증이 필요
  - What you achieved?/Or what you can do with this result?
    - 
- 아모레퍼시픽 PMS(Project Management System)
  - What problem, And what did you?
    - 아모레퍼시픽 IT 프로젝트 관리 프로그램 신규 개발
  - How solve/develop?
    - Express.js기반의 Sails.js 프레임워크로 백엔드 API 작성
  - What you achieved?/Or what you can do with this result?
    - 대규모 프로젝트 관리 및 다수의 관리자 접속시 효율적인 프로세스 실행이 가능한 비동기 비즈니스 로직 작성
- 아주 GPS 기반 관제 시스템
  - What problem, And what did you?
    - 아주 레미콘에서 사용할 레미콘 발주 관리, 배송, 입출차 관리 프로그램 신규 제작
    - 차량 위치 관제, 납품 정보 이력 조회, 채권 조회
  - How solve/develop?
    - Spring Framework를 기반으로 웹을 제작하고 웹뷰를 통해 안드로이드 앱과 윈도우 앱 제작
    - Spring Framework, Maven, MyBatis, Oracle 환경
    - MVC 패턴을 적용하여 뷰에 적용되어 있던 모든 로직을 제거하고 새로운 구조를 작성함
    - 프론트엔드와 백엔드 분리
  - What you achieved?/Or what you can do with this result?
    - 풀스택 개발자로 MVC 컴포넌트 단위 개발을 진행하여 2개월의 프로젝트 단축 효과
  
## 🛠️ Technologies & Tools

### Everyday Use (Advanced)
<p>
<!-- GitHub Actions  -->
<img src='https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&amp;logo=githubactions&amp;logoColor=white' />
<!-- MongoDB  -->
<img src='https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&amp;logo=mongodb&amp;logoColor=white' />
<!-- MySQL  -->
<img src='https://img.shields.io/badge/mysql-%2300000f.svg?style=for-the-badge&amp;logo=mysql&amp;logoColor=white' />
<!-- NestJS  -->
<img src='https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&amp;logo=nestjs&amp;logoColor=white' />
<!-- NodeJS  -->
<img src='https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&amp;logo=node.js&amp;logoColor=white' />
<!-- Yarn  -->
<img src='https://img.shields.io/badge/yarn-%232C8EBB.svg?style=for-the-badge&amp;logo=yarn&amp;logoColor=white' />
<!-- AWS  -->
<img src='https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&amp;logo=amazon-aws&amp;logoColor=white' />
<!-- JavaScript  -->
<img src='https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&amp;logo=javascript&amp;logoColor=%23F7DF1E' />
<!-- PHP  -->
<img src='https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&amp;logo=php&amp;logoColor=white' />
<!-- TypeScript  -->
<img src='https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&amp;logo=typescript&amp;logoColor=white' />
<!-- Linux  -->
<img src='https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&amp;logo=linux&amp;logoColor=black' />
<!-- Docker  -->
<img src='https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&amp;logo=docker&amp;logoColor=white' />
<!-- Kubernetes  -->
<img src='https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&amp;logo=kubernetes&amp;logoColor=white' />
<!-- Git  -->
<img src='https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&amp;logo=git&amp;logoColor=white' />
<!-- Bitbucket  -->
<img src='https://img.shields.io/badge/bitbucket-%230047B3.svg?style=for-the-badge&amp;logo=bitbucket&amp;logoColor=white' />
<!-- Datadog  -->
<img src='https://img.shields.io/badge/datadog-%23632CA6.svg?style=for-the-badge&amp;logo=datadog&amp;logoColor=white' />
<!-- JWT  -->
<img src='https://img.shields.io/badge/JWT-black?style=for-the-badge&amp;logo=JSON%20web%20tokens' />
<!-- Yarn  -->
<img src='https://img.shields.io/badge/yarn-%232C8EBB.svg?style=for-the-badge&amp;logo=yarn&amp;logoColor=white' />
<!-- Linux  -->
<img src='https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&amp;logo=linux&amp;logoColor=black' />
<!-- ESLint  -->
<img src='https://img.shields.io/badge/ESLint-4B3263?style=for-the-badge&amp;logo=eslint&amp;logoColor=white' />
<!-- Jest  -->
<img src='https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&amp;logo=jest&amp;logoColor=white' />

</p>

### Know How to Use (Intermediate)

<p>
<!-- RabbitMQ  -->
<img src='https://img.shields.io/badge/rabbitmq-FF6600?style=for-the-badge&amp;logo=rabbitmq&amp;logoColor=white' />
<!-- Oracle  -->
<img src='https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&amp;logo=oracle&amp;logoColor=white' />
<!-- GraphQL  -->
<img src='https://img.shields.io/badge/-GraphQL-E10098?style=for-the-badge&amp;logo=graphql&amp;logoColor=white' />
<!-- Grafana  -->
<img src='https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&amp;logo=grafana&amp;logoColor=white' />
<!-- Prometheus  -->
<img src='https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&amp;logo=Prometheus&amp;logoColor=white' />

</p>

### Under Development (Basic)
<p>
<!-- Flutter  -->
<img src='https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&amp;logo=Flutter&amp;logoColor=white' />
<!-- Terraform  -->
<img src='https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&amp;logo=terraform&amp;logoColor=white' />

</p>

## 🏋️‍♂️ Endeavors
![aws-certified-solutions-architect-associate](https://github.com/user-attachments/assets/c10cae8a-5609-47b4-8828-2134744b5e45)