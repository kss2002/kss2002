## frontend-fundamentals

공식 깃허브 -> https://github.com/toss/frontend-fundamentals

1. 레포지토리를 Fork하고 Fork한 내 레포지토리를 clone한다.

2. cd frontend-fundamentals 으로 디렉토리 수정

3. yarn 세팅하기

```bash
yarn install
yarn run build
```

4. 로컬 서버 열기

frontend-fundamentals은 2026년 기준으로 5개 챕터가 존재한다.

각각의 세부 폴더의 경로로 가야지 그 챕터에 해당되는 로컬을 열 수 있다. (이 방식이 직관적임)

ex) cd fundamentals/code-quality
-> 코드 퀄리티를 로컬로 열 수 있음.

나머지 챕터 접근시

```txt
The server is configured with a public base URL of /code-quality/ - did you mean to visit /code-quality/bundling instead?
```

404 not found이 발생한다.

```bash
yarn docs:dev
```

TIL의 경우, 개인 SPA을 할당 받았기에 yarn dev로 로컬 서버를 열어야 한다.

path -> package.json

```json
...
"scripts": {
    "docs:dev": "yarn workspace @frontend-fundamentals/code-quality docs:dev",
    "docs:build": "yarn workspace @frontend-fundamentals/code-quality docs:build",
    "docs:preview": "yarn workspace @frontend-fundamentals/code-quality docs:preview",
    "docs:bundle:dev": "yarn workspace @frontend-fundamentals/bundling docs:dev",
    "docs:bundle:build": "yarn workspace @frontend-fundamentals/bundling docs:build",
    "docs:bundle:preview": "yarn workspace @frontend-fundamentals/bundling docs:preview",
    "docs:debug:dev": "yarn workspace @frontend-fundamentals/debug docs:dev",
    "docs:debug:build": "yarn workspace @frontend-fundamentals/debug docs:build",
    "docs:debug:preview": "yarn workspace @frontend-fundamentals/debug docs:preview",
    "docs:a11y:dev": "yarn workspace @frontend-fundamentals/a11y docs:dev",
    "docs:a11y:build": "yarn workspace @frontend-fundamentals/a11y docs:build",
    "docs:a11y:preview": "yarn workspace @frontend-fundamentals/a11y docs:preview",
    "docs:til:dev": "yarn workspace @frontend-fundamentals/today-i-learned dev",
    "docs:til:build": "yarn workspace @frontend-fundamentals/today-i-learned build",
    "docs:til:preview": "yarn workspace @frontend-fundamentals/today-i-learned preview",
}
...
```
