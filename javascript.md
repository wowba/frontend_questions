# Javascript Questions

- [var, let, const를 이용해 hoisting과 TDZ에 대해 설명해 주세요.](#var-let-const를-이용해-hoisting과-tdz에-대해-설명해-주세요)
- [자바스크립트로 CSS를 조작하다보면 FOUC(Flash of Unstyled Content)가 발생하는 경우가 있는데, 이 현상이 DOM과 어떤 관련이 있는지 설명해보실래요?](#자바스크립트로-css를-조작하다보면-foucflash-of-unstyled-content가-발생하는-경우가-있는데-이-현상이-dom과-어떤-관련이-있는지-설명해보실래요)
- [브라우저의 렌더링 과정을 설명하세요.](#브라우저의-렌더링-과정을-설명하세요)

# Answers

## var, let, const를 이용해 hoisting과 TDZ에 대해 설명해 주세요.

실행 컨텍스트가 활성화 될 때(코드를 수행할 때), 자바스크립트 엔진은 해당 컨텍스트의 코드를 실행하는 데 필요한 정보를 실행 컨텍스트에 저장합니다.

이 때 environmentRecord에는 현재 컨텍스트와 관련된 코드의 식별자 정보가 저장되는데, 컨텍스트의 처음부터 끝까지 확인하여 이 식별자들을 확인하는 과정이 hoisting 입니다.

var, let, const는 모두 hoisting을 통해 식별자 정보가 최상단으로 끌어올려지지만, 차이가 존재합니다.

var 의 경우에는 environmentRecord가 인스턴스화 될 때 undefined로 초기화 되지만, let과 const는 실제 식별자에 값이 할당되기 전에는 접근할 수 없습니다.

즉, var와는 다르게 let과 const는 undefined로 초기화 되지 않으며, 메모리에 할당되지 않기 때문에 변수가 생성된 이후 할당되기 전 일시적으로 접근할 수 없는 그 상태를 TDZ라고 부릅니다.

## 자바스크립트로 CSS를 조작하다보면 FOUC(Flash of Unstyled Content)가 발생하는 경우가 있는데, 이 현상이 DOM과 어떤 관련이 있는지 설명해보실래요?

## 브라우저의 렌더링 과정을 설명하세요.
