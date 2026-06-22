# Kwak Daehoon - Frontend Developer

<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/rMUVpTN.jpeg" alt="Profile" width="180" style="border-radius: 12px;">
    </td>
    <td style="padding-left: 24px;">
      <h3>Contact</h3>
      <ul>
        <li><b>이름:</b> 곽대훈</li>
        <li><b>Email:</b> eogns6595@naver.com</li>
        <li><b>GitHub:</b> <a href="https://github.com/Kwak-DH">github.com/Kwak-DH</a></li>
        <li><b>Notion:</b> <a href="https://strong-iodine-bf5.notion.site/1813ffb1f473808b9332cb5b73ca59bf?pvs=4">kdh's notion</a></li>
        <li><b>Blog:</b> <a href="https://eogns6595.tistory.com/">Tistory</a></li>
      </ul>
      <h3>About</h3>
      <p>Vue 3 기반 실무형 웹 애플리케이션 개발에 집중하고 있는 프론트엔드 개발자입니다.<br>
      복잡한 통계 데이터 시각화, 권한 기반 관리자 시스템, AI 연동 인터페이스 등<br>
      단순 CRUD를 넘어선 업무형 시스템 개발 경험을 보유하고 있습니다.</p>
      <ul>
        <li>🏆 프론트엔드 구현 및 백엔드 개발을 위한 풀스택 인재양성 <b>최우수상</b></li>
        <li>🏆 프론트엔드 구현 및 백엔드 개발을 위한 풀스택 인재양성 <b>특모범상</b></li>
        <li>🎓 한국소프트웨어인재개발원 (2024.06 ~ 2024.12)</li>
        <li>🌱 현재 학습 중: Spring Boot, Node.js, React</li>
      </ul>
    </td>
  </tr>
</table>

---

## Tech Stack

| 분류 | 기술 |
|------|------|
| **Frontend** | Vue 3 (Composition API, `<script setup>`), React, JavaScript (ES6+) |
| **State / Routing** | Vuex, Vue Router |
| **Data Visualization** | Chart.js (Bar, Doughnut, Stacked, Mixed, Drill-down) |
| **Backend** | Spring Boot, Node.js, MyBatis |
| **Database** | MySQL, PostgreSQL |
| **HTTP / API** | Axios, REST API |
| **Style** | CSS3, SCSS, Scoped CSS |
| **Tools** | Git, GitHub, Figma, VS Code, IntelliJ IDEA, Eclipse, Fork, Gitlab, Postman, DBeaver, Cursor |

---

## Projects

### 1. EOSA - AI 기반 감사 분석 플랫폼

> 조선시대 암행어사(御史) 제도에서 착안한 AI 감사 분석 웹 애플리케이션

**기간:** 2026.02 ~ 06  
**역할:** 프론트엔드 개발 전담  
**링크:** [eosa.ai](https://eosa.ai)

**기술 스택**

`Vue 3` `Composition API` `Vuex` `Vue Router` `Axios` `Chart.js` `Scoped CSS`

**주요 구현 내용**

- Header / Footer / HomeView / AdminView / MyPage 전 영역 컴포넌트 설계 및 구현
- `loginType` (ADMIN / USER) Vuex 상태 기반 조건부 네비게이션 분기 처리
- 화이트 카드 레이아웃과 `#2563eb` 어센트 컬러 기반 일관된 디자인 시스템 적용
- Noto Sans KR 폰트 기반 한국어 최적화 타이포그래피 구성
- **AI 채팅 기능 통합:** 채팅방 생성 / 조회 / 삭제 / 목록 관리 등 실서비스 수준의 AI 대화 흐름을 EOSA 내부 기능으로 구현
  - 첫 질문 입력 시점에만 채팅방 생성 — 빈 방 누적 방지
  - 질문 첫 28자를 채팅방 제목으로 자동 변환 (공백 정리 포함)
  - 타이핑 애니메이션: AI 응답을 글자 단위로 순차 출력
  - `nextTick()` 활용 자동 스크롤 처리
  - 반응형 레이아웃: 데스크탑(좌우 분할) / 모바일(상하 구조) 대응

**AI 채팅 구현 흐름**

```
질문 입력 → 사용자 메시지 출력 → askAi API 호출 → AI 응답 수신 → 타이핑 애니메이션 출력
```

**시연 GIF**

> 오픈 전 샘플 페이지 기준 — 현재 서비스와 구성 동일

| 기능 | 미리보기 |
|------|----------|
| 메인 페이지 | ![eosamain](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/eosamain.gif) |
| AI 채팅 페이지 | ![eosa_chat](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/eosa_chat.gif) |
| 통계 페이지 | ![eosa_static](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/eosa_static.gif) |

---

### 2. PCOW - 내부통제 자가점검 솔루션

> 리스크 데이터 시각화와 체크리스트 기반 자가점검 기능을 갖춘 기업용 관리자 시스템

**기간:** 2025.03 ~ 09  
**링크:** [pcow.ezqar.com](https://pcow.ezqar.com)  
**역할:** 프론트엔드 개발 전담

**기술 스택**

`Vue 3` `Composition API` `Vue Router` `Axios` `Chart.js` `SCSS`

**주요 구현 내용**

- **권한 기반 통계 시스템:** user / admin / sAdmin 3단계 권한에 따라 API 및 화면 구조 분기
- **Drill-down 차트 구조:** 부서 통계 클릭 → 담당자 통계 → 리스크 상세까지 단계적 탐색 구현
- **다양한 차트 구현:** Doughnut / Bar / Stacked Bar / Mixed Dual Axis / Dynamic Chart
- **체크리스트 시스템:** 3점 이하 항목 입력 시 개선사항 필수 작성 조건 기반 렌더링
- **공통 formatter 함수:** API마다 다른 key 구조를 차트 공통 형식으로 변환해 재사용성 확보

**트러블슈팅**

| 문제 | 원인 | 해결 |
|------|------|------|
| 컴포넌트 조건문 복잡도 증가 | 하나의 컴포넌트에서 전 권한 처리 시도 | 권한 기준 컴포넌트 분리 + API 역할 명확화 |
| API 데이터 구조 불일치 | 응답 key 값이 API마다 상이 | 공통 `formatChartData()` formatter 작성 |

**시연 GIF**

| 기능 | 미리보기 |
|------|----------|
| Chart.js 샘플 차트 구현 | ![pcow_samplechart](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/pcow_samplechart.gif) |
| 관리자 통계 차트 (마스킹 처리) | ![pcow_uadminstac](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/pcow_uadminstac.gif) |

---

### 3. ICIK - 한국내부통제협회 리스크 관리 시스템

> 체크리스트 자가점검부터 통계 대시보드까지 내부통제 업무 전반을 디지털화한 관리자 플랫폼

**기간:** 2025.07 ~ 12  
**링크:** [icikorea.kr](https://icikorea.kr)  
**역할:** 프론트엔드 개발 전담

**기술 스택**

`Vue 3` `JavaScript` `Vue Router` `Axios` `Chart.js` `Kakao Maps API` `CSS3`

**프로젝트 구조**

```
src/
├── api/
├── components/
├── pages/
├── router/
├── layouts/     ← Router 기반 Layout 분리 (Header / Content / Footer)
├── assets/
└── styles/
```

**주요 구현 내용**

- **권한 기반 관리자 시스템:** 일반 사용자 / admin / sAdmin별 조회 데이터 및 화면 구성 분리
- **리스크 관리:** 리스크 점수 및 잔여 리스크 점수 동시 관리, 부서·담당자별 데이터 조회
- **체크리스트 자가점검:** 3점 이하 항목 개선사항 강제 입력 — 실무 내부통제 프로세스 반영
- **통계 대시보드:** 리스크 분포도(LOW/MEDIUM/HIGH), 부서별/담당자별 평균, 완료율 등 종합 시각화
- **Drill-down 대시보드:** 전체 부서 → 특정 부서 → 담당자 → 리스크 상세까지 단계별 탐색
- **위험도 시각화:** LOW(1,2점) / MEDIUM(3점) / HIGH(4,5점) 기준 색상 분류 및 프로그레스 바 표현
- **팝업 이미지 기능:** 메인 페이지 공지/배너 팝업 구현
- **카카오 지도 API:** 협회 소개 페이지 내 지도 연동
- **설문조사 / 역량진단:** 진단 절차 페이지 및 진단 결과 페이지 구현
- **게시판:** 게시글 목록 및 상세 조회 구현
- **용어사전 / 매트릭스 사전:** 클릭 시 드롭다운 전개, 라디오 버튼 선택에 따라 샘플 문서 동적 표시

**시연 GIF**

| 기능 | 미리보기 |
|------|----------|
| 어드민 로그인 및 메인 이동 | ![admin1](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik_admin1.gif) |
| 어드민 게시글 수정 / 삭제 | ![admin2](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik_admin2.gif) |
| 메인 페이지 및 팝업 기능 | ![icik1](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik1.gif) |
| 협회 소개 및 카카오 지도 | ![icik2](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik2.gif) |
| 설문조사 페이지 | ![icik3](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik3.gif) |
| 역량진단 절차 | ![icik4](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik4.gif) |
| 역량진단 결과 | ![icik5](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik5.gif) |
| 게시판 | ![icik6](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik6.gif) |
| 용어사전 / 매트릭스 사전 | ![icik7](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/icik7.gif) |

---

### 4. ACE - 감사인 역량진단 시스템

> 리스크 평가 → 점검 → 통계 → 분석 흐름이 유기적으로 연결된 기업형 내부감사 통합 플랫폼

**기간:** 2025.12 ~ 2026.03  
**링크:** [ace.ezqar.com](https://ace.ezqar.com)  
**역할:** 프론트엔드 개발 전담

**기술 스택**

`Vue 3` `Composition API` `Vue Router` `Vite` `Axios` `Chart.js`

**주요 구현 내용**

- **내부감사 프로세스 표준화:** 수기/엑셀 기반 감사 프로세스를 웹 시스템으로 전환
- **리스크 기반 감사 체계:** 리스크 점수 / 잔여 리스크 / 부서별 위험도를 정량적으로 분석
- **통계 대시보드:** 종합·부서별·담당자별·대분류/중분류 통계, 리스크 점수 분포도 제공
- **BI 스타일 Drill-down:** 부서 클릭 → 담당자 → 리스크 상세까지 단계적 데이터 탐색
- **Route → Layout → Page → Components** 구조 설계로 대규모 관리자 시스템 유지보수성 확보
- **Chart.js 고급 활용:** 클릭 이벤트 기반 Drill-down, 혼합형 차트, 커스텀 Tooltip, 실시간 데이터 갱신
- **Vite 빌드 도구 채택:** Webpack 대비 빠른 프로덕션 빌드 속도를 이유로 직접 선택 — 배포 사이클 단축에 기여

> 리스크 관리 및 내부통제 프로세스를 데이터 시각화와 통계 분석 중심으로 구현한 기업형 감사 관리 시스템

---

### 5. ezims - IMS 가중치 기반 기관 통계 시스템 개선

> 단순 평균 기반 통계 로직의 구조적 결함을 분석하고, 실제 IMS 평가 산식으로 전면 재구성한 개선 프로젝트

**링크:** [ezims.ezqar.com](https://ezims.ezqar.com)  
**역할:** 백엔드 개선 및 SQL 재설계

**기술 스택**

`Java` `Spring MVC` `MyBatis` `PostgreSQL`

**문제 상황**

기존 기관 통계는 `AVG()` 반복 구조로 구현되어, 세부평가 가중치(`evaluation_weight`) / Standard 가중치 / Principle 가중치가 전혀 반영되지 않았음. 결과적으로 **기관 상세 화면 점수 ≠ 기관 통계 화면 점수**라는 불일치 발생.

**개선 산식 구조**

```
1단계: evaluation_score × evaluation_weight
2단계: SUM(weighted_point) / SUM(evaluation_weight)         → controlObjectiveRating
3단계: controlObjectiveRating × standard_weight
4단계: SUM(weighted_control_objective) / SUM(standard_weight) → tacticalOrganizationalObjectives100
5단계: principle_score × principle_weight
6단계: SUM(tactical_objective_principle)                     → domainTacticalSum
7단계: SUM(domainTacticalSum)                               → totalScore (최종)
```

**주요 구현 내용**

- **신규 Bean 설계:** `AllOrgIMSStatsBean` 분리로 기존 Bean 구조 충돌 해소
- **API 구조 신설:** `/gias/allOrgIMSWeightStats` — Controller → Service → Dao → Mapper 전 계층 구현

**결과:** 기관 상세 점수 = 기관 통계 점수 — 동일 산식 기반으로 수치 완전 일치

---

### 6. ezQar - 컨베이어 벨트 로고 슬라이더

> CSS 애니메이션만으로 구현한 무한 루프 파트너 로고 슬라이더 (JS interval 미사용)

**기간:** 2025.03.17~2025.03.21  
**링크:** [ezqar.com](https://www.ezqar.com/login)  
**역할:** 프론트엔드 기능 개발

**기술 스택**

`Vue 3` `Composition API` `CSS Animation` `Flex Layout`

**핵심 구현**

```javascript
// 배열 2배 복제로 끊김 없는 무한 루프 구현
const doubledLogos = computed(() => [...logos, ...logos])
```

```css
.marquee-inner {
  display: flex;
  width: max-content; /* 콘텐츠 너비를 명시적으로 확보 — 슬라이드 끊김 방지 */
  animation: marquee-scroll 60s linear infinite;
}

@keyframes marquee-scroll {
  0%   { transform: translateX(0); }
  100% { transform: translateX(-50%); }  /* 절반 이동 → 끊김 없는 루프 */
}

.marquee:hover .marquee-inner {
  animation-play-state: paused;  /* Hover 시 일시정지 — 링크 클릭 편의성 확보 */
}
```

**트러블슈팅**

| 문제 | 원인 | 해결 |
|------|------|------|
| 애니메이션 종료 시 끊김 | 단일 배열, 빈 공간 발생 | 배열 2배 복제 |
| `translateX(-100%)` 적용 시 점프 | 전체 width 기준 이동으로 두 번째 배열까지 사라짐 | `-50%`로 수정 |

**성능 고려:** `transform` 기반으로 reflow 최소화 — 순수 CSS Animation으로 구현

**시연 GIF**

| 기능 | 미리보기 |
|------|----------|
| 푸터 로고 슬라이더 및 Family Site | ![ezQar_footer](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/ezQar_footer.gif) |

---

### 7. KKOMO ADOPT - 유기견 입양 플랫폼

> 유기견 보호소 정보 제공 및 입양 절차 간소화를 목표로 한 풀스택 웹 서비스

**기간:** 2024.10 ~ 2024.12  
**GitHub:** [github.com/Kwak-DH/kkomoadopt](https://github.com/Kwak-DH/kkomoadopt)  
**수상:** 프론트엔드 구현 및 풀스택 인재양성 **최우수상**

**기술 스택**

`React` `Spring Boot` `Node.js` `MySQL` `Git` `Figma`

**주요 역할**

- React 컴포넌트 UI 설계 및 메인 페이지 구현
- RESTful API 설계 및 구현 (Spring Boot)
- MySQL 스키마 설계 및 쿼리 최적화
- Git 기반 코드 리뷰 및 버전 관리

**시연 GIF**

| 기능 | 미리보기 |
|------|----------|
| 메인 페이지 | ![kkomoadopt1](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/Kkomoadopt1.gif) |
| 서비스 목적 소개 | ![kkomoadopt2](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/Kkomoadopt2.gif) |
| 커뮤니티 | ![kkomoadopt3](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/Kkomoadopt3.gif) |
| 마이페이지 | ![kkomoadopt4](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/Kkomoadopt4.gif) |
| 어드민 페이지 | ![kkomoadopt5](https://raw.githubusercontent.com/Kwak-DH/portfoilo/main/assets/Kkomoadopt5.gif) |

---

## Education

**한국소프트웨어인재개발원**  
프론트엔드 구현 및 백엔드 개발을 위한 풀스택 인재양성 과정  
2024.06.27 ~ 2024.12.17

---

추가적인 코드 샘플 및 프로젝트 상세 내용은 [GitHub](https://github.com/Kwak-DH)을 참고해 주세요.
