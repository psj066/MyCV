# 🛠️ 웹사이트 커스터마이징 질문지

아래 항목들을 채워주시면, 해당 내용으로 웹사이트를 수정해드리겠습니다.
비워두는 항목은 해당 섹션을 제거하거나 비활성화합니다.

> 💡 주석(`<!-- 예시 -->`)은 참고용입니다. 답변 작성 후 지워주세요.

---

## 1. 🪪 기본 정보

> 파일: `src/config.ts`, `BaseLayout.astro`, `BaseHead.astro`

| 항목 | 답변 |
|------|------|
| 사이트 제목 | <!-- 예: "Seongju Park | CV" (현재 값 유지?) --> |
| 사이트 설명 (meta description) | <!-- 예: "Systems & AI researcher based in Pohang" (현재 값 유지?) --> |
| 테마 | <!-- 현재: "lofi". DaisyUI 테마 목록: light, dark, cupcake, bumblebee, emerald, corporate, synthwave, retro, cyberpunk, valentine, halloween, garden, forest, aqua, lofi, pastel, fantasy, wireframe, black, luxury, dracula, cmyk, autumn, business, acid, lemonade, night, coffee, winter --> |
| 언어 | <!-- 현재: "en". "ko"로 변경? --> |

---

## 2. 🏠 홈페이지 (index)

> 파일: `src/pages/index.astro`

### 인사 & 자기소개
| 항목 | 답변 |
|------|------|
| 인사말 | <!-- 현재: "Hey there 👋" --> |
| 이름 | <!-- 현재: "I'm Manuel Ernesto" → 예: "I'm Seongju Park" --> |
| 직함/역할 | <!-- 현재: "Software Engineer and Entrepreneur" → 예: "Systems & AI Researcher" --> |
| 자기소개 문단 | <!-- 1~3줄 자유 작성 --> |

### 홈페이지 버튼
| 항목 | 답변 |
|------|------|
| 버튼 1 텍스트 & 링크 | <!-- 현재: "Let's connect!" → 트위터 링크. 이메일, 링크드인 등으로 변경? --> |
| 버튼 2 텍스트 & 링크 | <!-- 현재: "Get This template" → 삭제? 또는 다른 링크? --> |

### 홈 프로젝트 카드 (최근 프로젝트 3개)
<!-- 
각 프로젝트 예시 형식:
- 제목: "My Research Paper"
- 설명: "A study on..."
- 링크: "https://..."
- 이미지: (파일을 public/ 폴더에 넣어주세요)
- 뱃지: "NEW", "논문", 등 (선택)
-->

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
| 1 | | | |
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

> 파일: `src/pages/services.astro`

| 항목 | 답변 |
|------|------|
| Services 페이지 유지? | <!-- 예/아니오. 아니면 메뉴에서 제거합니다 --> |
| 유지한다면 어떤 서비스? | <!-- 예: "Consulting", "Tutoring" 등 --> |

---

## 6. 🛒 Store 페이지 — 필요 여부

> 파일: `src/pages/store/`, `src/content/store/`

| 항목 | 답변 |
|------|------|
| Store 페이지 유지? | <!-- 예/아니오. 아니면 메뉴에서 제거합니다 --> |

---

## 7. ✍️ Blog — 필요 여부

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
| Home | |
| Projects | |
| Services | |
| Store | |
| Blog | |
| CV | |
| Contact | |

### 소셜 링크
<!-- 필요 없는 항목은 비워두세요 → 해당 아이콘 제거합니다 -->

| 플랫폼 | URL |
|--------|-----|
| GitHub | <!-- 예: https://github.com/username --> |
| Twitter/X | |
| LinkedIn | <!-- 예: https://linkedin.com/in/username --> |
| Google Scholar | <!-- 학술 프로필이 있다면 --> |
| 이메일 | <!-- 예: your@email.com --> |
| 기타 | <!-- 추가하고 싶은 소셜 링크 --> |

### Contact 메일 주소
| 항목 | 답변 |
|------|------|
| 이메일 | <!-- 현재: contact.manuelernestog@gmail.com → 변경할 주소 --> |

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
| 하단 저작권 표시 이름 | <!-- 현재: "Manuel Ernesto" → 변경할 이름 --> |
| "Developed by" 문구 | <!-- 유지? 또는 수정? --> |

---

## ✅ 작성 완료 후

위 항목들을 채워주시면, 내용에 맞게 모든 파일을 수정해드리겠습니다!
- 비워둔 섹션은 메뉴에서 제거하고 관련 페이지를 비활성화합니다.
- 이미지 파일은 `public/` 폴더에 넣어주시면 적용합니다.
