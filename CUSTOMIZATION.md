# 🛠️ 웹사이트 커스터마이징 질문지

아래 항목들을 채워주시면, 해당 내용으로 웹사이트를 수정해드리겠습니다.
비워두는 항목은 해당 섹션을 제거하거나 비활성화합니다.

> 💡 주석(`<!-- 예시 -->`)은 참고용입니다. 답변 작성 후 지워주세요.

---

## 1. 🪪 기본 정보

> 파일: `src/config.ts`, `BaseLayout.astro`, `BaseHead.astro`

| 항목 | 답변 |
|------|------|
| 사이트 제목 | "Seongju Park" |
| 사이트 설명 (meta description) | 박성주의 정보, 관심사 등을 적어둔 소개 페이지 입니다. (Engligh) |
| 테마 | <!-- 현재: "lofi". DaisyUI 테마 목록: light, dark, cupcake, bumblebee, emerald, corporate, synthwave, retro, cyberpunk, valentine, halloween, garden, forest, aqua, lofi, pastel, fantasy, wireframe, black, luxury, dracula, cmyk, autumn, business, acid, lemonade, night, coffee, winter --> (답변 불가 뭐가 좋은지 모름. 근데 지금도 괜찮음)|
| 언어 | En, Ko 둘 다 있으면 좋겠어. 우선 내가 적은 것들을 영어로 적어줘. Korean 으로 보여주는 것은 나중에 적자. |

---

## 2. 🏠 홈페이지 (index)

> 파일: `src/pages/index.astro`

### 인사 & 자기소개
| 항목 | 답변 |
|------|------|
| 인사말 | Hi! I'm SeongjuPark |
| 이름 | 박성주 |
| 직함/역할 | 포항공과대학교 컴퓨터공학과 학부생 4th grade. |
| 자기소개 문단 | (AI, HCI, 심리) 에 전반적으로 관심있어 하는 사람으로 궁극적으로는 필요하지만 주목받지 못 하는 연구를 하고 싶어. 최근에는 AI와 사람의 멘탈 모델이 얼마나 alignment 되어 있는지, 이를 통해 잘 알지 못했던 autism 에 대해 더 알수 있을지 관심있어하고 있어. |

### 홈페이지 버튼
| 항목 | 답변 |
|------|------|
| 버튼 1 텍스트 & 링크 | Connect via email -> psj066@postech.ac.kr 로 메일 작성하도록 한 대표적인 방법 활용 |
| 버튼 2 텍스트 & 링크 | More information -> CV 로 이동 |

### 홈 프로젝트 카드 (최근 프로젝트 3개)
<!-- 
각 프로젝트 예시 형식:
- 제목: "My Research Paper"
- 설명: "A study on..."
- 링크: "https://..."
- 이미지: (파일을 public/ 폴더에 넣어주세요)
- 뱃지: "NEW", "논문", 등 (선택)
-->
이 부분들은 비워두고, 하나 하나 채워갈거야. 아직은 빈 칸으로 남겨둬.
| # | 제목 | 설명 | 링크 | 뱃지 |
|---|------|------|------|------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

---

## 3. 📄 CV / 이력서 페이지

> 파일: `src/pages/cv.astro`

### Profile (자기소개)
```
여기에 자기소개 작성 (1~2문단)
```

### Education (학력)
<!-- 
예시 형식:
- 학위: "Ph.D. in Computer Science"
- 기간: "2020 to 2024"
- 학교: "POSTECH, Pohang, South Korea"
-->

| # | 학위/전공 | 기간 | 학교/도시/국가 |
|---|----------|------|---------------|
| 1 |학사/컴퓨터공학과 |재학중 | 포항공과대학교|
| 2 | | | |

### Experience (경력)
<!-- 
예시 형식:
- 직함: "Research Assistant"
- 기간: "From Mar 2022 to Present"
- 회사: "POSTECH AI Lab, Pohang"
- 설명: "연구 내용이나 담당 업무 설명"
-->

| # | 직함 | 기간 | 회사/장소 | 설명 |
|---|------|------|----------|------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

### Certifications (자격증) — 없으면 비워주세요
| # | 자격증명 | 링크 (선택) |
|---|---------|------------|
| 1 | | |
| 2 | | |

### Skills (기술 스택)
<!-- 쉼표로 구분해서 나열해주세요 -->
```
예: Python, C++, PyTorch, Linux, Docker, ...
```

---

## 4. 🔬 Projects 페이지

> 파일: `src/pages/projects.astro`

### 프로젝트 카테고리 (섹션 제목)
<!-- 현재 "Projects Header"가 2개. 카테고리를 어떻게 나눌지 결정 -->
<!-- 예: "Research Projects", "Side Projects", "Open Source" 등 -->

| 카테고리명 | 포함할 프로젝트 수 |
|-----------|-------------------|
| | |
| | |

### 프로젝트 목록
| # | 카테고리 | 제목 | 설명 | 링크 | 뱃지 |
|---|---------|------|------|------|------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

---

## 5. 🛎️ Services 페이지 — 필요 여부
필요 없어. 아예 없애줘도 돼
> 파일: `src/pages/services.astro`

| 항목 | 답변 |
|------|------|
| Services 페이지 유지? | <!-- 예/아니오. 아니면 메뉴에서 제거합니다 --> |
| 유지한다면 어떤 서비스? | <!-- 예: "Consulting", "Tutoring" 등 --> |

---

## 6. 🛒 Store 페이지 — 필요 여부
필요 없어. 아예 없애줘도 돼
> 파일: `src/pages/store/`, `src/content/store/`

| 항목 | 답변 |
|------|------|
| Store 페이지 유지? | <!-- 예/아니오. 아니면 메뉴에서 제거합니다 --> |

---

## 7. ✍️ Blog — 필요 여부
필요 없지만 사용할 수도 있어. 일단은 Project처럼 나중에 채울 용도로 작성해줘.
> 파일: `src/content/blog/`, `src/pages/blog/`

| 항목 | 답변 |
|------|------|
| Blog 유지? | <!-- 예/아니오 --> |
| 기존 데모 포스트 삭제? | <!-- 예/아니오 --> |

---

## 8. 📱 사이드바 & 소셜 링크

> 파일: `SideBarFooter.astro`, `SideBarMenu.astro`

### 프로필 사진
| 항목 | 답변 |
|------|------|
| 프로필 사진 | <!-- public/profile.webp를 교체해주시거나, 파일 경로 알려주세요 --> |

### 메뉴 구성
<!-- 현재 메뉴: Home, Projects, Services, Store, Blog, CV, Contact -->
<!-- 필요 없는 메뉴를 삭제 표시해주세요 -->

| 메뉴 | 유지/삭제 |
|------|----------|
| Home | 유지|
| Projects | 유지|
| Services | 삭제 |
| Store | 삭제 |
| Blog | 유지 |
| CV | 유지 |
| Contact | Home에 합쳐져도 될듯. 굳이? |

### 소셜 링크
<!-- 필요 없는 항목은 비워두세요 → 해당 아이콘 제거합니다 -->

| 플랫폼 | URL |
|--------|-----|
| GitHub | psj066@github.com |
| Twitter/X | |
| LinkedIn | |
| Google Scholar | 주석처리 해줘. 언젠가는 넣을거야. | 
| 이메일 | psj066@postech.ac.kr |
| 인스타그램 | @to_templato_vida |

### Contact 메일 주소
| 항목 | 답변 |
|------|------|
| 이메일 | psj066@postech.ac.kr |

---

## 9. 🎨 이미지 & 미디어

> 파일: `public/` 폴더

| 항목 | 설명 | 답변 |
|------|------|------|
| 프로필 사진 | `public/profile.webp` 교체 | <!-- 파일 경로 또는 "나중에" --> |
| 파비콘 | `public/favicon.svg` 교체 | <!-- 파일 경로 또는 유지 --> |
| OG 이미지 | `public/social_img.webp` (SNS 공유 시 썸네일) | <!-- 교체? --> |
| 프로젝트 이미지 | 각 프로젝트 카드에 사용할 이미지 | <!-- 파일 제공 or 기본 유지 --> |

---

## 10. 🦶 Footer (하단)

> 파일: `src/components/Footer.astro`

| 항목 | 답변 |
|------|------|
| 하단 저작권 표시 이름 | 저작권 유지|
| "Developed by" 문구 | 저작원 유지 |

---

## ✅ 작성 완료 후

위 항목들을 채워주시면, 내용에 맞게 모든 파일을 수정해드리겠습니다!
- 비워둔 섹션은 메뉴에서 제거하고 관련 페이지를 비활성화합니다.
- 이미지 파일은 `public/` 폴더에 넣어주시면 적용합니다.
