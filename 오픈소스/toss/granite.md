## granite

공식 깃허브 -> https://github.com/toss/granite

1. 레포지토리를 Fork하고 Fork한 내 레포지토리를 clone한다.

2. cd granite 으로 디렉토리 수정

3. yarn 세팅하기

```bash
yarn install
yarn run build
```

4. 로컬 서버 열기

폴더 중 docs으로 이동해서 열어야 합니다.

```bash
yarn docs:dev
```

```json
...
  },
  "scripts": {
    "docs:dev": "yarn vitepress dev", // dev
    "docs:build": "yarn vitepress build",
    "docs:preview": "yarn vitepress preview",
    "preview": "npx serve ./.vitepress/dist"
  }
}
```
