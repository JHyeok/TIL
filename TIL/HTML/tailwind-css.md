# Tailwind CSS

Tailwind CSS에서 제공되는 컴포넌트들은 직접 만들어져서 제공되는 컴포넌트라기 보다는 사용자 지정이 가능한 저수준의 CSS 프레임워크로 직접 재정의해서 사용하기 보다는 기존의 HTML태그에 CSS를 작성하듯이 사용하면 된다. Tailwind CSS에서 제공하는 클래스 이름을 사용해서 작성해야 한다.

CSS파일이 분리되어 있지 않고 HTML에서 CSS에 className으로 직접 CSS를 작성해서 사용할 수 있다. 어떠한 레이아웃 또는 디자인을 구현할 수 없을 때, Tailwind CSS에서 제공하는 HTML과 CSS를 가지고 살짝만 수정해서 원하는 방식으로도 구현할 수 있다.

컴포넌트를 재정의하기 보다는 CSS를 직접 다루는 것을 선호하는 개발자들이 좋아하는 방식이며 직관적이다.

아래는 전통적인 방식의 HTML과 CSS를 이용한 접근이다.

```html
<div class="chat-notification">
  <div class="chat-notification-logo-wrapper">
    <img class="chat-notification-logo" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div class="chat-notification-content">
    <h4 class="chat-notification-title">ChitChat</h4>
    <p class="chat-notification-message">You have a new message!</p>
  </div>
</div>

<style>
  .chat-notification {
    display: flex;
    max-width: 24rem;
    margin: 0 auto;
    padding: 1.5rem;
    border-radius: 0.5rem;
    background-color: #fff;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  .chat-notification-logo-wrapper {
    flex-shrink: 0;
  }
  .chat-notification-logo {
    height: 3rem;
    width: 3rem;
  }
  .chat-notification-content {
    margin-left: 1.5rem;
    padding-top: 0.25rem;
  }
  .chat-notification-title {
    color: #1a202c;
    font-size: 1.25rem;
    line-height: 1.25;
  }
  .chat-notification-message {
    color: #718096;
    font-size: 1rem;
    line-height: 1.5;
  }
</style>
```

Tailwind CSS를 사용하면 아래의 코드로 구현할 수 있다.

```html
<div class="max-w-sm mx-auto flex p-6 bg-white rounded-lg shadow-xl">
  <div class="flex-shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div class="ml-6 pt-1">
    <h4 class="text-xl text-gray-900 leading-tight">ChitChat</h4>
    <p class="text-base text-gray-600 leading-normal">You have a new message!</p>
  </div>
</div>
```

코드의 양도 줄어들고 직관적으로 변경되었다. 커스터마이징에도 유용할 것 같다. 

공식문서에서는 전통적인 접근 방식에서는 새 기능을 추가할 때마다 CSS 파일을 추가하거나 CSS 파일을 수정하므로 CSS파일이 커지지만, Tailwind CSS는 재사용이 가능하므로 작성할 필요가 거의 없어진다고 한다.

클래스 이름에서도 어떤 것을 스타일링하는지 지칭하는 이름의 클래스를 생성할 필요도 없으며 클래스 이름을 짓는데 시간을 낭비할 필요도 없다고 한다.

마지막으로, CSS의 변경작업은 대부분이 전역적이고 무엇이 깨질지 알 수 없지만 HTML의 클래스는 로컬이므로 다른 문제에 대해 걱정하지 않고 변경 할 수 있다고 한다.

---
#### 참고

- [공식문서](https://tailwindcss.com/docs/utility-first)
- [공식문서-설치](https://tailwindcss.com/docs/installation)
- [react native web, tailwind css](https://m.post.naver.com/viewer/postView.nhn?volumeNo=27031958&memberNo=10070839)
- [TailWind CSS 알아보기](https://velog.io/@jinsu2504/tailwind-1)