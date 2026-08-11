# 고운숨결 문학상 · 독후감 공모전 홈페이지

정적 HTML 한 파일(`index.html`)로 이루어진 사이트입니다. 별도 서버나 빌드 과정 없이
Vercel, Netlify 등 정적 호스팅 서비스에 바로 올리면 됩니다.

---

## 방법 A. Netlify (가장 쉬움 — 드래그 앤 드롭)

1. https://app.netlify.com 접속 후 로그인(회원가입)
2. 대시보드에서 **"Add new site" → "Deploy manually"** 선택
3. 이 폴더(`site` 폴더, 또는 `index.html`이 들어있는 폴더)를 통째로 화면에 끌어다 놓기
4. 몇 초 후 `https://무작위이름.netlify.app` 주소로 바로 접속 가능
5. 필요하면 **Site settings → Change site name** 에서 주소를 원하는 이름으로 변경
6. 커스텀 도메인을 연결하려면 **Domain settings → Add custom domain**

---

## 방법 B. Vercel

### B-1. 웹 대시보드로 배포
1. https://vercel.com 접속 후 로그인
2. **Add New → Project → Deploy without Git (드래그 앤 드롭)** 또는
   GitHub 저장소에 이 폴더를 올린 뒤 **Import Project**로 연결
3. Framework Preset은 **Other**로 두고, Build Command·Output Directory는 비워둔 채 Deploy
4. 배포 완료 후 `https://프로젝트명.vercel.app` 주소 발급

### B-2. CLI로 배포 (Node.js 설치되어 있다면)
```bash
npm install -g vercel
cd site           # index.html이 있는 폴더로 이동
vercel             # 안내에 따라 로그인 및 배포
vercel --prod       # 실제 서비스용 배포
```

---

## 방법 C. GitHub 연동 (Vercel / Netlify 공통)

1. 이 폴더를 GitHub 저장소에 업로드
2. Vercel 또는 Netlify에서 **"Import from GitHub"** 로 해당 저장소 선택
3. 이후 저장소에 커밋을 푸시할 때마다 자동으로 재배포됩니다

---

## 참고

- 이미지(책 표지)는 `index.html` 안에 base64로 포함되어 있어 파일 하나만으로도 완전히 동작합니다.
- 접수 폼은 별도 백엔드가 없어 "제출" 시 사용자의 메일 앱이 열리며 접수 내용이 채워진 이메일 초안이 자동 생성됩니다(mailto 방식). 자동으로 서버에 저장·회신되길 원하시면 Netlify Forms, Google Forms 연동 등 별도 설정이 필요합니다.
- 커스텀 도메인을 연결하면 실제 서비스 주소(예: `www.gounsumgyeol.com`)로 운영할 수 있습니다.
