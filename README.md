# youminki.github.io


이 저장소에서 `youminki` 폴더를 GitHub Pages(gh-pages 브랜치)로 배포하는 방법입니다.

요약:

- 배포 URL: [https://youminki.github.io/youminki](https://youminki.github.io/youminki)
- 사용 패키지: `gh-pages`

설치 및 배포 방법:

1. gh-pages 설치 (로컬 또는 CI에서 실행):

```bash
npm install --save-dev gh-pages
```


2. package.json에 `homepage`와 `predeploy`, `deploy` 스크립트를 이미 추가했습니다.

3. 배포 실행:

```bash
npm run deploy
```

명령 설명:

- `predeploy`는 `deploy` 실행 시 자동으로 선행 실행됩니다. 현재 예시는 정적 폴더이므로 `build-youminki`가 간단한 echo 명령입니다. 필요하면 빌드 도구(예: `webpack`, `vite`, `react-scripts`)로 교체하세요.
- `deploy`는 `gh-pages -d youminki`로 `youminki` 폴더를 `gh-pages` 브랜치로 푸시합니다.

GitHub 설정:

1. GitHub 저장소 페이지의 Settings > Pages에서 배포 브랜치를 `gh-pages`로 변경하세요(자동으로 감지될 수 있음).
2. 페이지가 활성화되기까지 몇 분 소요될 수 있습니다.

참고: GitHub에 푸시할 권한이 있어야 하고, 첫 배포 시 GitHub 인증(토큰/SSH)이 요구될 수 있습니다.

추가 도움 필요하면 알려주세요.

