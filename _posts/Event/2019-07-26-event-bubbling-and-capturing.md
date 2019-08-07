---
category: Event
path: '/Event'
title: 'Event Bubbling and Capturing'
type: 'POST'
layout: nil
---
### Event bubbling(이벤트 버블링)
이벤트 버블링은 이벤트가 버블처럼 전파 된다는 것을 뜻 한다. 가장 쉽게 생각하면 버블 버블을 생각하면 된다(!?)
아래에서 위로 이벤트가 전달 된다.

Event bubbling 예제 코드


```<body>
    <div>
        <button></button>
    </div>
</body>```



예를 들어 위와 같은 코드에서 button의 이벤트가 동작하면 div, body의 순서로 연결된 이벤트들이 동작 하게 된다.
이벤트 버블링을 막기 위해서는 event.stopPropagation()을 사용하여 이벤트가 전파하는것을 막는다.

## Event Capturing(이벤트 캡처링)
이벤트 캡처링은 이벤트 버블링과 반대 방향으로 진행 된다.

Event Capturing 예제 코드


```<body>
    <div><!--1번-->
        <div><!--2번-->
            <button></button><!--3번-->
        </div>
    </div>
</body>```


예를 들어 위와 같은 코드에서 div 또는 button의 이벤트를 발생 시켰을 경우 body, div(1번), div(2번), button(3번) 의 순서로 이벤트들이 동작 하게 된다.

## Event Capturing(이벤트 캡처링) 발생 방법
자바스크립트는 이벤트 버블링을 기본으로 한다. addEventListener메서드에 파라미터로 useCapture=true를 넣게되면 캡처링으로 동작하게 된다.
