# CREDITS — 8번째 용사 시험판

> 규칙 = `../Studio/.claude/instructions/studio/studio_credits.md`. 서드파티 · 폰트 · AI 생성물은 **들여온 그 자리에서** 적는다.

## 1. 라이브러리

| 이름 | 버전 | 라이선스 | 불러오는 곳 |
| --- | --- | --- | --- |
| three.js | r128 | MIT | cdnjs — `boss_graybox` 판만 쓴다. 지금 공개 빌드(여왕전)에는 없다 |

## 2. 폰트

| 이름 | 라이선스 | 불러오는 곳 |
| --- | --- | --- |
| Gowun Batang | SIL OFL 1.1 | Google Fonts — 지금 공개 빌드(여왕전). 빌드에 포함하지 않는다 |
| ~~Song Myung (JIKJI)~~ | SIL OFL 1.1 | 🔄 2026-11-07 거뒀다 — 대화문은 고운바탕(D-241) |
| Nanum Myeongjo (Sandoll) | SIL OFL 1.1 | Google Fonts — 여왕의 외침(D-152). 빌드에 포함하지 않는다 |
| ~~East Sea Dokdo~~ | SIL OFL 1.1 | 🔄 2026-11-06 거뒀다(외침은 고운바탕) |
| Do Hyeon | SIL OFL 1.1 | Google Fonts — `boss_graybox` · `queen_stage` 판. 빌드에 포함하지 않는다 |
| IBM Plex Sans KR | SIL OFL 1.1 | Google Fonts — 같음 |

## 3. 그림 · 소리

소리 = §3-0. 지금 공개 빌드의 그림 = §3-2. 시험을 마친 판들은 코드로 그린 사각형 · 도트 · 복셀을 썼다. 서드파티 에셋은 없다.

### 3-0. 소리 (2026-11-05 · D-110)

| 무엇 | 출처 | 라이선스 | 쓴 곳 |
| --- | --- | --- | --- |
| Impact Sounds 1.0 · RPG Audio | Kenney (kenney.nl) · 원본 `Studio/projects/ProjectEighth/resources/audio/source/` | **CC0** — 표기 의무 없음(License.txt 동봉) | `parts/sfx_*.ogg` — 겹치고 피치를 바꿔 구웠다(`bake_audio.py`) |
| 배경음악 3곡 | 로컬 생성 — ComfyUI · ACE-Step v1 3.5B · 프롬프트 `resources/audio/bgm_prompts.json` · 2026-11-05 | 모델 **Apache-2.0** · 밖으로 나간 것 없음 | `parts/bgm_*.ogg` |
| 괴물 울음 4개 | 로컬 생성 — ComfyUI · Stable Audio Open 1.0 · 프롬프트 `Studio/projects/ProjectEighth/resources/audio/sfx_beast_prompts.json` · 시드 7102 · 7201 · 7302 · 7400 · 2026-11-07(D-252) | 모델 **Stability AI Community License** — 연 매출 100만 달러 미만 상업 이용 가능 · ⚠️ 상업 출시 전 등록 · 밖으로 나간 것 없음 | `parts/sfx_roar0` · `growl0` · `howl0` · `groan0` |
| 합성음 | 코드(`beep`) | 자체 | 쇠 울림 · 웅웅거림 |

### 3-1. AI 생성 참고 그림 (2026-11-04)

폐기한 도트 판의 참고 그림이다(D-12). 지금 공개 빌드에는 들어가지 않는다.

| 파일 | 도구 | 쓴 곳 | 상태 |
| --- | --- | --- | --- |
| `Studio/projects/ProjectEighth/resources/art/source/hero_chatgpt_sheet_20261104.png` | ChatGPT 이미지 생성(사용자 실행) | 후보생 3방향의 참고 | 게임에는 픽셀을 복사하지 않았다. 보고 다시 찍었다 |
| `Studio/projects/ProjectEighth/resources/art/source/hero_chatgpt_attack_20261104.png` | 같음 | 공격 자세의 참고 | 같음 |

### 3-2. AI 생성 그림 — 동화풍 시험판 (2026-11-04)

🔄 2026-11-06 괴물 조각 = `out/mon2/sb_monster/sb_queen_monster2_v08.png`(프롬프트 · 시드 = 그 폴더 `art_manifest.json`) · 탁자 = `sb_pr_table_v01` 에서 동물을 지우고 편지를 코드로 그림(`bake_table.py`) · 벌판 시체 `prop_fd*` · 시체산 = `bake_field.py` · `bake_summit.py`(`out/sb_grim/`). 모델은 같은 Nova Anime XL · 라이선스 감사 통과(2026-11-06).

🔄 2026-11-05 프롤로그 추가 — 수녀 · 대리석 석상 7 · 가시 · 문 · 나무 판자 · 철퇴(`parts/prop_nun*` · `prop_statue*` · `prop_spike*` · `prop_door*` · `prop_fence` · `prop_mace`, 원본 `resources/art/out/sb_side` · `sb_prop` · `sb_prop_marble`, 같은 모델). 시험용이다. 벽 · 바닥 · 횃불 · 가시 판은 코드로 그렸다.

`Prototype/queen_storybook/parts/` 의 인물 조각 · 괴물 조각 · 돼지 시체 · 시체 더미 · 잘린 머리 · 무기 · 나무 · 폐허 · 풀. 로컬 ComfyUI + Nova Anime XL(`novaAnimeXL_ilV130` · `--audit` 통과 · 이미지 상업 허용) · LoRA 없음. 프롬프트 · 시드 = `Studio/projects/ProjectEighth/resources/art/prompts.yaml` · `out/art_manifest.json`. 🔸 땅(`ground.jpg`) · 돌(`prop_rock*.webp`) · 활 · 뼈 팔은 AI 없이 코드로 그렸다. 🔄 돼지 시체 · 더미 · 잘린 머리는 2026-11-05 다시 만들었다(`sb_grim` · 같은 모델) — 더미의 밑그림은 같은 모델의 그림을 오려 쌓은 것이다(`Prototype/queen_storybook/bake_heap.py`).

🔄 2026-11-07 둥근 말풍선(D-241) — `parts/ui_bubble3_s · m · l.webp`. 원본 = `Studio/projects/ProjectEighth/resources/art/out/bubble4/ui_dsb_tex/ui16_dialog_s_v06 · m_v01 · l_v05.png`(프롬프트 · 시드 = 그 폴더 `art_manifest.json`) · 밑그림 = `Prototype/queen_storybook/art_src/ui/pe_bubble3_*.png`(코드로 그린 둥근 상자) → img2img 0.74 · 화풍 `ui_dsb_tex`(Nova Anime XL 단독 · LoRA 없음) · 바깥 흰 곳만 지워 줄임. 사람 손 안 댐 · 밖으로 나간 것 없음.

🔄 2026-11-07 아나샤 분노 머리(D-235) — `parts/queen_head_rage.png`. 원본 `sb_side_nc/sb_queen_nc_side_v05.png` 의 얼굴만 인페인트(`Studio/tools/ai-art/inpaint_region.py` · 화풍 `sb_face` · Nova Anime XL 단독 · LoRA 없음 · IP-Adapter 끔 · denoise 0.8 · seed 32 · 상자 268,102,466,370 · 마스크 타원 586,244,110,126 · 662,390,44,34) → `out/queen_expr/d_rage_s32.png` → 원래 머리 조각과 같은 상자 · 테두리(알파)로 잘라 줄임. 🔄 D-276 조각 해상도를 0.3 → 0.6배로 올리며 같은 원본 · 같은 상자로 다시 잘랐다(테두리 = 새 기본 머리). 증오 머리 `parts/queen_head_hate.png` = 같은 방법 · 같은 마스크 · denoise 0.8 · seed 41 → `out/queen_expr/h_hate_d0.8_s41.png`. 찡그림 머리 `parts/queen_head_wince.png` = 같은 방법 · denoise 0.8 · seed 52 → `out/queen_expr/w_wince_d0.8_s52.png`. 사람 손 안 댐 · 밖으로 나간 것 없음.

🔄 2026-11-07 일곱 용사 제단의 받침(🔸 D-228) — `parts/prop_altar.webp`. 원본 = `Studio/projects/ProjectEighth/resources/art/out/altar/sb_obj/sb_altar_v02.png`(프롬프트 · 시드 = 그 폴더 `art_manifest.json`) · 화풍 `sb_obj`(Nova Anime XL 단독 · LoRA 없음 · 같은 체크포인트라 위 감사 그대로) · 배경 따기 `cutout_ml.py`(rembg · 로컬) · 480px 로 줄임. 사람 손 안 댐 · 밖으로 나간 것 없음.

🔄 2026-11-07 길의 🔸 임시 짐승(D-223) — `parts/prop_beast_s.webp` · `prop_beast_b.webp`. 원본 = `Studio/projects/ProjectEighth/resources/art/out/beast/sb_beast/sb_beast_s_v02.png` · `sb_beast_b_v05.png`(프롬프트 · 시드 = 그 폴더 `art_manifest.json`) · 화풍 `sb_beast`(Nova Anime XL 단독 · LoRA 없음 · 같은 체크포인트라 위 감사 그대로) · 배경 따기 `cutout_ml.py`(rembg · 로컬) · 작은 것은 좌우 뒤집음. 사람 손 안 댐 · 밖으로 나간 것 없음.

### 3-3. UI 그림 시험 — StorybookRedmond LoRA (2026-11-06 · 시험 중, 게임에 아직 안 넣음)

| 항목 | 값 |
| --- | --- |
| 모델 | StorybookRedmond — StoryBook Kids Lora Style for SD XL (v1.0) · 제작자 `artificialguybr` |
| 출처 | https://civitai.com/models/132128 (버전 145304) |
| 파일 | `D:/AI/ComfyUI/models/loras/StoryBookRedmond-KidsRedmAF.safetensors` · 665,266 KB · SHA256 `D6417A074EA3832531DAAD518DCD2B74F42980CA8998A4B0C91601E591105C1B`(받은 파일과 일치 확인) |
| 권한(Civitai 플래그 · 2026-11-06 API 확인) | `allowCommercialUse = Image, RentCivit, Rent` — **생성 이미지 상업 판매 허용** · `allowNoCredit = true`(표기 의무 없음 — 그래도 여기 적는다) |
| 쓰는 곳 | `Studio/projects/ProjectEighth/resources/art/styles.yaml` 의 `ui_sb*` 화풍 · 결과 `resources/art/out/ui_sb*/` |

- ⚠️ 특정 작가 · 게임 화풍을 학습했는지는 플래그로 알 수 없다(«아이들 그림책 화풍» 일반). 출시 전 `--audit` 와 함께 사람이 다시 본다.

### 3-4. UI 그림 — 어두운 동화풍 (2026-11-06 · D-142 · 게임에 넣음)

`Prototype/queen_storybook/parts/ui_bossframe · ui_bubble · ui_shout · ui_btn_parry · ui_btn_attack.webp`(🔄 하트 · 해골 · 그로기 틀은 거뒀다 · 대화창 `ui6_*` · 외침 `ui7_*` = 틀 전용 화풍 · LoRA 없음 · 종이는 `ui6_bubble_parchment_v03`) — 원본 `art_src/ui/`(굽기 = `bake_ui.py`). 로컬 ComfyUI + Nova Anime XL(`novaAnimeXL_ilV130`) · 일부는 Game icon LoRA(Civitai 141066 · v1.0 · SHA256 `9E39A540E97173442ABBB319437080E4DC5A48087F43ED94C53BAFEF75E2E903` · `allowCommercialUse = Image, RentCivit, Rent, Sell` · 표기 의무 없음) 0.35. 프롬프트 · 시드 = `Studio/projects/ProjectEighth/resources/art/prompts.yaml` 의 `ui4_*` · `out/art_manifest.json`.

🔸 2026-11-07 폰 버튼 셋(D-271) — `parts/ui_btn_roll · ui_btn_flask · ui_btn_skill.webp`. 같은 화풍 `ui_dsb_none`(LoRA 없음) · 로컬 ComfyUI + Nova Anime XL(`novaAnimeXL_ilV130`) · 고른 것 = `ui5_btn_roll4_none_v03`(피 튄 깃털) · `ui5_btn_flask_none_v02`(둥근 유리병) · `ui5_btn_skill_none_v03`(소용돌이 칼날) · 프롬프트 = `prompts.yaml` 의 `ui5_*` · 시드 = `resources/art/out/ui5/art_manifest.json` · 원본 `art_src/ui/btn_*.webp` → `bake_ui.py buttons`(종이를 지우고 큰 덩어리 둘레만 남김). 사람 손 안 댐 · 밖으로 나간 것 없음.

### 3-4-1. 프롤로그 횃불 (2026-11-06 · D-148)

`parts/prop_torch.webp` — 원본 `Studio/projects/ProjectEighth/resources/art/out/sb_prop/ui10_torch2_v04.png`(Nova Anime XL · LoRA 없음 · 프롬프트 · 시드 = `art_manifest.json`). 아래쪽에 끼어든 작은 생물은 잘라 냈다(`art_src/ui/torch.webp` = 위 70%).

### 3-4-2. 말풍선 (2026-11-06 · D-152)

`parts/ui_bubble_body · ui_bubble_tail · ui_shout2.webp` — 밑그림(코드)을 깔고 ComfyUI img2img(Nova Anime XL · LoRA 없음 · 0.6). 원본 = `resources/art/out/ui_dsb_tex/ui14_dialog_v01.png` · `ui_dsb_frame/ui13_shout_v02.png` · 프롬프트 · 시드 = `art_manifest.json`. 밑그림 = `D:/AI/ComfyUI/input/pe_bubble2_*.png`.

### 3-5. 말풍선 시험 모델 (2026-11-06 · 시험 중, 게임에 아직 안 넣음)

| 모델 | 출처 | 파일 · SHA256 | 권한(Civitai API 2026-11-06) |
| --- | --- | --- | --- |
| Multi-Genre Game UI Panels · 제작자 `Warfrost` | https://civitai.com/models/1869446 | `game_ui_panels.safetensors`(이미 설치 · ProjectIdle 감사 캐시) | `Image, RentCivit, Rent` · 🔴 **`allowNoCredit = false` — 쓰면 제작자를 표기해야 한다** |
| Comic page generator · Illustrious Manga Boxes · 제작자 `vaszkull` | https://civitai.com/models/1577414 (버전 1785024) | `Comic_page_generator__Illustrious_Manga_Boxes.safetensors` · 223,106 KB · `8ABAE25CF478F2DD77F0D7F53419F364A831EF8B31FBDB3EBF98138CB0FA42E3`(받은 파일과 일치) | `RentCivit, Image` · 표기 의무 없음 |

- ⏳ 프롬프트 원문 · 사용한 요금제 · 상업 이용 조건은 출시 전에 확인해 여기에 적는다. 3방향 프롬프트 초안은 AI 가 썼고, 사용자가 ChatGPT 에서 고쳤는지는 확인하지 않았다.
