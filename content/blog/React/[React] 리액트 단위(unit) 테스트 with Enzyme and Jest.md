---
title: '[React] 리액트 단위(unit)테스트 with React.js Unit Testing, Enzyme and Jest'
date: 2020-12-17 11:20:13
category: React
draft: false
---

![](./images/UnitTest-Logo.png)

## React.js Unit Testing

리엑트 유닛 테스팅이란 컴포넌트를 기능별로 쪼개서 아주 작은 단위로 만든 후 독립적으로 테스팅을 하는것을 의미한다. 단일 책임 원칙에 따라서 한 컴포넌트는 한 가지 역할만 하면 충분하기 때문에 역할 단위로 테스트하는 방법이다. 리액트 어플리케이션 안에 있는 **개별적인 코드 단위가 의도한 대로 동작하는지를 확인하는 방법**이라고 말할 수도 있다. 유닛 테스팅은 부가적인 것이기 때문에 무조건 해야하는것은 아니다. 소규모 개인프로젝트에는 시간낭비가 될수도 있기에 추천하지 않는다.
<br/>
<br/>
<br/>
<br/>

> **Component Testing**  
> 리액트 컴포넌트 테스팅은 아래와 같은 형식으로 이루어진다.

- 특정한 props에 따라 컴포넌트가 에러없이 렌더링 되는가?
- 과거의 렌더링 결과와 현재 렌더링 한 결과가 일치하는가?
- 특정한 DOM 이벤트의 원하는 변화가 제대로 발생하는가?
- 렌더링 된 결과물을 이미지로 저장하여 픽셀을 확인했을때 일치하는가?(이 경우 스토리북을 이용한 테스팅 추천)
  <br/>
  <br/>
  <br/>

> **with react-testing-library, Enzyme and Jest**  
> 리액트 공식문서에서 사용을 권장하는 테스팅 라이브러리는 react-testing-library 이다. 대체방안으로 Enzyme이 있으며 좀 더 큰 개념인 Jest는 테스트 프레임워크로 볼 수 있다. enzyme과 jest를 함께 사용할 수도 있다.

<br/>
<br/>

` - react-testing-library : 렌더링 결과에 더 집중을 한다. 실제 DOM 에 대해서 신경을 더 많이 쓰기 때문에 실제 화면에 무엇이 보여지는지 그리고 이벤트가 발생했을때 화면에 의도한 변화가 생겼는지 등을 확인하기에 최적화 되어있다. 따라서 react-testing-library 는 사용자의 관점에서 테스팅하기에 좋다.`

` - Enzyme : 컴포넌트의 내부 기능에 더 집중한다. 컴포넌트가 지니고 있는 props, state 를 확인하고, 컴포넌트의 내장 메서드를 직접 호출하기도 한다. 또한 Dom 이벤트를 시뮬레이트 할 수 있고, 라이프 사이클이 정상적으로 돌아가는지 확인 가능하다.`

` - Jest : jest의 스냅샷 테스팅은 컴포넌트를 주어진 설정으로 렌더링하고, 그 결과물을 파일로 저장한다. 그리고 다음에 테스트를 할 때 이전의 결과물과 일치하는지 확인한다. 변경이 발생할 경우 에러를 발생시킴으로써 컴포넌트의 의도하지 않은 변경을 추적할 수 있다.`
