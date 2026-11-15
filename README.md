# 샤로로앙 (SHAROROANE) 공식 브랜드 웹사이트

> **“불필요한 것은 덜어내고, 피부에 필요한 것만 남깁니다.”**  
> 몽드플로(Mondflo)에서 전개하는 미니멀 더마 뷰티 브랜드 샤로로앙의 공식 랜딩페이지입니다.

---

## 1. 프로젝트 특징

- **미니멀 & 럭셔리 감각 디자인**: 차분한 뉴트럴 크림/샌드 톤과 클래식 세리프 타이포그래피(Cormorant Garamond + Pretendard) 적용
- **단일 원페이지 롱스크롤 (One-Page Storytelling)**: 4대 핵심 메뉴(`BRAND`, `PRODUCT`, `SCIENCE & LAB`, `SHOP`)를 매끄러운 스크롤 인터랙션으로 연결
- **사진 준비팀을 위한 친절한 비주얼 가이드**: 사진이 교체되기 전에도 완성도 높은 미니멀 레이아웃을 유지하며, 추천 사진 규격(화각, 비율, 픽셀 권장치)을 각 플레이스홀더에 명시
- **GitHub Pages 최적화 정적 웹**: 복잡한 빌드 단계 없이 GitHub 저장소에 `index.html`을 올리는 것만으로 즉시 전 세계 배포 및 무료 SSL(HTTPS) 적용

---

## 2. 사진 교체 가이드 (디자인/촬영팀 협업 시)

추후 사진 촬영 및 보정 완료 시, `index.html` 내의 `.placeholder-box` 영역을 `<img>` 태그로 교체하시면 됩니다:

| 섹션 | 추천 사진 내용 | 권장 비율 / 규격 |
| :--- | :--- | :--- |
| **Hero 우측** | 아침 자연광을 머금은 세럼 보틀 무드 컷 | 4:5 세로형 (1200 × 1500px) |
| **Brand Story** | 피부결 질감 또는 차분한 오브제/자연 연출 컷 | 1:1 정사각 (1000 × 1000px) |
| **Product Shot** | 위스퍼링 하이드레이션 세럼 보틀 누끼 및 연출 컷 | 3:4 세로형 (1200 × 1600px) |
| **Texture Close-up** | 밀키(Milky) 텍스처 도포 클로즈업/매크로 샷 | 21:9 와이드 (1680 × 720px) |
| **Science & Lab** | 시험 분석 그래프, 성적서 인포그래픽 그래픽 | 1:1 정사각 (800 × 800px) |

---

## 3. GitHub Pages 배포 및 커스텀 도메인 연결 방법

### Step 1: GitHub 저장소 생성 및 푸시
```bash
git init
git add index.html README.md
git commit -m "feat: 샤로로앙 공식 브랜드 랜딩페이지 템플릿 구축"
git branch -M main
git remote add origin https://github.com/<사용자계정>/<저장소이름>.git
git push -u origin main
```

### Step 2: GitHub Pages 활성화
1. GitHub 저장소의 **Settings** > **Pages** 메뉴로 이동합니다.
2. **Build and deployment** 항목의 **Source**를 `Deploy from a branch`로 설정합니다.
3. Branch를 `main` / `/(root)`로 지정하고 **Save**를 누릅니다.
4. 약 1~2분 후 `https://<사용자계정>.github.io/<저장소이름>/` 주소로 사이트가 즉시 오픈됩니다.

### Step 3: 구매하신 커스텀 도메인 연결
1. **GitHub Pages 설정**:
   - 동일한 **Settings** > **Pages** 페이지의 **Custom domain** 입력창에 구매하신 도메인(예: `sharoroane.com` 또는 `www.sharoroane.com`)을 입력하고 **Save**를 클릭합니다.
   - 하단의 **Enforce HTTPS**를 체크합니다 (SSL 자동 적용).
2. **도메인 구매처 DNS 설정** (가비아, 후이즈, 알리고, Cloudflare 등):
   - **루트 도메인 (`sharoroane.com`) 연결 시 (A 레코드)**:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **서브 도메인 (`www.sharoroane.com`) 연결 시 (CNAME 레코드)**:
     - 호스트: `www` / 값: `<사용자계정>.github.io`
