## Deploy React App

1. SPA 프로젝트 배포 이해하기
2. serve 패키지로 React Wep App 배포하기
3. AWS S3 에 React Wep App 배포하기
4. node.js express 로 React Web App 배포하기
5. NginX 로 React Wep App 배포하기
6. 서버사이드 렌더링 이해하기

### SPA 프로젝트 배포 이해하기

- `Single Page Application`

- `npm run build`-(in create-react-app Proj)

  - production 모드로 빌드되어, 'build' 폴더에 파일 생성
    - 이렇게 만들어진 파일들을 웹서버를 통해 사용자가 접근할 수 있도록 처리
  - build/static 폴더 안에 JS, CSS 파일들이 생성
    - 파일 이름에 hash 값이 붙는다.
    - `long term caching techniques`
    - ex\_) main.eb74f4d0.chunk.css

- SPA Deploy 특징
- 모든 요청을 서버에 하고 받아오는 형태가 아님
- 라우팅 경로에 상관없이 리액트 앱을 받아 실챙
- 라우팅은 받아온 리액트 앱을 실행 후, 적용
- static 파일을 제외한 모든 요청을 index.html 로 응답해주도록 작업
- serve -s build
- AWS S3에 배포
- node.js express
- NginX

### Serve Package

- serve 패키지를 전역으로 설치
- `npm install serve -g`
- serve 명령어를 -s 옵션으로 build 폴더 지정
  - -s 옵션은 어떤 라우팅으로 요청해도 index.html 을 응답하도록 지정
  - -s => SPA의 약자
- `serve -s build`
