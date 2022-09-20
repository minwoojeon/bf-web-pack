# bf-web-pack
쓰다보니 자주 쓰이지만 귀찮게 할게 많았던 것들을 모아놓은 팩


### Need

- 설치해야하는 프로그램 : jQuery (동봉된 jQuery 사용 가능)

### API (추가중)

- setAppKey : `카카오 앱키 등록`

```
window.bfAddressPack.setAppKey('1234567890');
```

- setLoadingImageId : `로딩바 이미지 태그 id`

```
// <div id="loadingBar">...</div>
window.bfAddressPack.setLoadingImageId('loadingBar');
```

- setSuccessThenFn : `(콜백) 성공시`

```
// return function 의 param 은 2가지 제공
// 1. params: 전송하는 인자
// 2. response: 응신 결과
// * 일반적으로 네트워크 통신을 하는 함수의 가장 끝 인자에 제공하나 상황에 따라 사용할 수 있도록 제공
window.bfAddressPack.setSuccessThenFn(function(params, response){ ... }); // 함수 주입은 자유
```

- setErrorThenFn : `(콜백) 실패시`

```
// return function 의 param 은 1가지 제공
// 1. response: 응신 결과
// * 일반적으로 네트워크 통신을 하는 함수의 가장 끝 인자에 제공하나 상황에 따라 사용할 수 있도록 제공
window.bfAddressPack.setErrorThenFn(function(response){ ... }); // 함수 주입은 자유
```


- convertAddress2LanLng : `(카카오) 주소를 기준으로 세부 정보 조회 (완전일치)`

```
// 함수 원형
window.bfAddressPack.convertAddress2LanLng(address, successThenFn, errorThenFn);
// 인자 설명
// 1. address: String, 조회할 주소
// 2. successThenFn: function, 성공시 콜백
// 3. errorThenFn: function, 실패시 콜백
```

- convertAddresses2LanLng : `(카카오) 주소를 기준으로 세부 정보 조회`

```
// 함수 원형
window.bfAddressPack.convertAddresses2LanLng(address, successThenFn, errorThenFn);
// 인자 설명
// 1. address: String, 조회할 주소
// 2. successThenFn: function, 성공시 콜백
// 3. errorThenFn: function, 실패시 콜백
```



- 정규식
- 서버 통신
- 토큰 분해
- 다국어 번역 (config 파일/xml 파일 파싱)
- 크롤링 (html 미파싱 데이터 콜백형)


- Copyrighted by botbinoo.
