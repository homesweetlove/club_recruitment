# Club Recruitment

팀 소개·프로젝트·활동·채용 안내 화면과 개발 학습 아카이브를 담은 **정적 웹사이트**입니다. 기존 `remind.github.io`의 메인 페이지와 학습 아카이브를 한 저장소의 `main` 브랜치로 통합했습니다.

## 페이지 구성

| 경로 | 내용 |
| --- | --- |
| [`index.html`](./index.html) | 메인 포트폴리오/팀 소개 페이지. 멤버, 프로젝트, 활동, 채용 화면과 다크·라이트 테마 전환 |
| [`club/index.html`](./club/index.html) | 메인 페이지의 별도 경로 버전 |
| [`study/index.html`](./study/index.html) | **Study Archive**. 카테고리 필터와 학습 글 목록 |
| [`study/posts/`](./study/posts/) | C 언어, Python, 개발 영어, 기초 수학 관련 학습 글 8개 |

메인 화면의 **Study Archive — 학습 노트 보기** 링크를 통해 학습 아카이브로 이동할 수 있습니다.

## 기술 구성

- HTML5, CSS3, JavaScript (별도 프레임워크 없이 동작)
- 메인 페이지: HTML 파일 내부 스타일·스크립트
- Study Archive: `study/css/style.css`, `study/js/app.js` 및 `study/posts/` 문서
- 별도 빌드 도구·데이터베이스·백엔드 서버 없음

## 로컬 실행

```bash
git clone https://github.com/homesweetlove/club_recruitment.git
cd club_recruitment
python -m http.server 8000
```

브라우저에서 다음 경로로 접속합니다.

- 메인: <http://localhost:8000/>
- 클럽 페이지: <http://localhost:8000/club/>
- 학습 아카이브: <http://localhost:8000/study/>

정적 파일이므로 `index.html`을 직접 열 수도 있지만, 로컬 웹 서버를 사용하면 배포 환경에 가까운 경로로 확인할 수 있습니다.

## 주의 사항

> **지원 폼은 데모 UI입니다.** 브라우저에서 제출 확인 알림만 표시하며, 입력한 지원서는 서버로 전송되거나 저장되지 않습니다. 실제 모집·접수 기능으로 사용하려면 별도의 전송 및 개인정보 처리 기능을 구현해야 합니다.

사이트 안의 멤버 정보, 프로젝트 링크, 채용 일정 등 일부 콘텐츠는 예시 데이터입니다. 실제 운영 중인 모집 정보로 간주하지 마세요.

## 배포

GitHub Pages에서 **Settings → Pages → Deploy from a branch → main / (root)** 를 선택하면 정적 사이트를 배포할 수 있습니다.

설정 후 예상 경로:

- 메인: `https://homesweetlove.github.io/club_recruitment/`
- 학습 아카이브: `https://homesweetlove.github.io/club_recruitment/study/`

GitHub Pages 활성화 여부는 별도로 확인해야 합니다.

---

원본: [zlem8952/remind.github.io](https://github.com/zlem8952/remind.github.io)
