# JD Resume Updater

`jd-resume-updater`는 사용자가 제공한 프로젝트 메모, 직무 정보, 기존 이력서, 목표 JD를 바탕으로 이력서 콘텐츠를 업데이트하는 Codex skill입니다.

완성된 문서가 없어도 사용할 수 있습니다. 일부 프로젝트 메모, 기억 기반 요약, 회의 내용, 기존 이력서 일부만 있어도 근거를 추출하고 JD와 연결해 이력서 bullet, 경력 요약, 면접 답변 재료를 만듭니다.

## 주요 기능

- 목표 JD의 필수 역량, 우대 역량, 반복 키워드, 직무 레벨 신호 분석
- 프로젝트 메모에서 이력서에 쓸 수 있는 근거 추출
- PM, 서비스 기획, 운영 기획, 앱 서비스 고도화 경험을 JD 요구사항과 매칭
- 한국어 또는 영어 이력서 bullet 작성
- 이력서 섹션, 경력 요약, LinkedIn/About 문장, 면접 STAR 답변 초안 작성
- 부족한 성과 수치, 오너십, 협업 범위, 기밀 정보 여부에 대한 후속 질문 생성

## 사용 방법

Codex에서 이 skill을 사용한다고 말하고, 가지고 있는 자료를 붙여넣으면 됩니다.

```text
Use $jd-resume-updater to update my resume for this JD.

목표 JD:
...

내 직무 정보:
- 현재 직무: PM
- 연차: 4년차
- 담당 범위: 운영기획 / 앱 서비스 고도화
- 강조 역량: 구조화 역량

프로젝트 메모:
...

기존 이력서:
...
```

모든 항목을 채울 필요는 없습니다. 정보가 부족하면 skill이 이력서 품질을 높이기 위한 후속 질문을 정리합니다.

## 입력 템플릿

```markdown
## 목표 JD
지원하려는 JD를 붙여넣어 주세요.

## 내 직무 정보
- 현재/과거 직무:
- 연차:
- 담당 범위:
- 강조하고 싶은 역량:
- 지원하려는 포지션/회사:

## 기존 이력서 또는 경력 요약
기존 이력서, 경력 요약, LinkedIn/About 문장 등이 있으면 붙여넣어 주세요.

## 프로젝트 메모
- 기간:
- 프로젝트 목적:
- 문제 상황:
- 내가 한 일:
- 사용 기술/도구/방법:
- 협업 대상:
- 성과 수치:
- 정성 성과:
- 공개하면 안 되는 정보:

## 선호사항
- 한국어/영어:
- 필요한 출력물: 이력서 / 경력기술서 / LinkedIn / 면접 답변
- 원하는 톤:
- 특별히 피하고 싶은 표현:
```

## 출력 모드

- 프로젝트 증거표
- JD 분석
- JD-경험 매칭
- 이력서 bullet
- 이력서 섹션 업데이트
- 커리어 서사
- 면접 준비 답변
- 후속 질문 리스트

## 설치 방법

이 저장소를 Codex skills 디렉터리에 clone합니다.

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/gwonRan/jd-resume-updater.git ~/.codex/skills/jd-resume-updater
```

그다음 새 Codex 세션에서 다음처럼 호출합니다.

```text
Use $jd-resume-updater
```

## 저장소 구조

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── input_template_ko.md
│   ├── project_evidence_template.md
│   ├── resume_template_en.md
│   └── resume_template_ko.md
└── references/
    ├── bullet_patterns.md
    ├── followup_questions.md
    ├── jd_analysis_framework.md
    ├── project_evidence_framework.md
    └── resume_quality_rubric.md
```

## 작성 원칙

- 사용자가 제공한 정보만 확정 사실로 사용합니다.
- 수치, 날짜, 도구, 프로젝트 범위, 오너십, 성과를 임의로 만들지 않습니다.
- 불확실한 내용은 `[확인 필요]`로 표시하거나 후속 질문으로 분리합니다.
- 개인 기여와 팀/회사 성과를 구분합니다.
- 고객명, 내부 시스템명, 미공개 제품, 민감한 비즈니스 수치는 일반화합니다.
- JD 키워드는 자연스럽게 반영하고, 키워드 나열식으로 억지 삽입하지 않습니다.
- 사용자의 실제 연차와 역할 범위를 과장하지 않습니다.
