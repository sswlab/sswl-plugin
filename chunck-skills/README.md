# chunk-skills: 코드 제출 가이드

여러분의 코드를 스킬로 변환합니다.
아래 안내를 따라 코드를 올려주세요. **Git을 몰라도 괜찮습니다!**



---

## 코드 올리는 법 (GitHub 웹에서 클릭만으로)

> GitHub 아이디만 있으면 됩니다. 설치할 것 없습니다.

### Step 1. 이 저장소를 Fork 하기

1. https://github.com/sswlab/sswl-plugin 에 접속
2. 오른쪽 위 **`Fork`** 버튼 클릭
3. **`Create fork`** 클릭
4. 내 계정에 복사본이 생깁니다 (주소: `github.com/내아이디/sswl-plugin`)

### Step 2. 내 브랜치 만들기

> 이렇게 하면 다른 사람과 충돌이 나지 않습니다.

1. Fork한 내 저장소 페이지에서 왼쪽 위 **`master`** 버튼 클릭
2. 빈 칸에 `submit/내아이디` 입력 (예: `submit/youn_j`)
3. **`Create branch: submit/내아이디 from master`** 클릭

### Step 3. 내 폴더 만들고 코드 올리기

1. **`Add file`** → **`Create new file`** 클릭
2. 파일 이름 칸에 이렇게 입력:
   ```
   chunck-skills/내아이디/REQUEST.md
   ```
   (`/`를 입력하면 자동으로 폴더가 만들어집니다)

3. 아래 내용을 복사해서 붙여넣기:
   ```
   # Skill Conversion Request

   - Name: (본인 이름)
   - ID: (본인 아이디, 예: youn_j)
   - Code Path: (원본 코드 위치, 예: /home/youn_j/lab-codes/)
   - Purpose: (왜 스킬로 만들고 싶은지)
   - Notes: (참고사항)
   ```

4. 페이지 아래쪽 **`Commit changes`** 클릭

5. 코드 파일도 같은 방법으로 올리기:
   - **`Add file`** → **`Upload files`** 클릭
   - 파일을 드래그하거나 선택
   - **`Commit changes`** 클릭

   > 올리는 위치가 `chunck-skills/내아이디/` 안인지 확인하세요!

### Step 4. PR(Pull Request) 보내기

1. 내 Fork 저장소 페이지 상단에 노란 배너가 뜹니다:
   ```
   "submit/내아이디 had recent pushes — Compare & pull request"
   ```
2. **`Compare & pull request`** 버튼 클릭
3. 제목에 본인 이름 작성 (예: `[Submit] Junmu Youn`)
4. **`Create pull request`** 클릭
5. 끝! 관리자가 확인 후 merge합니다.

---

## 한 눈에 보는 전체 흐름

```
Fork → 브랜치 만들기 → 코드 올리기 → PR 보내기 → 관리자 merge
```

```
내 Fork (submit/내아이디 브랜치)        원본 저장소 (master)
┌──────────────────────┐            ┌──────────────────────┐
│ chunck-skills/       │            │ chunck-skills/       │
│   내아이디/          │  -- PR --> │   내아이디/          │
│     REQUEST.md       │            │     REQUEST.md       │
│     (코드 파일들)    │            │     (코드 파일들)    │
└──────────────────────┘            └──────────────────────┘
```

---

## 폴더 구조 예시

```
chunck-skills/
├── youn_j/                # Junmu Youn
│   ├── REQUEST.md
│   └── (code files)
├── kim_s/                 # Seonghwa Kim
│   ├── REQUEST.md
│   └── (code files)
└── README.md              # 이 파일
```

### ID 규칙

- 서버 홈 디렉터리 사용자명을 사용합니다.
- 예) **Junmu Youn** → `youn_j`

---

## 자주 묻는 질문

**Q. Git을 설치해야 하나요?**
A. 아닙니다. 웹 브라우저에서 전부 할 수 있습니다.

**Q. 다른 사람이 올린 코드랑 충돌나지 않나요?**
A. 각자 `submit/내아이디` 브랜치와 `chunck-skills/내아이디/` 폴더를 사용하기 때문에 충돌이 나지 않습니다.

**Q. 코드 파일이 너무 많아요.**
A. zip으로 압축해서 올려도 됩니다. 또는 ssw-tools 저장소의 어떤 폴더인지만 REQUEST.md에 적어주세요.

**Q. 올린 후에 코드를 수정하고 싶어요.**
A. 같은 브랜치에서 파일을 수정하면 PR에 자동 반영됩니다.

---

## 제출 현황

| # | Name | ID | Status |
|---|---|---|---|
| 1 | Junmu Youn | `youn_j` | completed |

> Status: `pending` → `processing` → `completed`

---

## 변환 파이프라인

제출된 코드는 아래 과정을 거쳐 스킬로 변환됩니다:

```
코드 제출 → 분석 → 분류 → [승인] → 리팩터링 → 스킬 패키징 → 검증 → 병합
```

- 원본 코드는 절대 수정하지 않습니다.
- 분류 결과 확인 후 승인 단계가 있습니다.
- 완성된 스킬은 `skills/` 디렉터리에 병합됩니다.
