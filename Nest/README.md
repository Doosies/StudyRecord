# NestJs에 대해
`Nestjs`는 `Nodejs` 기반의 **서버 애플리케이션을 위한** 프레임워크다.  
그리고 `Nestjs`는 `Typescript`로 빌드됐지만 `Javscript`도 사용이 가능하다.  
기본적으로 Express를 사용하지만 Fastify도 사용할 수 있다.

> 위의 설명은 [공식 홈페이지][공홈]에 나와있는데 Nestjs를 선택한 이유기도 하다!!  

<br>

예전에 개인 사이트를 만들기 위해 진행했던 [프로젝트][예전꺼]는 백엔드 개발을 위해 `Spring Boot`를 사용했다.  
[더 이전][더이전]에 진행했던 프로젝트에서 한번 쓴 기억이 있어서 썼던건데 지금 생각하면 잘못된 선택같다.  
`Java`의 이해도가 떨어졌기 때문에 문제가 발생했을 떄 해결하는데 시간을 많이 썼기 때문이다.  

이번엔 `Typescript`를 사용해 개발할 수 있기 때문에 백엔드 프레임워크를 `Nestjs`로 골랐다.  
이유는 이렇다.
1. 다른 언어를 학습하는데 시간을 더 쓰지 않아도 된다. 
2. 개발을 진행하며 `Typescript`에 더 익숙해질거라 생각한다.

# 프로젝트 만들기
프로젝트 생성은 `CRA`로 리액트 앱을 생성하는것만큼 매우 간단하다.  
```bash
$ npm i -g @nestjs/cli
$ nest new project-name
```
이렇게 하고 패키지 매니저를 선택하면 아래처럼 설치가 완료된다.
```bash
✔ Installation in progress... ☕

🚀  Successfully created project study
👉  Get started with the following commands:

$ cd study
$ yarn run start


                          Thanks for installing Nest 🙏
                 Please consider donating to our open collective
                        to help us maintain this package.
```
# 프로젝트 살펴보기
새로운 프로젝트를 만들면 역시 main부터 보면 된다.  
main.ts파일을 살펴보면 이렇다.  
```typescript
import { NestFactory } from '@nestjs/core';
import { AppModule } from './app.module';

async function bootstrap() {
  const app = await NestFactory.create(AppModule);
  await app.listen(3000);
}
bootstrap();

```
대충 살펴보면 app은 NestFactory를 AppModule을 사용해 만든후,  
3000번 포트에서 요청을 기다리고있다.

## 플랫폼
맨 위에서 `Nestjs`는 이렇다고 했었다.  
> 기본적으로 Express를 사용하지만 Fastify도 사용할 수 있다.  

`Nestjs`는 플랫폼에 구애받지 않는 프레임워크로 목표로 하기 때문이다.  
이에대한 설명은 [여기][플랫폼]에 더 자세히 설명되어있다.  

## 프로젝트 실행
아래 명령어를 사용해 프로그램을 실행한다.
```bash
$ npm run start:dev
```
그럼 이렇게 프로그래밍 처음 배울 때 국룰인 `Hello World`가 화면에 나온다.
![Hello]




[공홈]: https://docs.nestjs.com/
[예전꺼]: https://github.com/Doosies/portfolio
[더이전]: https://github.com/Doosies/sktelProjt
[플랫폼]: https://docs.nestjs.com/first-steps#platform

[Hello]: https://velog.velcdn.com/images/song961003/post/40f6cafc-b41c-4b61-9ffa-32b817816a68/image.png