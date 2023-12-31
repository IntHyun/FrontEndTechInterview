Q. prototype에 대해 설명해보세요.

```
모든 JS 객체는 prototype이라는 내부 속성을 가지고 있습니다.

prototype은 여러 객체들 간에 공통된 프로퍼티와 메서드를 사용하기 위해 prototype을 활용할 수 있습니다.
예를 들어 js에서 함수는 객체이기 때문에 prtotoype을 사용한다면 함수로부터 생성된 객체들이 공통된 프로퍼티와 메서드를 상속받을 수 있게 할 수 있습니다.

좀 더 예를 들어보겠습니다. 생성자 함수를 통해 Foo라는 함수를 생성한 뒤 Foo.prototype에 메서드를 추가합니다.
그 뒤 새로운 인스턴스를 Foo 생성자 함수로 생성하게 되면 만들어진 새로운 인스턴스들은 모두 prototype 에 선언한 메서드들을 상속받게 됩니다.
생성자 함수내에서도 메서드를 정의할 수 있겠지만 prototype에 메서드를 등록하는 이유는 메모리를 효율적으로 사용하기 위함입니다.

생성자 함수내에서 메서드를 정의하게 된다면 새롭게 생기는 인스턴스마다 독립적으로 해당 메서드를 가지게되고 해당 메서드는 각각 별도의 메모리 공간에 해당메서드를 등록하게 됩니다.
그러나 prototype에 해당 메서드를 등록하게 되면 prototype 객체에 단 한 번만 정의되며 모든 객체가 이를 공유하므로 메모리 사용이 효율적이라는 측면에서
prototype을 사용하게 되는 것입니다.
```
