# 🎸 Guitar Tutor 프로젝트 관리 및 운영 가이드

이 문서는 **Guitar Tutor (일렉트릭 기타 학습 로드맵)** 프로젝트의 온라인 배포 정보와 GitHub 연동 및 업데이트 방법을 기록한 가이드입니다.

---

## 1. 🌐 온라인 링크

| 항목 | URL | 설명 |
|------|-----|------|
| **웹사이트 바로보기 (GitHub Pages)** | [https://kkomjirak.github.io/Guitar_tutor/](https://kkomjirak.github.io/Guitar_tutor/) | 스마트폰, 태블릿, PC 등 어디서나 접속 가능 |
| **GitHub 소스코드 저장소** | [https://github.com/kkomjirak/Guitar_tutor](https://github.com/kkomjirak/Guitar_tutor) | 전체 소스코드 및 커밋 히스토리 보관소 |

---

## 2. 📁 프로젝트 파일 구성

```text
Tutor/
├── index.html       # 기타 학습 로드맵 메인 인터랙티브 웹페이지
├── images/
│   └── hero.jpg     # 히어로 배경 고화질 기타 이미지 (1920x1277)
├── README.md        # GitHub 저장소 소개 문서
├── guide.md         # 프로젝트 운영 및 Git 연동 가이드 (본 파일)
└── .gitignore       # macOS .DS_Store 등 불필요한 시스템 파일 제외
```

---

## 3. 🔄 작업 내용 GitHub 자동 반영 방법

로컬 작업 폴더(`Tutor`)의 원격 저장소(`origin`)가 GitHub 저장소(`kkomjirak/Guitar_tutor`)의 `main` 브랜치로 자동 푸시되도록 구성되어 있습니다.

### 변경 사항을 반영할 때 실행하는 명령어:

```bash
git add .
git commit -m "수정 내용 설명"
git push
```

> [!TIP]
> - `git push`를 실행하면 로컬 `Tutor` 브랜치의 변경 사항이 원격 저장소의 `main` 브랜치로 바로 업로드됩니다.
> - 푸시 후 GitHub Actions(`pages-build-deployment`)가 자동으로 작동하여 **약 30초 내에 온라인 웹사이트(GitHub Pages)에 변경 사항이 자동 반영**됩니다.
> - 또는 AI 어시스턴트에게 *"수정한 내용 GitHub에 올려줘"*라고 요청하셔도 자동으로 커밋 및 푸시가 완료됩니다.

---

## 4. ⚙️ Git 환경 설정 정보

- **로컬 작업 디렉토리**: `/Volumes/Hagibis/Works/AI/Orca/Guitar_tutor/Tutor`
- **로컬 브랜치**: `Tutor`
- **원격 저장소 (Remote)**: `origin` (`https://github.com/kkomjirak/Guitar_tutor.git`)
- **원격 업스트림 브랜치**: `origin/main`
- **푸시 기본 설정**: `push.default = upstream` (브랜치 이름이 달라도 상위 브랜치로 자동 푸시)
- **호스팅 방식**: GitHub Pages (Branch: `main`, Path: `/`)
