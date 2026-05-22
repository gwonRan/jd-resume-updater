# Career Document Skills

이 저장소는 이력서와 포트폴리오 작성을 위한 Codex skill 두 개를 함께 관리합니다.

## Skills

### `resume-jd-updater`

목표 JD와 프로젝트 메모를 바탕으로 이력서와 경력기술서를 업데이트하는 skill입니다.

주요 기능:

- JD 분석
- 마스터 이력서 재료집 생성
- JD-경험 매칭
- 성과 언어 변환
- 스킬/도구 맥락화
- 기간/기한 반영
- 이력서 bullet 및 섹션 업데이트
- 후속 질문 생성

사용 예시:

```text
Use $resume-jd-updater to update my resume for this JD.
```

### `portfolio-case-builder`

프로젝트 메모를 채용용 포트폴리오 케이스 스터디로 바꾸는 skill입니다.

주요 기능:

- 포트폴리오 목차 구성
- 프로젝트 증거 추출
- 문제 정의-해결 과정-결과-회고 구조화
- 스킬/도구 활용 맥락 정리
- 성과 시각화 아이디어 도출
- JD와 연결되는 역량 매핑
- 후속 질문 생성

사용 예시:

```text
Use $portfolio-case-builder to create portfolio case studies from these project notes.
```

## 저장소 구조

```text
.
├── README.md
├── portfolio-case-builder/
│   ├── SKILL.md
│   ├── agents/
│   ├── assets/
│   └── references/
└── resume-jd-updater/
    ├── SKILL.md
    ├── agents/
    ├── assets/
    └── references/
```

## 설치 방법

이 저장소를 받은 뒤, 필요한 skill 폴더를 Codex skills 디렉터리에 복사하거나 링크합니다.

```bash
mkdir -p ~/.codex/skills
cp -R resume-jd-updater ~/.codex/skills/resume-jd-updater
cp -R portfolio-case-builder ~/.codex/skills/portfolio-case-builder
```

두 skill을 모두 쓰려면 두 폴더가 각각 `~/.codex/skills/` 바로 아래에 있어야 합니다.

## 작성 원칙

- 사용자가 제공한 정보만 확정 사실로 사용합니다.
- 수치, 날짜, 도구, 프로젝트 범위, 오너십, 성과를 임의로 만들지 않습니다.
- 불확실한 내용은 `[확인 필요]`로 표시하거나 후속 질문으로 분리합니다.
- 개인 기여와 팀/회사 성과를 구분합니다.
- 스킬과 도구는 이름만 나열하지 않고 실제 사용 맥락과 결과에 연결합니다.
- 고객명, 내부 시스템명, 미공개 제품, 민감한 비즈니스 수치는 일반화합니다.
