# 당신은 산이다 (The Mountain Is You) - Korean Translation

이 저장소는 브리아나 위스트(Brianna Wiest)의 저서 "The Mountain Is You"를 한국어로 번역한 Quarto 책 프로젝트입니다.

## 프로젝트 개요

이 프로젝트는 원작의 내용을 한국어 독자들에게 전달하기 위해 번역되었습니다. 책 전체 내용은 `mybook` 디렉토리 내에 Quarto 파일(`.qmd`)로 구성되어 있으며, GitHub Pages를 통해 배포됩니다.

## 프로젝트 구조 (Project Structure)

- `mybook/`: Quarto 책 소스 파일들이 포함되어 있습니다.
  - `index.qmd`: 책의 서문(Preface) 및 소개
  - `introduction.qmd`: 도입부 (Introduction)
  - `chapter1.qmd` ~ `chapter6.qmd`: 각 챕터 번역본
  - `_quarto.yml`: Quarto 프로젝트 설정 파일 (책 제목, 저자, 챕터 순서 등)
- `pixi.toml`: 의존성 관리 파일 (Quarto, Python/R 라이브러리 등)
- `.github/workflows/publish.yml`: GitHub Actions를 통한 자동 배포 워크플로우

## 사용 방법 (Usage)

이 프로젝트는 [Pixi](https://prefix.dev/)를 사용하여 의존성을 관리합니다.

### 사전 준비 (Prerequisites)

- [Pixi](https://prefix.dev/)가 설치되어 있어야 합니다.

### 로컬 개발 (Local Development)

1. 저장소 클론 (Clone the repository):

    ```bash
    git clone https://github.com/your-username/You-are-Mountain.git
    cd You-are-Mountain
    ```

2. 책 미리보기 (Preview the book):

    다음 명령어를 실행하여 Quarto 미리보기 서버를 시작합니다:

    ```bash
    pixi run quarto preview mybook
    ```

3. 책 빌드 (Build the book):

    ```bash
    pixi run quarto render mybook
    ```

## 배포 (Deployment)

이 저장소는 GitHub Actions를 사용하여 변경 사항이 `main` 브랜치에 푸시될 때 자동으로 책을 빌드하고 GitHub Pages에 배포하도록 설정되어 있습니다.

1. GitHub 설정:
    * 저장소의 Settings > Pages로 이동합니다.
    * Build and deployment 섹션에서 "Deploy from a branch"를 선택합니다.
    * 워크플로우가 처음 성공적으로 실행된 후 `gh-pages` 브랜치가 생성됩니다.
    * Branch를 `gh-pages`, 폴더를 `/(root)`로 설정하고 저장합니다.

2. 빌드 트리거:
    * `main` 브랜치에 푸시하면 워크플로우가 자동으로 실행됩니다.