## 📘 OpenWebUI 기반 프론트엔드 개발 및 운영 가이드

이 문서는 `OpenWebUI`를 기반으로 프론트엔드 구조를 확장하고, **한국어 사용자 친화적 개선** 및 **접근성 중심의 UI 커스터마이징** 작업을 진행한 결과를 담고 있습니다.

각 섹션을 통해 프로젝트의 방향성과 작업 내용을 한눈에 파악할 수 있으며, 하단의 문서 링크를 통해 세부 작업 내역을 확인할 수 있습니다.

---

### 🧾 프로젝트 개요

- **목표:** OpenWebUI의 사용자 경험(UX)과 시각적 접근성 향상
- **주요 작업 및 성과:**

    - **한국어 현지화 개선**
        - 미번역/부자연스러운 번역을 교정하고, `ko.json` 기반 번역 체계를 정비
        - 번역 품질 개선 작업을 PR로 제출
          → [공식 OpenWebUI 레포지토리에 Merge 승인](https://github.com/open-webui/open-webui/pull/13929)
          → [OpenWebUI v0.6.10에 release 완료](https://github.com/open-webui/open-webui/releases/tag/v0.6.10)
          
    - **웹 접근성 개선**
        - WCAG AAA 기준을 충족하는 **고명도 대비 다크 테마**(👁️ColorBlind👁️) 신규 설계 및 적용
        - 색상 대비 7:1 이상 확보 및 색약 대응을 고려하여 시각적 피로도 최소화
        - [명도 분석 및 접근성 검증 시뮬레이션 도구 사용](https://accessibleweb.com/color-contrast-checker/)

---

### 📁 문서 목차 (docs/ 디렉토리 기반)

### 📋 기본 개요

- 📖 OpenWebUI란?
- 📘 OpenWebUI를 프론트엔드 기반으로 선택한 배경
- [🔗 공식 OpenWebUI 리소스 링크](docs/OpenWebUI_공식_리소스.md)

### 🎨 프론트엔드 커스터마이징

- [🈺 한국어 현지화 및 번역 품질 개선](docs/한국어_현지화_및_품질개선.md)
- ♿ 고명도 대비 다크 테마(Colorblind Theme) 설계 및 적용 가이드

### ⚙️ 운영 환경 구성

- [🐳 Docker 이미지 빌드 가이드](docs/Docker_이미지_빌드_가이드.md)

---

### 🙋‍♀️ 참여자 (8dobibim 프론트엔드 팀)

| 이름 | GitHub |
| --- | --- |
| <img src="https://github.com/mini-777.png" width="60" /> | [@mini-777](https://github.com/mini-777) |
| <img src="https://github.com/choyeyeong.png" width="60" /> | [@choyeyeong](https://github.com/choyeyeong) |
