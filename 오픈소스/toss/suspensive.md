## suspensive

공식 깃허브 -> https://github.com/toss/suspensive

1. 레포지토리를 Fork하고 Fork한 내 레포지토리를 clone한다.

2. cd suspensive 으로 디렉토리 수정

3. 올바른 Node 버전을 사용하기.

.nvmrc 파일에 명시된 버전을 사용하면 된다. 로컬 머신의 Node 버전을 간편하게 관리하려면 nvm 사용을 강력히 권장한다.

4. 패키지를 설치하기.

suspensive는 pnpm@9.15.4 버전을 사용한다.

가능하면 corepack을 사용하여 pnpm을 설치하기. corepack을 사용하면 package.json 파일의 packageManager 필드에 지정된 버전을 자동으로 사용하도록 pnpm을 설치할 수 있다.

```bash
corepack enable && corepack prepare
pnpm install
```

5. pnpm 설치 후 빌드

```bash
pnpm run build
```

위 명령어로 빌드하기. 만일 이후에도 모듈을 못 가져온다면 클린이 필요하다.

```bash
pnpm run clean
```

path -> packages/react/package.json

```json
...
"scripts": {
    "build": "tsdown",
    "ci:eslint": "eslint \"**/*.{ts,tsx,cts,mts}\"",
    "ci:test": "vitest run",
    "ci:type": "tsc --noEmit",
    "clean": "rimraf ./dist ./coverage ./node_modules",
    "test:ui": "vitest --ui"
  },
```

6. 로컬 서버 열기

폴더 중 docs/suspensive.org으로 이동해서 열어야 합니다.

```bash
pnpm dev
```
