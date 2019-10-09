* Exception을 발생시켜서 테스트를 해보려는 과정 중에 java.lang.VerifyError가 발생했다.
* 어떤 방법을 사용해도 달라지지가 않아서 고민을 하던 차에 다른 분의 도움(갓구글링!)을 받아서 해결할 수 있었다.

### VerifyError 발생 원인
1. 사용한 라이브러리가 상위 버전의 JDK에서 컴파일된 경우
- 이번 case는 테스트하려는 환경은 JDK1.6이고, 내가 만든 테스트 어플리케이션은 JDK1.8에서 컴파일을 했기 때문에 발생
- 다른 해결 방법으로는 옵션으로 -Xverify:none을 넣으면 된다는 말도 봤다.