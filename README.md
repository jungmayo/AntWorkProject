# AntWork - 그룹웨어 프로젝트

![header](https://capsule-render.vercel.app/api?type=wave&color=gradient&height=250&section=header&text=🖇️AntWork%20Project🖇️&fontSize=70&fontAlign=50)

## 📖 프로젝트 개요
AntWork는 롯데 그룹의 사내 협업 플랫폼을 현대화하고, 실무 환경과 유사한 경험을 제공하기 위해 설계된 **풀스택 웹 애플리케이션**입니다.  
효율적인 업무 처리를 위한 **전자 결재 시스템**, **실시간 협업**, **데이터 관리** 등 **비즈니스 최적화**를 목표로 합니다.

---

## 🎯 프로젝트 목표
1. **사용자 중심의 그룹웨어 제공**  
   - 직관적이고 반응형 UI/UX 설계.
2. **실시간 협업 기능 강화**  
   - 채팅, 파일 공유, 일정 관리.
3. **확장 가능한 시스템 설계**  
   - 현대적 기술 스택을 활용하여 유연한 구조 구축.

---

## 🛠️ 기술 스택

### **Frontend**
- **React**: 사용자 인터페이스 개발.
- **TypeScript**: 코드 안정성과 유지보수성 향상.
- **TailwindCSS & Sass**: 빠른 개발과 일관된 스타일링.
- **Zustand**: 상태 관리.
- **Axios**: 효율적인 API 요청 처리.

### **Backend**
- **SpringBoot**: 비동기 이벤트 기반 서버.
- **MySQL**: 관계형 데이터 저장소.
- **MongoDB**: NoSQL 데이터 저장소.
- **Redis:**: 캐싱 및 세션 관리.
- **JWT**: 사용자 인증 및 세션 관리.
- **Stomp**: WebSocket 기반의 실시간 통신.
- **JWT**: 사용자 인증 및 세션 관리.

### **DevOps & Tools**
- **GitHub Actions**: CI/CD 파이프라인 자동화.
- **AWS EC2**: 서버 배포.
- **Slack**: 팀 커뮤니케이션.
- **Postman**: API 테스트.
- **Notion & Google Sheets**: 작업 관리와 일정 공유.

---

## 🧑‍💻 팀원 소개
| 이름          | 역할                           | 주요 담당 기능                                 |
|---------------|--------------------------------|-----------------------------------------------|
| **최준혁(팀장)** | 프로젝트 관리, 관리자 기능, 전자결재 및 유저기능, 백 서버 배포 | 프로젝트 기획 및 계획 수립, 프로젝트 및 일정관리, 로그인/회원가입/약관, 관리자(팝업/알림/결재/부서관리/멤버접근로그), 전자결재(휴가&출장신청), 백 서버 배포 및 관리|
| **김민희**     | 게시판 기능                    | 게시판 글쓰기/전체목록/페이징, 첨부파일 업로드/다운로드, 글 상세보기/검색/수정/삭제, 댓글입력/수정/삭제/비밀댓글 |
| **정지현**     | 드라이브 기능                  | 드라이브 폴더 생성 및 수정, 드라이브 폴더 삭제/복원, 공유드라이브 구현 |
| **박경림**     | 채팅 기능                      | 채팅 채널 생성/초대/나가기, DM, 채팅 메세지 전송/조회/검색, 채팅 금칙어 설정 및 필터링 |
| **황수빈**     | 페이지 기능                    |페이지 생성/삭제/복구협업자 추가 & 실시간 공유 및 수정, 페이지 템플릿 생성 및 공유, 문의 작성/답변/조회|
| **하정훈**     | 캘린더 기능, 유저기능           | 캘린더 일정관리 및 수정 ,아이디&비밀번호 찾기 ,사용자 정보 수정 ,관리자 메인 & 유저 관리 |
| **강은경**     | 프로젝트 기능, 프론트 서버 배포 | 프로젝트 기능 구현, 협업자 추가 & 실시간 공유 및 수정, 프로젝트 설정 기능 구현 , 프론트 서버 배포 및 관리 |

---

## 📅 개발 일정
**2024년 11월 18일 ~ 2024년 12월 27일 (6주)**

1. **11월 3주차**: 요구사항 분석 및 화면 설계
2. **11월 4주차**: 프론트 화면 구현, DB 설계 
3. **12월 1주차**: 사용자 중심 주요 기능 개발
4. **12월 2주차**: 통합 테스트 및 리팩토링
5. **12월 3주차**: 최종 검토 및 배포

---

## 🏗️ 시스템 설계

### **아키텍처**
- **프론트엔드와 백엔드 분리**: React 기반 SPA와 RESTful API 연동.
- **3계층 구조**: Controller, Service, Repository.

---

## 🚀 주요 기능
#### 사용자 기능
- **회원가입/약관**: 관리자 멤버 초대를 통한 이메일로 토큰을 실은 회원가입 링크를 통한 가입, 각종 유효성 검사 진행
- **로그인**: JWT 토큰 인증 방식으로 JwtProvider를 통한 토큰 관리, JwtAuthenticationFilter를 통한 검증 진행 후 AccessToken -> 로컬 스토리지, RefreshToken -> Http-Only 저장 후 Zustand로 인증정보 관리 
- **유저 정보 수정**: 이름, 이메일, 프로필 이미지 등 유저 정보 수정
- **아이디/비밀번호 찾기**: 이메일 인증을 통한 아이디, 비밀번호 찾기 및 재설정 가능 

#### 관리자 기능
- **회원 관리**: 멤버 초대, 직위 변경, 멤버 삭제, 상태별 조회, 비밀번호 초기화
- **팝업 관리**: 팝업 추가, 팝업 수정, 팝업 삭제, 팝업 보기, Redis를 사용한 _일간 안보기 캐싱처리  
- **부서 관리**: 부서 생성, 부서 수정, 부서 내 소속 유저 드래그 앤 드랍으로 부서 이동, 부서 삭제(삭제시 소속 유저 다른 부서 이동)
- **근태 관리**: 유저 출,퇴근 처리, 근태 출력, 검색 및 필터링 기능, 누적시간 확인, 주간 월간별 출력
- **멤버 접근 로그**: Spring AOP 사용 특정 PointCut으로 로그 남길 메서드 지정, Kafka와 MongoDB를 사용한 대규모 데이터 효과적으로 처리
- **알림 관리**: 회사 전체 부서 특정 유저별 알림 전송(웹 소켓을 사용한 실시간 알림 처리), 보낸 알림 히스토리 출력
- **전자 결제**: 결제 상태에 따라 필터링 구분, 결제 승인 및 반려 처리, 결제 담당자는 유저 결제 요청시 웹소켓으로 실시간 알림 구현 
  
#### 게시판 기능
- **글 작성**: 제목, 본문 작성 및 첨부파일 업로드
- **글 수정**: 게시글 편집 가능
- **글 삭제**: 게시글 삭제 
- **댓글 관리**: 댓글 추가/수정/삭제, 비밀댓글 기능 
- **첨부파일 관리**: 파일 업로드/다운로드
- **검색 및 필터링**: 제목, 작성자, 내용별 검색

#### 캘린더 기능
- **일정 추가**: 이벤트 생성, 알림 설정
- **일정 수정**: 일정 수정 및 재할당
- **일정 삭제**: 일정 삭제 및 복구
- **공유 캘린더**: 부서별/팀별 캘린더 공유
- **언어 변경**: 캘린더 내 사용 언어 변경
- **동기화**: FullCalendar API 사용 

#### 드라이브 기능
- **파일 업로드**: 개별 파일 업로드, 대용량 지원
- **파일 다운로드**: 실시간 동기화된 파일 제공
- **폴더 관리**: 폴더 생성/이동/삭제
- **권한 설정**: 읽기/쓰기 권한 관리
- **파일 복구**: 삭제된 파일 복원 기능
- **드라이브 설정**: 휴지통 복원가능 기간 설정

#### 프로젝트 기능
- **프로젝트 생성**: 제목, 목표, 협업자 추가.
- **진행 상태 관리**: Kanban 보드 스타일 상태 변경.
- **문서 관리**: 프로젝트별 문서 첨부 및 공유.
- **멤버 역할 설정**: 멤버별 역할 및 권한 관리.
- **통계**: 프로젝트 진행 상태 통계 제공

#### 페이지 기능
- **페이지 생성**: 템플릿 선택 및 사용자 지정
- **페이지 삭제 및 복구**: 잘못된 페이지 복구 가능
- **공유 템플릿 관리**: 부서별 템플릿 공유
- **공유 페이지**: 공유자 추가해서 공유페이지 추가 및 실시간 수정사항 확인가능
  
####  채팅 기능
- **DM (Direct Message)**: 개인 대화 기능
- **그룹 채팅(채널)**: 팀 채팅방 생성
- **파일 공유**: 실시간 파일 전송
- **알림**: 새로운 메시지 알림
- **읽음 확인**: 읽은 메시지 여부 표시

---

## 🎥 기능 시연
[시연 영상 바로가기](https://www.youtube.com/watch?v=awnQofAVuoo)

---

## 🤝 질문 및 피드백
- **정지현**: (wlgus5946@gmail.com)

---

## 💎 배웠던 점
1. **폴더,파일의 계층 구조 구축**
   - 트리구조를 활용해 하위의 항목들을 생성 및 조회하는 개념을 익혔습니다.
   - 논리적,물리적 경로에 대한 개념을 학습하였고 재귀적 함수를 통해 폴더 이동을 경험했습니다.
2. **효율적인 데이터 관리와 성능**  
   - MongoDB를 사용해 성능조회 속도를 향상을 경험했습니다
3. **팀워크와 협업의 중요성**
   - 역할을 명확히 분배하고 팀원들과의 소통을 통해 프로젝트를 효율적으로 진행하는 방법을 배웠습니다.
   - Notion과 Google Sheets를 사용하여 일정과 작업을 체계적으로 관리하며 협업 도구의 중요성을 실감했습니다.
