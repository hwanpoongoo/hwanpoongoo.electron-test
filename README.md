
# ELECTRON
![electron-logo](https://user-images.githubusercontent.com/80228504/117521003-68c4d100-afe6-11eb-96fd-393e8e975e7f.PNG)

# 목차
> 0. 서론   
> 1. ELECTRON 이란?   
> 2. 일렉트론이 인기있는 이유?   
> 3. 일렉트론의 장/단점?   
> 4. 일렉트론 간단한 실습

# 0. 서론   
kamranahmedse 양반의 개발자 로드맵을보자    
https://github.com/kamranahmedse/developer-roadmap   

`데스크톱 어플리케이션을 만들고 싶으면, 일렉트론을 배워라`
   
   
# 1. ELECTRON 이란?   
## 1-1. 정의   
> HTML, CSS, 자바스크립트를 사용해 크로스 플랫폼 데스크탑 애플리케이션을 만들기 위해 GitHub에서 개발한 오픈 소스 라이브러리   

일렉트론 활용 사례 👉 https://www.electronjs.org/   
트위치, 디스코드 슬랙 등등...   
   
## 1-2. 역사   
> Atom 에디터를 만들면서 공개한 오픈소스   

```
2013년 4월 11일, 일렉트론은 아톰 셸로 시작되었다.
2014년 5월 6일,  아톰과 아톰 셸은 MIT 라이선스와 더불어 오픈 소스로 되었다.
2015년 4월 17일, 아톰 셸은 일렉트론으로 이름이 바뀌었다.
2016년 5월 11일, 일렉트론은 버전 1.0에 도달하였다.
2016년 5월 20일, 일렉트론은 패키지된 앱을 맥 앱 스토어로 제출할 수 있게 허용하였다.
2016년 8월 2일,  일렉트론 앱의 윈도우 스토어 지원이 추가되었다.
```
   
## 1-3. 구조   
![캡처2](https://user-images.githubusercontent.com/80228504/117522077-49c93d80-afec-11eb-8fda-417fc6e81746.PNG)   
+ 크로미움 - 오픈소스 웹브라우저   - 프론트엔드 
- NODE JS - 자바스크립트 실행 런타임 환경   - 백엔드
* V8 - 자바스크립트 엔진    

```상세하게 알고싶다면?```    
 (공식문서) 👉 https://www.electronjs.org/docs/tutorial/quick-start   
 (공식문서 중요부분 요약/번역) 👉 https://velog.io/@ckstn0777/Electron-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0     
 main process <-> render process 이론 👉 https://cyberx.tistory.com/206     
 main process <-> render process 통신 예제 (IPC) 👉 https://m.blog.naver.com/sssang97/221818769601    

# 2. 일렉트론이 인기있는 이유?    
## 2-1. 웹개발자에게 좋은 접근성 
![구성요소](https://user-images.githubusercontent.com/80228504/117521049-a590c800-afe6-11eb-84f3-30940510b165.PNG)         
`html + css + javascript만 알면 데스크톱 어플리케이션을 만들수있다`       
   
## 2-2. 검증된 완성도   
![캡처](https://user-images.githubusercontent.com/80228504/117521720-30bf8d00-afea-11eb-8816-349fe48bd382.PNG)       
성공적인 활용사례가 이미 넘쳐남, 완성도 높은 프레임워크임이 입증    
https://www.electronjs.org/apps   
   
## 2-3. 많은 레퍼런스       
잘 정리된 예제 및 레퍼런스들이 활발히 공유   
https://github.com/sindresorhus/awesome-electron       

   
      
# 3. 일렉트론의 장/단점   
   
## 3-1. 장점    

### - 크로스 플랫폼     
윈도우, 리눅스, 맥 구분없이 개발 가능   
리눅스/윈도우/맥 개발자 전부 고용할것인가?  웹개발자만 있으면...   
     
### - 노드 기반이다    
npm 가능.   
무수한 패키지들의 사용가능하다   
     
### - 웹으로 개발한 소스     
수정쪼금하면 사용가능   
    
### - 편리한 ELECTRON API   
데스크톱 앱에서만 쓰이는 기능?   
->편하게 쓸수있게 제공
   
   
API doc 👉https://www.electronjs.org/   
API 관련 예제는 이 양반이 잘 정리해놓았다 👉 https://github.com/hokein/electron-sample-apps   

   
## 3-2. 단점   
```swift
- 큰 용량.. 
크로미움/노드가 포함되므로
hello world 파일 -> 미니멈 100메가, 인스톨러(nsis)도 55메가..

- 네이티브 앱에 비해 느려!
네이티브 코드로 만든 프로그램에 비해 속도/메모리 무겁다
```
   
### 단점을 상쇄할만한 장점을 가졌다


<br>  

# 4. 일렉트론 가볍게 시작하기

이론을 다 파악 후, 시작해야할까? -> https://pks2974.medium.com/electron-%EA%B0%84%EB%8B%A8-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-e1aa1fb3d81   
그보다, 가볍게 만들어보자

## 4.1 Boilerplate? , start Template?


### Boilerplate : 상용구 라고도 함    
상용구 : 최소한의 수정만을 거쳐 여러 곳에 필수적으로 사용되는 코드   

`EX.1) 객체지향 프로그래밍`
```java
class Person{
    private int age;
    private int name;
    
    private String hobby;
    private int hobby_id;
    private String school;
    private int school_id;
    private String phoneNumber;
    private int gender;
    private int pw;

    public int getAge() {
        return age;
    }

    public int getName() {
        return name;
    }

    public void setAge(int age) {
        if(age >=0){
            this.age = age;
        }
        else
            this.age = 0;
    }
}
```

`EX.2) HTML`
```html
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

보일러 플레이트라 함은...   
hello world를 뿌려주는 템플릿 ~   
보통 크로스 브라우징과 호환성을 위한 Modernizr, polyfill, Normalize 등이 적용된 템플릿 ~   

Vue - https://github.com/SimulatedGREG/electron-vue  
React - https://github.com/electron-react-boilerplate/electron-react-boilerplate  
Angular - https://github.com/maximegris/angular-electron  

		
##. 4.2 HELLO WORLD!  
### "Hello World"를 출력해보자 
3줄이면 끝!	

```
$ git clone https://github.com/electron/electron-quick-start 
$ cd electron-quick-start
$ npm install
$ npm start
```


![설치](https://user-images.githubusercontent.com/80228504/117667839-4d251a80-b1e0-11eb-86d8-2a81027b853d.PNG)    
![실행](https://user-images.githubusercontent.com/80228504/117667845-4e564780-b1e0-11eb-86e9-0dc2fedc8f80.PNG)     
	

## 파일/인스톨러 생성     
Third-Party Package Tool을 사용해보자 !  
   
> electron-builder  https://github.com/electron-userland/electron-builder  
electron-forge  https://github.com/electron-userland/electron-forge  
electron-packager https://github.com/electron/electron-packager  



```
npm install yarn -g                // yarn 사용을 위해 npm으로부터 다운로드받자
yarn add electron-builder --dev    // yarn을 통해 electron-builder를 다운로드받자 (--dev를 꼭 붙여주자 devDependency , dependency어디에 넣을것인지 정함. dev에 넣어줘야 잘동작)
```

<br>   
   
![일렉트론 빌더 설치](https://user-images.githubusercontent.com/80228504/117668078-8c536b80-b1e0-11eb-9d51-9582eba43db0.PNG)  
   
(좌)설치 전 / (우)설치 후 
자동으로 디펜던시에 추가가 된다
![일렉트론빌더 yarn으로 설치후](https://user-images.githubusercontent.com/80228504/117668088-8eb5c580-b1e0-11eb-9e3e-6a7f523cc671.PNG)    


   


### package-json  : 빌드옵션을 기입해주자
```swift
 "build" :{
    "appId": "your.id"
  }
```

빌드 옵션 기입
(좌)수정 전 / (우)수정 후   
![빌드 키값을 추가해주자](https://user-images.githubusercontent.com/80228504/117668675-22879180-b1e1-11eb-964e-454c831d67c6.PNG)    

지금은 default 빌드 옵션을 사용하였다   
상세 옵션 정보는 다음을 참고하자 👉 https://www.electron.build/configuration/configuration  



<br>
  
```
yarn electron-builder
```
<br>


![패키징](https://user-images.githubusercontent.com/80228504/117668215-b0af4800-b1e0-11eb-8558-aa9b6de4ba1b.PNG)    
![일렉트론빌더 패키징](https://user-images.githubusercontent.com/80228504/117668124-95443d00-b1e0-11eb-9d71-2d444653955c.PNG)    



###  참고)경로에 한글이 들어갈경우, 패키징이 잘안됨
![경로에 한글이 들어갈경우](https://user-images.githubusercontent.com/80228504/117668135-98d7c400-b1e0-11eb-90d4-f357deb54a6e.PNG)
   
해결 방법 👉 https://steady-snail.tistory.com/241   
앵간하면 그냥 경로에 한글이 안들어가게 하자...   


### 최종 
![패키징 완료후 디렉터리구조](https://user-images.githubusercontent.com/80228504/117668246-b86eec80-b1e0-11eb-87a2-a3560daefee8.PNG)

dist 폴더가 생성되고, 해당 폴더안에 인스톨러 / exe파일이 생성된다






