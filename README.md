
# ELECTRON
![electron-logo](https://user-images.githubusercontent.com/80228504/117521003-68c4d100-afe6-11eb-96fd-393e8e975e7f.PNG)


# 서론   
kamranahmedse 양반의 개발자 로드맵을보자    
https://github.com/kamranahmedse/developer-roadmap   

`데스크톱 어플리케이션을 만들고 싶으면, 일렉트론을 배워라`
   
   
# ELECTRON 이란?   
## 뜻
> HTML, CSS, 자바스크립트를 사용해 크로스 플랫폼 데스크탑 애플리케이션을 만들기 위해 GitHub에서 개발한 오픈 소스 라이브러리

> Atom 에디터를 만들면서 공개한 오픈소스

## 구조
![캡처2](https://user-images.githubusercontent.com/80228504/117522077-49c93d80-afec-11eb-8fda-417fc6e81746.PNG)   
크로미움 - 오픈소스 웹브라우저    
NODE JS - 자바스크립트 실행 런타임 환경   
V8 - 자바스크립트 엔진    

    
 
   

# 일렉트론이 끌리는 이유?    
## 1. 웹개발 친화적 개발환경   
![구성요소](https://user-images.githubusercontent.com/80228504/117521049-a590c800-afe6-11eb-84f3-30940510b165.PNG)      
`html + css + javascript만 알면 데스크톱 어플리케이션을 만들수있다`     
   
## 2. 많은 성공적인 사례   
![캡처](https://user-images.githubusercontent.com/80228504/117521720-30bf8d00-afea-11eb-8816-349fe48bd382.PNG)    
더많은 사례를 확인 할수 있다   
https://www.electronjs.org/apps
   
## 3. 많은 레퍼런스    
https://github.com/sindresorhus/awesome-electron     

   
      
# 일렉트론의 장/단점   
   
## 장점    
```swift
- 크로스 플랫폼임  
윈도우, 리눅스, 맥과도 호환 -> 리눅스개발자 / 윈도우 개발자 / 맥팀 만드는건 어려움 - 걍 웹팀하나만 있음됨

- 쿨한 api 제공 
웹말고 데스크톱 앱에서 해야하는것들 ? 자동 업데이트 /네이티브 메뉴/알람 /버그리포트 , /윈도우 인스톨러...

- 노드기반임 
npm 쌉가능 자바스크립트 오픈소스 다가져와

- 웹으로 개발한 소스 
수정쪼금하면 사용가능
```

## 단점   
```swift
- 큰 용량.. 
크로미움/노드가 포함되므로헬로월드도 미니멈 100메가

- 네이티브 앱에 비해 느려!
당연히 네이티브 코드로 만든 프로그램에 비해 속도/메모리 가볍x
```
   
### 그치만.. 그러기엔 장점이 너무커서 많이들씀


open source/closed source  
boilerplates  
samples - API usage  

<br>  
일렉트론의 내부구조는 ?

# 어떻게 시작할까...?  

다 파악해야할까? -> https://pks2974.medium.com/electron-%EA%B0%84%EB%8B%A8-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-e1aa1fb3d81

### Boilerplate , start Template를 활용해보자

html + java스크립트로만 개발하면 공수가 쥰내들겠지 ?
react / view를 써보렴 -> 보일러플레이트

보일러플레이트 : 상용구 라고도 함 
위키피디아에 의하면... 최소한의 수정만을 거쳐 여러 곳에 필수적으로 사용되는 코드
ex)객체지향 프로그래밍 ->  getter ,setter 

html의 경우
```swift
<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<title>
	</title>
	</head>
	<body>
	</body>
</html>
```

Vue - https://github.com/SimulatedGREG/electron-vue  
React - https://github.com/electron-react-boilerplate/electron-react-boilerplate  
Angular - https://github.com/maximegris/angular-electron  



		
# 진짜해보자 

### 퀵스타트
3줄이면 끝!	

```swift
$ git clone https://github.com/electron/electron-quick-start 
$ cd electron-quick-start
$ npm install
$ npm start
```
	
여기서 소스좀 고쳐서 해보자~
	

<br>  

# 빌드는 어떻게 해?  
굳이 어렵게 할필요는 없자너 ?  
Third-Party Package Tool을 사용해보자 !  
   
> electron-builder  https://github.com/electron-userland/electron-builder  
electron-forge  https://github.com/electron-userland/electron-forge  
electron-packager https://github.com/electron/electron-packager  



```swift
npm install yarn -g                // yarn 사용을 위해 npm으로부터 다운로드받자
yarn add electron-builder --dev    // yarn을 통해 electron-builder를 다운로드받자 (--dev를 꼭 붙여주자 devDependency , dependency어디에 넣을것인지 정함. dev에 넣어줘야 잘동작)
```

<br>  

다음을 추가하자  

### package-json  
```swift
 "build" :{
    "appId": "your.id"
  }
```

<br>
  
```swift
yarn electron-builder
```
<br>

-> 경로에 한글 안들어가게 주의할것 그러면 좀 수정해야할게 있음!
