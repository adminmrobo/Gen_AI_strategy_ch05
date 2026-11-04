# 생성형 AI 활용 전략 — AI 연구실 해설

강의 **「생성형 AI 활용 전략」** 교안을 장마다 하나의 인터랙티브 해설 페이지로 옮긴 시리즈입니다.
박사 · 조수(하루) · 초파리 연구원 · 주판봇 네 캐릭터가 진행하고, 계산기와 대결, 확인 퀴즈로 내용을 직접 확인합니다.

글 · 안상선 ((주)M-Robo 대표) · Ahn Sangsun

![표지](og_05.webp)

## 페이지 목록

| 장 | 페이지 | 다루는 내용 |
|---|---|---|
| 제5장 | [프롬프트로 창업 장부 미리 써 보기 — 카페·패션몰 업종분석](05_startup_prompt.html) | 5단계 흐름(검증→시장→KPI→손익→브랜딩), 패션몰 전환 퍼널과 민감도, 카페 7단계 손익, RTP-ASK-FC 8요소, 문제 분해 7단계 |

전체 목차는 [`index.html`](index.html)에서 볼 수 있습니다.

### 제5장 페이지 구성

- **사다리 다섯 칸:** ① 병렬 검증 → ② 전환 퍼널·민감도 → ③ 카페 7단계 → ④ RTP-ASK-FC 프롬프트 조립기 → ⑤ 문제 분해·브랜딩
- **대결:** 같은 월 500만원을 결제 마찰 줄이기(초파리 연구원)와 광고 증액(주판봇) 중 어디에 쓸 것인가. 판정 기준은 월 이익 증가분
- **확인 퀴즈:** 12문항 (계산 문항 3개)
- **지식 색인·꾸러미:** 개념 77개 · 관계 98개. JSON · JSON-LD · Turtle · CSV · CSL-JSON · BibTeX · RIS를 ZIP 하나로 내려받기

> 계산기의 기본값은 모두 **예시값**입니다. 일부는 교안 표 5-5의 예시이고, 나머지는 설명용으로 정한 값입니다. 실제 상권·쇼핑몰 데이터가 아니며 창업 판단의 근거로 쓰지 마세요.

## 폴더 구조

```
.
├── index.html                 # 시리즈 목차 (표지)
├── 05_startup_prompt.html     # 제5장 해설 페이지 (단일 파일: 그림·캐릭터·데이터 포함)
├── cover_05_960.webp          # 목차 표지 그림
├── thumb_05.webp              # 목차 카드 썸네일 (600×400)
├── og_05.webp                 # 공유 미리보기 (1200×630)
├── .nojekyll                  # GitHub Pages가 파일을 그대로 내보내도록
├── README.md
└── docs/
    ├── IMG_05_startup_prompt.md     # 이미지 제작 명세서 (매니페스트 포함)
    ├── COVER_05_startup_prompt.md   # 표지 생성 지시문 (Genspark용)
    └── KG_00_registry.json          # 시리즈 지식 그래프 ID 등록부
```

해설 페이지는 **파일 하나로 완결**됩니다. 그림과 캐릭터, 지식 그래프 데이터가 모두 HTML 안에 들어 있어 내려받아 더블클릭만 해도 열립니다. 인터넷이 없으면 웹 글꼴만 시스템 글꼴로 바뀝니다.

## GitHub Pages로 공개하기

1. 이 폴더의 내용을 저장소 맨 위(root)에 올립니다.
2. 저장소 **Settings → Pages**에서 *Source*를 `Deploy from a branch`, 브랜치를 `main`, 폴더를 `/ (root)`로 정합니다.
3. 잠시 뒤 `https://<계정>.github.io/<저장소 이름>/`에서 목차가 열립니다.

### 공개 뒤 한 번 바꿀 것

SNS 공유 미리보기가 그림을 가져가려면 `og:image`가 전체 주소여야 합니다. 공개 주소가 정해지면 아래 두 파일에서 바꿔 주세요.

| 파일 | 지금 | 바꿀 값 |
|---|---|---|
| `index.html` | `<meta property="og:image" content="og_05.webp">` | `https://<계정>.github.io/<저장소 이름>/og_05.webp` |
| `05_startup_prompt.html` | 같은 줄 | 같은 주소 |

꾸러미의 개념 ID는 지금 `urn:lab:` 접두어를 씁니다. 공개 주소가 정해지면 바꿀 수 있습니다(`docs/KG_00_registry.json` 참조).

## 새 장 추가하기

1. `NN_slug.html` 이름으로 해설 페이지를 올립니다 (예: `06_xxx.html`).
2. `thumb_NN.webp`(600×400)와 `og_NN.webp`(1200×630)를 함께 올립니다.
3. `index.html`의 목차에 카드 하나를 복사해 넣고 링크·제목·썸네일을 바꿉니다. 장 번호는 목차 카드에만 적습니다.
4. 이 README의 **페이지 목록** 표에 한 줄 추가합니다.
5. `docs/`에 그 장의 명세서·지시문을 넣고, `KG_00_registry.json`에 새 개념 ID를 합칩니다.

## 출처와 인용

- 원자료: 「제5장 프롬프트 엔지니어링 활용 — 창업 업종분석: 카페·패션몰」 강의용 교안
- 인용 예: 안상선 (2026). 프롬프트로 창업 장부 미리 써 보기 — 카페·패션몰 업종분석. AI 연구실 해설 대시보드 05, v1.0.
- BibTeX·RIS는 각 페이지 맨 아래 **온톨로지·서지 꾸러미**에서 복사할 수 있습니다.

## 크레딧

- 캐릭터: [adminmrobo/fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (캐릭터 팩 @ `ea5da3f`)
- 제작 도구: [adminmrobo/ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) — ai-lab-explainer 스킬
- 표지·배경·장면 그림: Genspark로 생성
- 글꼴: IBM Plex Sans KR (Google Fonts, SIL Open Font License)

## 라이선스

<!-- 라이선스를 정하면 여기에 적고 LICENSE 파일을 추가하세요. 예: 글·그림 CC BY-NC 4.0, 코드 MIT -->
아직 정하지 않았습니다. 정해지기 전까지 모든 권리는 저자에게 있습니다. 네 캐릭터의 권리는 캐릭터 저장소의 안내를 따릅니다.
