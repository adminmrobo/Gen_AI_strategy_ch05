# 05번 「프롬프트로 창업 장부 미리 써 보기」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 05_startup_prompt.html |
| 모드 / 주 앵커 | 교과서 / C 장부: 연구실 옆 회계실 (③칸 거리 장면만 D 현장 보조) |
| 시즌 | 기본 |
| 대결 | 같은 월 500만원, 결제 마찰 줄이기(초파리) vs 광고비 증액(Money-Robo) → 결과 **F**, 월 이익 증가 +334만원 vs +205만원 (차이 약 39%) |
| 반영 (2026-11-03) | 표지·배경·히어로·아웃트로·썸네일·OG 6장 반영, 캐릭터 팩 fruitfly-lab-expressions@ea5da3f 23표정(96px) 적용. 그림 합계 표지 포함 464 KB / 표지 제외 307 KB |
| 새로 그릴 그림 | P1 3장 (cover_05 별도) · P2 2장 · P3 2장 |
| 재사용 | 공용 표정 13키 (IMG_00_index.md 참조) |
| 그림이 없을 때 | 페이지는 픽셀 지도와 CSS·캔버스 대체 그림으로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 RPG 픽셀아트, 굵은 어두운 외곽선, 2~3단계 명암)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로 (조수 표기는 "조수(하루)", 그림에는 이름 글자 없음)
- 이 페이지 장소: 밤의 연구실 옆 아늑한 회계실. 금화 탑, 가죽 장부(줄무늬만), 둥근 금고 문, 놋쇠 저울. 이 페이지만의 소품은 **층층이 색이 다른 깔때기 모양 장부 탑**(위가 넓고 아래로 좁아지는 여섯 칸)과 **작은 카페 모형**(좌석이 보이는 미니어처)
- 장소 영어 묘사: *cozy accounting room beside the night lab, stacks of gold coins, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light, purple lab light spilling in from one side*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|
| 0 | cover_05 | L | 1920×1080 | 새로 (COVER_05_startup_prompt.md) | P1 | 맨 위 글 표지 | 캔버스 대체 표지 (깔때기 + 픽셀 넷) |
| 1 | bg_05 | F | 1920×720 | 새로 | P3 (표지 있음) | 히어로 배경 | 벌집 무늬 + 방사 그라데이션 |
| 2 | sc_05_hero | E | 1200×800 | 새로 | P1 | 히어로 오른쪽 그림 | 금화 탑 + Money-Robo 픽셀 |
| 3 | doc_think | A | 192×192 | 공용·필요 | P1 | 히어로 대화창 | doc_front |
| 4 | asst_smile | B | 180×220 | 공용 | — | 히어로, 등장인물 | 픽셀 |
| 5 | fly_point | C | 220×220 | 공용 | — | 히어로, 왜, 대결 전 | 픽셀 |
| 6 | robo_coin | D | 180×200 | 공용 | — | 히어로, ②칸, 대결 전 | 픽셀 |
| 7 | doc_front · fly_clip · robo_smile | A·C·D | — | 공용 | — | 등장인물 카드, 아웃트로 | 픽셀 |
| 8 | doc_magic | A | 192×192 | 공용·필요 | P2 | ④칸 박사의 한 줄 | doc_front |
| 9 | asst_ledger | B | 180×220 | 공용·필요 | P1 | ③칸 숫자 발표, 꾸러미 | asst_firm |
| 10 | asst_firm | B | 180×220 | 공용 | — | 대결 결과 전 | asst_smile |
| 11 | fly_arms · robo_sigh | C·D | — | 공용 | — | 대결 후 (F), 아웃트로 | 픽셀 |
| 12 | asst_spark · doc_judge | B·A | — | 공용 | — | 대결 후, 아웃트로 | 픽셀 |
| 13 | robo_happy · fly_coffee | D·C | — | 공용 | — | (R로 바뀔 때만: ②칸에서 탄력성 0.6↑) | 픽셀 |
| 14 | sc_05_outro | E | 1200×800 | 새로 | P2 | 아웃트로 장면 | 캔버스 대체 장면 |
| 15 | thumb_05 | I | 600×400 | 새로 (cover_05 3:2 자르기) | P2 | 목차 카드 | 색 카드 |
| 16 | og_05 | K | 1200×630 | 새로 (cover_05 자르기) | P3 | 공유 미리보기 | 없음 |
| — | 행동으로 보기 (콘셉트 카드, 퍼널 막대, 가게 앞 거리), 지식 그래프 | — | — | 코드 | — | 캔버스 | — |

## 3. 새로 그릴 그림 상세

### 3-1. `sc_05_hero` — 장부 탑 앞의 네 사람
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 (2배 가능) |
| 배경 | 그림 전체 |
| 구도 | 가운데에 여섯 칸 깔때기 장부 탑(위 넓고 아래 좁음, 칸마다 다른 색, 글자 없음). 왼쪽 초파리가 오른쪽을 보며 한쪽 겹눈을 가늘게, 오른쪽 Money-Robo가 왼쪽을 보며 금화를 들어 보임, 박사는 가운데 뒤에서 턱에 손, 조수는 오른쪽 앞에서 줄무늬 장부를 펼침. 중요한 것은 위쪽 62% 안 |
| 표정·몸짓 | doc_think · asst_ledger · fly_point · robo_coin |
| 소품 | 깔때기 장부 탑, 금화 몇 개가 아래 구멍으로 떨어짐, 작은 카페 모형 (글자 없음) |
| 빛·분위기 | 금빛 램프가 장부 탑에 모임, 한쪽에서 보라 연구실 빛 |
| 피할 것 | 승패 암시, 화면·장부의 글자·숫자, 실제 쇼핑몰·카페 브랜드 |
| 대체 글 (alt) | 네 캐릭터가 색색의 깔때기 모양 장부 탑을 둘러싸고 바라보는 밤의 회계실 장면 |
| 대신 쓰는 그림 | 히어로 픽셀 그림 |

**프롬프트 (복사해서 사용)**
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, cozy accounting room beside the night lab with stacks of gold coins, leather ledgers with blank striped pages, a round vault door and a brass scale, warm golden lamp light, in the center a tall funnel-shaped tower of six stacked ledger trays in different colors, wide at the top and narrow at the bottom, a few gold coins dropping out of small gaps, a tiny cafe miniature with little seats on a side table, chibi scientist with round glasses and black hair with one white streak in a white lab coat over black vest and tie standing at the back center with a hand on his chin, anthropomorphic fruit fly researcher with black body, big red compound eyes and a blue helmet with a gold stripe and pink and blue cables, white lab coat, transparent wings, on the left facing right with one eye narrowed and pointing, round white floating robot with short antenna, black face screen with yellow pixel eyes and a blue chest light, no legs, oval shadow below, on the right facing left holding up a shiny gold coin, girl researcher with pink hair in two round buns with a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, at the front right holding an open striped ledger and a pen, curious friendly rivalry before any result, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-2. `sc_05_outro` — 새는 칸을 막은 장부 (결과 F)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 |
| 배경 | 그림 전체 |
| 구도 | 같은 회계실, 같은 깔때기 장부 탑. 왼쪽 앞(크게) 초파리가 팔짱, 탑의 넷째 칸 틈은 초록 패치로 막혀 있음. 오른쪽 Money-Robo는 한숨 방울을 띄우고 팔을 내렸지만 탑을 보며 고개를 끄덕임(인정). 박사는 가운데 뒤에서 옆을 가리키는 판정 몸짓, 조수는 두 손을 가슴 앞에 모으고 반짝이 |
| 표정·몸짓 | fly_arms · robo_sigh · doc_judge · asst_spark |
| 소품 | 초록 패치, 쌓인 금화 (글자 없음) |
| 빛·분위기 | 패치 위로 빛이 모임, 따뜻하고 편안 |
| 피할 것 | 패자 조롱, 울음 과장, 글자 |
| 대체 글 (alt) | 초파리 연구원이 깔때기 장부의 새는 칸을 막고 Money-Robo가 고개를 끄덕이는 밤의 회계실 장면 |
| 대신 쓰는 그림 | 캔버스 대체 장면 |

**프롬프트**
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, cozy accounting room beside the night lab with stacks of gold coins, leather ledgers with blank striped pages and a round vault door, warm golden lamp light, a funnel-shaped tower of six stacked colored ledger trays where the fourth tray's gap is sealed with a glowing green patch, anthropomorphic fruit fly researcher with black body, big red compound eyes and a blue helmet with a gold stripe and pink and blue cables, white lab coat, transparent wings, large in the front left facing right with arms crossed and a confident look, round white floating robot with short antenna, black face screen with yellow pixel eyes and a blue chest light, no legs, oval shadow below, on the right facing left with half-closed eyes, a small sigh bubble and arms lowered, nodding in acceptance, chibi scientist with round glasses and black hair with one white streak in a white lab coat over black vest and tie at the back center pointing to the side as a judge, girl researcher with pink hair in two round buns with a navy streak in a white lab coat over lavender hoodie with hands together and small sparkles, friendly mood, no mocking, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-3. `bg_05` — 회계실 넓은 배경 (P3)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | F · 1920×720 |
| 구도 | 왼쪽 45%는 어둡고 단순(벽과 그림자), 오른쪽에 금고 문·금화 탑·깔때기 장부 탑 실루엣. 인물 없음 |
| 대체 글 (alt) | 금고 문과 금화 탑이 있는 밤의 회계실 |
| 대신 쓰는 그림 | 표지 자르기 |

```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, cozy accounting room beside the night lab, a round vault door, stacks of gold coins, a funnel-shaped tower of six colored ledger trays in silhouette, warm golden lamp on the right, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-4. 공용 표정 중 아직 없는 것 (P1·P2)
`doc_think`, `doc_magic`, `asst_ledger` — 공용 키이므로 IMG_00_index.md에서 만든다. 표정만 바꿀 때 덧붙이는 문장: *same character, same size and position, only change the facial expression and pose to ...* (18-5 사전의 얼굴·몸짓 그대로)

## 4. 일관성 지침
- 참고 이미지: GitHub `adminmrobo/fruitfly-lab-expressions`의 네 캐릭터 기본 그림
- 같은 캐릭터는 같은 세션에서 연달아. 시드를 고를 수 있으면 캐릭터마다 고정
- 투명 배경이 안 되면 *solid flat #00ff00 background*
- 깔때기 장부 탑은 표지·히어로·아웃트로에서 같은 모양(여섯 칸, 색 순서 파랑·초록·갈색·보라·빨강·청록)

## 5. 넘겨받은 뒤 처리
1. 크기·투명 배경 확인, 단색 배경 제거
2. 빌드 크기로 줄이고 WebP 압축 (E판 너비 760)
3. `data-img` 자리(`sc_05_hero`, `sc_05_outro`, `bg_05`)에 넣고 재빌드, 그림 합계 표지 제외 400 KB · 표지 포함 600 KB 이하
4. 표지는 SKILL 18-15 절차

## 6. 체크리스트
- [x] HTML의 `data-img` 키 15개가 모두 이 명세서에 있음
- [x] 대결 후 표정이 5-8 표와 일치 (F: fly_arms · robo_sigh · doc_judge · asst_spark)
- [x] 결과 전 그림(sc_05_hero, cover_05)에 승패 암시 없음
- [x] 장소가 C 장부 앵커와 일치, 현미경·해부 소품 없음
- [x] 모든 프롬프트에 고정 외형 영어 묘사와 금지 구절
- [x] P1 새 그림 3장 (표지 제외) — 6장 이하

## 7. 매니페스트
```json
{
  "page": "05_startup_prompt",
  "anchor": "C:accounting-room",
  "season": "default",
  "duel": {"result": "F", "fly": 334, "robo": 205, "unit": "만원/월"},
  "images": [
    {"key":"cover_05","received":"2026-11-03","kb":156,"plate":"L","size":[1920,1080],"status":"done","priority":"P1","slot":"cover","fallback":"canvas-four","alt":"네 캐릭터가 밤의 회계실에서 색색의 깔때기 장부 탑을 둘러싼 표지"},
    {"key":"bg_05","received":"2026-11-03","kb":51,"plate":"F","size":[1920,720],"status":"done","priority":"P3","slot":"hero-bg","fallback":"cover_05","alt":"금고 문과 금화 탑이 있는 밤의 회계실"},
    {"key":"sc_05_hero","received":"2026-11-03","kb":75,"plate":"E","size":[1200,800],"status":"done","priority":"P1","slot":"hero-art","fallback":"pixel-robo-coins","alt":"네 캐릭터가 색색의 깔때기 모양 장부 탑을 둘러싸고 바라보는 밤의 회계실 장면"},
    {"key":"sc_05_outro","received":"2026-11-03","kb":72,"plate":"E","size":[1200,800],"status":"done","priority":"P2","slot":"outro","fallback":"canvas-stage","alt":"초파리 연구원이 깔때기 장부의 새는 칸을 막고 Money-Robo가 고개를 끄덕이는 밤의 회계실 장면"},
    {"key":"doc_think","plate":"A","size":[192,192],"status":"pack","priority":"P1","slot":"hero-dialog","fallback":"doc_front","alt":""},
    {"key":"doc_magic","plate":"A","size":[192,192],"status":"pack","priority":"P2","slot":"lv4-say","fallback":"doc_front","alt":""},
    {"key":"asst_ledger","plate":"B","size":[180,220],"status":"pack","priority":"P1","slot":"lv3-say","fallback":"asst_firm","alt":""},
    {"key":"thumb_05","received":"2026-11-03","kb":49,"plate":"I","size":[600,400],"status":"done","priority":"P2","slot":"index-card","fallback":"color-card","alt":"카페와 패션몰 창업 장부 해설 05"},
    {"key":"og_05","received":"2026-11-03","kb":114,"plate":"K","size":[1200,630],"status":"done","priority":"P3","slot":"og","fallback":"none","alt":"프롬프트로 창업 장부 미리 써 보기"}
  ]
}
```
