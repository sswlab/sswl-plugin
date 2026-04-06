# chunk-skills: Code Submission Request

SSW Plugin에 포함할 스킬을 만들기 위해 여러분의 코드를 수집합니다.
아래 양식에 맞춰 코드 경로를 등록해 주세요.

수집된 코드는 [99-SSWL-skill-collector](https://github.com/sswlab/SSWL-harness-ops) 하네스를 통해
분석 → 분류 → 리팩터링 → 스킬 패키징 파이프라인으로 변환됩니다.

---

## How to Submit

**이름 / 코드 경로** 형식으로 아래 표에 추가해 주세요.

| Name | Path | Description |
|---|---|---|
| Junmu Youn | `youn_j` | Sun and Space Weather toolkit |
| _your name_ | `_your_id_` | _brief description_ |

### Naming Convention

- 홈 디렉터리 사용자명을 기준으로 합니다.
- 예) **Junmu Youn** → `youn_j` → `/home/youn_j/`

### Steps

1. 이 저장소를 fork 또는 clone 합니다.
2. `chunck-skills/` 아래에 **자신의 ID 디렉터리**를 만듭니다.
3. 변환하고 싶은 코드를 해당 디렉터리에 넣습니다.
4. 아래 메타 파일(`REQUEST.md`)을 함께 작성합니다.
5. PR을 올리거나, 관리자에게 경로를 알려주세요.

```
chunck-skills/
├── youn_j/                # Junmu Youn
│   ├── REQUEST.md
│   └── (your code files)
├── kim_s/                 # (example) Seonghwa Kim
│   ├── REQUEST.md
│   └── (your code files)
└── README.md              # this file
```

---

## REQUEST.md Template

각자 디렉터리 안에 `REQUEST.md`를 작성해 주세요.

```markdown
# Skill Conversion Request

- **Name**: (your name)
- **ID**: (your_id)
- **Code Path**: (original code location, e.g., /home/youn_j/lab-codes/)
- **Purpose**: (why you want this code converted to a skill)
- **Mode**: Full Scan / Incremental / Targeted
- **Notes**: (any additional context)
```

### Mode Guide

| Mode | When to Use |
|---|---|
| **Full Scan** | 처음으로 코드를 정리할 때 (전체 분석) |
| **Incremental** | 기존 스킬에 새 코드를 추가할 때 |
| **Targeted** | 특정 파일만 스킬로 변환할 때 |

---

## Processing Pipeline

```
코드 제출 → skill-collector 분석 → 분류 → [승인] → 리팩터링 → 스킬 패키징 → 검증 → 병합
```

- 원본 코드는 수정하지 않습니다 (사본으로 작업).
- 분류 결과 확인 후 승인 단계가 있습니다.
- 변환된 스킬은 `skills/` 디렉터리에 병합됩니다.

---

## Registered Submissions

| # | Name | ID | Status |
|---|---|---|---|
| 1 | Junmu Youn | `youn_j` | completed |

> 제출 후 이 표에 추가됩니다. Status: `pending` → `processing` → `completed`
