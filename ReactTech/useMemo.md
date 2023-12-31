Q. useMemo에 대해 설명해주세요.

```
useMemo는 컴포넌트의 성능 최적화를 위해 사용되는 대표적인 훅입니다.
메모이제이션 기법을 활용하여 연산한 값을 재사용하는데 이전 렌더링에서 계산한 값과 현재 렌더링에서 계산한 값이 같다면
중복 연산을 하지 않고 저장해 둔 값을 재사용 함으로써 성능을 최적화 할 수 있게 도와줍니다.
useMemo의 첫 번째 인자로는 계산 비용이 많은 함수를 입력합니다. 이 함수는 useMemo 내부에서 호출되며 결과가 memoizedValue에 저장이 됩니다.
그 뒤 두 번째 인자에 감시할 배열을 작성해주고 배열에 포함된 값들 중 하나라도 변경이 된다면 계산 함수를 실행합니다. 이때 의존성 배열이 비어있다면
useMemo는 매 렌더링마다 계산 함수를 실행합니다.

이렇듯 useMemo는 주로 복잡한 계산, 데이터 가공, 외부 API 호출 등 성능에 영향을 주는 연산에서 사용하여 컴포넌트의 성능을 최적화 할 수 있게 도와줍니다.
그러나 모든 상황에서 useMemo를 사용하는 것은 아닙니다. useMemo는 추가적인 메모리를 사용하므로 성능 최적화가 필요한 경우에만 사용하는 것이 좋습니다.

요약하자면 컴포넌트 성능 최적화를 위해 사용되지만 적절한 상황에 알맞게 사용해야 한다 라고 정리할 수 있겠습니다.
```

Q. 비슷한 훅으로 useCallback도 있는데 무슨 차이가 있는가?

```
우선 두개의 훅 모두 성능 최적화를 위해 사용되는 React 훅입니다. 하지만 useMemo는 함수의 결과값을 메모이제이션하여 재사용하는 것이 주 목적입니다.
따라서 주로 계산 비용이 많은 함수의 결과 값을 재사용할 때 사용됩니다.

반면에 useCallback의 경우 함수의 결과값을 재사용하는 것이 아닌 콜백함수를 반환합니다. 따라서 이벤트 핸들러나 콜백 함수를 메모이제이션 하여 재사용하고자 할 때
주로 사용이 됩니다.

요약하자면 둘 다 성능 최적화를 위해 사용하지만 useMemo는 함수의 결과값 을 반환하고 useCallback은 콜백함수를 반환한다는 차이점이 있습니다.
```
