# JWT에 대해서 제대로 이해하기

## Refresh Token
- https://tecoble.techcourse.co.kr/post/2021-10-20-refresh-token/
### 정리
- 액세스 토큰은 클라이언트단에만 저장이 되는 거기 때문에, 탈취되면 해커가 액세스 토큰이 유효한 동안에는 일반 사용자처럼 이용할 수 있다.
- 그렇기 때문에 액세스 토큰의 유효기간은 길면 안된다.
- refresh token은 access token을 재발급받을 수 있는 token이다. 
- refresh token은 서버에 저장이 된다.
