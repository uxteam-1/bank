---
name: Connected 문제은행 플랫폼 개발 계획
overview: ""
todos:
  - id: 99d31ecb-6d84-4643-84a3-55b6201fa567
    content: "프로젝트 기본 설정: Shadcn/ui 설치, 폴더 구조 생성, 기본 레이아웃 구성"
    status: completed
  - id: 9439764c-3a2f-48bb-8bb6-9cff309d6f9d
    content: TypeScript 타입 정의 및 더미 데이터 구조 생성
    status: completed
  - id: bc6df48b-339b-4218-83d9-46026f73c5e6
    content: 공통 UI 컴포넌트 구현 (네비게이션, 레이아웃, 폼 컴포넌트 등)
    status: completed
  - id: d00ea0d3-8a18-47f8-a14d-15165bc8e699
    content: Context API를 활용한 상태 관리 시스템 구현
    status: completed
  - id: a7ea39aa-1520-473b-a927-5c991aa7643c
    content: 선생님용 대시보드 구현 (주요 지표, 최근 활동)
    status: completed
  - id: f04dcdd8-3fc5-4292-966d-cec6a8c03ed6
    content: 학습지 관리 시스템 구현 (목록, 상세, 3단계 생성 프로세스)
    status: completed
  - id: d6777bcd-7536-4b66-9c3e-16b3325f4c06
    content: 과제 관리 시스템 구현 (배정, 진행 현황, 결과 분석)
    status: completed
  - id: 002b4dbb-2c37-4411-85f8-ceeb9801db3c
    content: 학생 관리 시스템 구현 (목록, 개별 현황, 과제 결과)
    status: completed
  - id: bfda7df2-f780-40ea-9feb-b780312a7113
    content: 학생용 홈 화면 구현 (학습 현황, 진행 중 과제, 취약 유형)
    status: completed
  - id: 19aca8d1-d1d2-46d9-9b6f-98ce84ecf67d
    content: 학생용 과제 시스템 구현 (목록, 문제 풀이, 결과 확인)
    status: pending
  - id: 5ea6a4d9-fde1-4d8e-b4c1-f03f57cf1f93
    content: 학생용 리포트 시스템 구현 (학습 이력, 성적 추이, 분석)
    status: pending
  - id: e600e30c-3e25-4758-883f-043b84431c26
    content: 고급 기능 구현 (상위권 특화, 유사 문항 추천, 오답 재시험지)
    status: pending
  - id: e5b901de-4da3-476e-bd09-335030d45194
    content: 모바일 최적화 및 반응형 디자인 개선
    status: pending
isProject: false
---

# Connected 문제은행 플랫폼 개발 계획

## 기술 스택

- **Frontend**: Next.js 16.0.0, React 19, TypeScript
- **Styling**: TailwindCSS 4, Shadcn/ui + Radix UI
- **상태관리**: React Context API + useReducer
- **데이터**: 더미 데이터 (JSON 파일)
- **인증**: 기존 대교 하이캠퍼스 연동 대비 인터페이스 구성

## 프로젝트 구조

```
app/
├── (auth)/                 # 인증 관련 페이지
├── teacher/               # 선생님용 LMS
│   ├── dashboard/         # 대시보드
│   ├── worksheets/        # 학습지 관리
│   ├── assignments/       # 과제 관리
│   └── students/          # 학생 관리
├── student/               # 학생용 Web
│   ├── home/             # 홈
│   ├── assignments/      # 나의 과제
│   └── reports/          # 리포트
├── components/           # 공통 컴포넌트
├── lib/                 # 유틸리티 및 더미 데이터
└── types/               # TypeScript 타입 정의
```

## 주요 구현 기능

### 1. 공통 기반 구조

- 반응형 레이아웃 컴포넌트
- 네비게이션 시스템 (선생님/학생 구분)
- 더미 데이터 구조 및 Context API
- 공통 UI 컴포넌트 (Shadcn/ui 기반)

### 2. 선생님용 LMS

- **대시보드**: 주요 지표, 최근 학습지/과제 목록
- **학습지 관리**: 목록, 상세, 3단계 생성 프로세스
- **과제 관리**: 배정, 진행 현황, 상세 분석
- **학생 관리**: 목록, 개별 학습 현황

### 3. 학생용 Web

- **홈**: 학습 현황, 진행 중 과제, 취약 유형
- **나의 과제**: 과제 목록, 문제 풀이 화면, 학습 결과
- **리포트**: 학습 이력, 성적 추이, 취약 유형 분석

### 4. 특별 기능

- 상위권 학생을 위한 고난도 문제 필터링
- 유사/쌍둥이 문항 추천 시스템 (더미)
- 오답 기반 재시험지 자동 생성
- 폴더 기반 학습지 관리
- QR 코드 기반 모바일 채점 인터페이스

## 구현 우선순위

1. 기본 프로젝트 설정 및 공통 컴포넌트
2. 더미 데이터 구조 및 Context API
3. 선생님용 LMS 핵심 기능
4. 학생용 Web 핵심 기능
5. 고급 기능 및 상위권 특화 기능
6. 모바일 최적화 및 반응형 개선