# yarn-1-workspace
yarn workwpace는 사용자가 여러개의 package.json으로 부터 dependencies를 설치할 수 있는 기능입니다.

## 시작하기
`npm install --global yarn`

### [1. root package.json에서 workspaces를 정의합니다.](https://github.com/songbetter/yarn-1-workspace/commit/de22e8df264bc176f142c4b3d752f241b58d15c1) 
1. workspace에 packages/* 을 추가합니다.
2. private 설정을 해줍니다.

### [2. packages 폴더를 생성합니다.](https://github.com/songbetter/yarn-1-workspace/commit/d562af3005195e81b3787aeb711995877a23fcca)
1. packages 하위 폴더를 만들고 package.json을 생성합니다.
2. 의존성 주입 시 인식하기 쉬운 이름으로 변경합니다. @study/common

### [3. packages 하위 폴더 간 의존성을 주입합니다.](https://github.com/songbetter/yarn-1-workspace/commit/99fb3cdc87016001ada8d043e3cc9d888c13b226)
`yarn workspace @study/server add @study/common@1.0.0`

## 서버 실행하기
`yarn workspace @study@server env`

### Reference
[Workspaces in Yarn](https://classic.yarnpkg.com/blog/2017/08/02/introducing-workspaces/)<br/>
[How to use it?](https://classic.yarnpkg.com/en/docs/workspaces#toc-how-to-use-it)
