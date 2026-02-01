---
title: Vite로 React 프로젝트 시작하기
author: amie
categories: [Web, React]
tags: [React, Vite, Study]
---

## Vite

Vite는 프랑스어로 "Quick", 즉 빠르다는 뜻이다. 

이름이 말해주듯 Vite는 빠르고 간결한 프론트엔드 빌드 툴이다.

Vite는 리액트 앱을 빠르게 생성하고 가볍게 실행할 수 있게 해준다.


## Node

Vite는 Node package manager(npm)로 설치할 수 있다.

그럼 Node란 무엇인가?

Node.js는 자바스크립트 코드를 서버 환경에서 실행할 수 있게 해주는 런타임이다. 

Node를 설치하면 자동으로 npm도 함께 설치되어 사용할 수 있게 된다.

[설치는 여기에서...](http://nodejs.org/en/download)

설치를 완료했다면 터미널에 `node -v`를 입력했을 때 버전이 출력된다.


## Vite 설치 

사실 Vite는 별도로 글로벌 설치할 필요 없이 프로젝트 생성 시 자동으로 설치된다. 

하지만 원한다면 아래 명령어로 최신 버전의 Vite를 설치할 수도 있다.
```shell
npm install -g vite@latest
```


## 리액트 앱 세팅

이제 리액트 프로젝트를 만들 수 있다!
```shell
npm create vite@latest
```

위의 명령어를 입력하면 우선 프로젝트명을 뭘로 설정할지 묻는다. 원하는 이름을 입력하고 엔터를 쳐준다.

![](/assets/img/posts/2026-02-02/img1.png){: .w-75 .normal}

이번엔 어떤 프레임워크를 선택할지 묻는데, 방향키로 내려 React를 골라준다.

![](/assets/img/posts/2026-02-02/img2.png){: .w-75 .normal}

이건 프로젝트 스택에 따라 골라주면 된다. 

JavaScript를 선택하면 일반 JS로, TypeScript를 선택하면 TS 환경으로 프로젝트가 구성된다.

![](/assets/img/posts/2026-02-02/img3.png){: .w-75 .normal}


## 리액트 앱 실행

프로젝트 생성이 완료되면 다음 명령어로 실행할 수 있다.
```shell
cd my-project
npm install
npm run dev
```

생성 시에 아래 옵션을 선택했다면 자동으로 설치 및 실행이 진행된다.
![](/assets/img/posts/2026-02-02/img4.png){: .w-75 .normal}

`npm install`은 프로젝트 실행에 필요한 여러 패키지와 종속성을 설치한다.

`npm run dev`로 실행하면 개발 서버가 로컬에 띄워진다.

![](/assets/img/posts/2026-02-02/img5.png){: .w-75 .normal}

터미널에 이렇게 떴다면 잘 실행된 것이고, 화면에 표시된 http://localhost:5173/ 로 접속해보면 초기 화면이 잘 떠있는 걸 확인할 수 있다!

![](/assets/img/posts/2026-02-02/img6.png){: .w-75 .normal}

## Vite 앱 구조

그럼 다시 Vite로 돌아가서,

앞서 말한대로 Vite가 몇 개의 입력만으로 아주 빠르게 React 프로젝트를 생성해줬다.

그럼 이 녀석이 뭘 만들었는지 확인해보자.

- `src/App.jsx`: `<App>` 컴포넌트를 위한 코드.
- `src/main.jsx`: React 앱의 진입점. 여기서 App 컴포넌트를 렌더링한다.
- `src/index.css`: 리액트 앱을 위한 기본 스타일.
- `index.html`: 리액트 앱의 HTML 템플릿. Vite는 이 파일을 기반으로 앱을 서빙한다.
- `package.json`: 이 앱을 실행하기 위해 사용되는 외부 패키지 목록과 스크립트 정의.
- `vite.config.js`: Vite 설정 파일. 빌드 옵션이나 플러그인 등을 여기서 관리한다.


## 마무리

Vite는 기존 CRA(Create React App)보다 훨씬 빠른 개발 서버 구동 속도와 HMR(Hot Module Replacement)를 제공한다. 이는 ES 모듈을 네이티브로 활용하고, esbuild로 사전 번들링을 수행하기 때문이다.

처음 React를 시작한다면 Vite로 프로젝트를 세팅하는 것을 추천한다. 빠르고, 가볍고, 설정도 간단하니까!