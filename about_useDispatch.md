# useDispatch() 사용 시 주의할 점
- AXIOS로 API통신을 할 때 axios.interceptors.response.use() 와 같이 인터셉터를 사용해서, response를 받고 호출한곳으로 return을 하기 전에, 토큰을 저장하는 등 다른 작업을 진행할 수 있다. 
- useDispatch를 사용해서  리프레시 토큰값을 store에 저장하려고 했으나 Hook 에러가 났다.
- 이와 관련해서 서치를 해보니, 아래와 같은 답을 얻을 수 있었다.
```
useDispatch must be called within the context of a React Component.
useDispatch는 반드시 리액트 컴포넌트 내에서만 사용해야 한다.
```
- 이에 대한 해결 방법으로는 
- https://stackoverflow.com/questions/60643890/redux-dispatch-not-work-when-use-in-axios-interceptors
- 위 링크에서 확인은 했다.
- 기존에 만들어논 store를 먼저 import 한 후, 아래와 같이 코드를 작성했고, FLIPPER 로 리덕스를 확인한 결과, state가 정상적으로 업데이트 된 것을 확인했다.
```
reduxStore.dispatch({
  type: 'reducer 액션 타입',
  payload: 저장 혹은 변경할 데이터 값,
});
```
