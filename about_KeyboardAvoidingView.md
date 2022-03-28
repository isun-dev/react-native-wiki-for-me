# KeyboardAvoidingView
- 개발을 하다보면 Textinput위로 키보드가 나타나 불편함이 있다. 이때 KeyboardAvoidingView를 사용하여 위치를 조정해줄 수 있다.
- https://reactnative.dev/docs/keyboardavoidingview
- 아래와 같이 사용한다.
```
<KeyboardAvoidingView
            behavior={Platform.OS == 'ios' ? 'padding' : 'height'}
            enabled>
```
- https://brunch.co.kr/@hopeless/5
