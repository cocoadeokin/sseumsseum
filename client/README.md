# **씀씀 :: 똑똑한 소비 비서** 씀씀이 📝

**씀씀**은 월별 예산을 효과적으로 관리하고 소비 습관을 개선할 수 있도록 돕는 스마트 가계부 웹 애플리케이션입니다. 복잡한 재무 관리, 이제 씀씀이와 함께 쉽고 스마트하게 시작해 보세요!



---

## ✨ 주요 기능

-   **월별 예산 설정**: 사용자는 매월 수입 및 지출 카테고리별로 예산을 자유롭게 설정하고 수정할 수 있습니다.
-   **수입/지출 내역 기록**: 간편한 인터페이스를 통해 일별 수입과 지출 내역을 손쉽게 추가하고 관리할 수 있습니다.
-   **카테고리 관리**: 사용자의 소비 패턴에 맞게 지출 및 수입 카테고리를 직접 추가, 수정, 삭제할 수 있습니다. 추천 카테고리 기능으로 더욱 빠른 설정이 가능합니다.
-   **월별 소비 리포트**: 월별 지출 내역을 카테고리별로 분석하여 시각적인 차트로 제공합니다. 이를 통해 자신의 소비 습관을 한눈에 파악하고 개선점을 찾을 수 있습니다.
-   **보안 인증**: JWT(JSON Web Token)를 사용한 안전한 사용자 인증 및 세션 관리를 통해 개인의 금융 정보를 보호합니다.

---

## 🛠️ 기술 스택

이 프로젝트는 다음과 같은 기술들을 사용하여 구축되었습니다.

-   **Frontend**:
    -   ![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
    -   ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
    -   ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
    -   ![Zustand](https://img.shields.io/badge/Zustand-000000?style=for-the-badge&logo=react&logoColor=white) (상태 관리)
    -   ![React Hook Form](https://img.shields.io/badge/React_Hook_Form-EC5990?style=for-the-badge&logo=react-hook-form&logoColor=white) (폼 관리)
    -   ![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white) (HTTP 통신)

-   **Backend**:
    -   *(백엔드 서버에서 사용된 기술 스택을 여기에 추가하세요. 예: Node.js, Express, PostgreSQL 등)*

-   **Deployment & Architecture**:
    -   ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
        -   **Hosting**: 프론트엔드 배포
        -   **Cloud Functions**: API 프록시 서버 구축 (CORS 문제 해결 및 안전한 백엔드 통신)

---

## 🚀 시작하기

프로젝트를 로컬 환경에서 실행하려면 다음 단계를 따르세요.

### **1. 사전 준비**

-   [Node.js](https://nodejs.org/) (v18 이상 권장)
-   [npm](https://www.npmjs.com/) 또는 [yarn](https://yarnpkg.com/)

### **2. 프로젝트 클론 및 설치**

```bash
# 저장소를 클론합니다.
git clone [https://github.com/cocoadeokin/sseumsseum.git]

# 프로젝트 폴더로 이동합니다.
cd sseumsseum/client

# 필요한 패키지를 설치합니다.
npm install
```

### **3. 환경 변수 설정**

프로젝트 루트 디렉토리에 `.env.local` 파일을 생성하고, 필요한 환경 변수를 입력합니다. (프론트엔드에서 백엔드 API 주소를 직접 호출하는 경우)

```
VITE_API_BASE_URL=http://localhost:44445
```
*본 프로젝트는 Firebase 프록시를 사용하므로 이 설정이 필요 없을 수 있습니다.*

### **4. 로컬 서버 실행**

```bash
# 개발 서버를 시작합니다.
npm run dev
```

이제 브라우저에서 `http://localhost:5173` (또는 터미널에 표시된 주소)으로 접속하여 애플리케이션을 확인할 수 있습니다.

---

## 🏗️ 프로젝트 구조

```
sseumsseum-project/
├── functions/              # Firebase Cloud Functions (API 프록시)
│   ├── src/
│   │   └── index.ts        # 프록시 서버 로직
│   └── package.json
├── public/                 # 정적 에셋
├── src/
│   ├── api/                # API 호출 함수
│   ├── components/         # 재사용 가능한 UI 컴포넌트
│   ├── pages/              # 라우팅 페이지 컴포넌트
│   ├── store/              # Zustand 상태 관리 스토어
│   ├── styles/             # 전역 스타일 및 CSS 파일
│   ├── types/              # TypeScript 타입 정의
│   ├── utils/              # 유틸리티 함수
│   ├── App.css             # App 컴포넌트 스타일
│   ├── App.tsx             # 메인 애플리케이션 컴포넌트
│   ├── index.css           # 기본 스타일
│   └── main.tsx            # 애플리케이션 진입점
├── .firebaserc             # Firebase 프로젝트 설정
├── firebase.json           # Firebase 호스팅 및 함수 설정
└── package.json
```