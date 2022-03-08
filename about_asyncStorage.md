- 안드로이드 및 아이폰 기기 각각에서 AsyncStorage.clear(); 후 테스트해야 한다.

## 설치 방법
yarn add @react-native-async-storage/async-storage

## pod install 
터미널에서 프로젝트 위치 확인 후
cd ios && pod install

## importing to component
import AsyncStorage from '@react-native-async-storage/async-storage';

## String 값을 가져올 때
```
const getData = async () => {
  try {
    const value = await AsyncStorage.getItem('@storage_Key')
    if(value !== null) {
      // value previously stored
    }
  } catch(e) {
    // error reading value
  }
}
```
## Object 값을 가져올 때
```
const getData = async () => {
  try {
    const jsonValue = await AsyncStorage.getItem('@storage_Key')
    return jsonValue != null ? JSON.parse(jsonValue) : null;
  } catch(e) {
    // error reading value
  }
}

```
