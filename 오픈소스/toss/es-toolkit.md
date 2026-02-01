## es-toolkit

공식 깃허브 -> https://github.com/toss/es-toolkit

1. 레포지토리를 Fork하고 Fork한 내 레포지토리를 clone한다.

2. cd es-toolkit 으로 디렉토리 수정

3. 구성 요소 확인

- Node.js가 설치되어 있는지 확인하기(`.nvmrc`필요한 버전을 참조)
- Corepack 활성화:`corepack enable`

4. 필수 구성 요소를 설치

```bash
yarn install
```

5. 로컬 서버 열기

```bash
yarn docs:dev
```

```json
...
 "scripts": {
    "docs:build": "vitepress build",
    "docs:dev": "vitepress dev",
    "docs:preview": "vitepress preview"
  },
```
