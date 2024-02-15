

## ❗ 동적 라우팅을 왜 사용하는가..??

<br/><br/>
>예를 들어 우리가 쇼핑몰을 만드는 중이다. 그리고 수백개가 넘는 제품이 있다고 가정했을때 수백개 별로 페이지를 만드는건 아주 힘든 방법이다. 제품의 경로를 입력해도 동일한 제품 페이지를 이용하면서 경로에 해당하는 제품의 데이터를 보여주는 식으로 진행해야한다

<br/><br/>

## ☝️경로 세팅

```
/app
	ㄴ-- contents
	  ㄴ-- [slug]
      	 ㄴ-- page.tsx
      ㄴ-- page.tsx
/public
```


대괄호를 사용하여 키워드를 넣는다. (ex. slug) 해당 페이지는 동적으로 경로가 지정되는 페이지가 된다.
<br/>
<br/>

```javascript
// [slug]/page.tsx

type Props = {
	parmas:{
		slug: string;
	};
};

export default function 페이지이름({params}:Props){
	return(
  	
  	<h1>{parmas.slug}페이지페이지</h1>
    
    )

}

```
컴포넌트로 props을 전달하는 방식으로 어떤 경로에 들어왔는지 확인

<br/><br/>

## ❗정적 라우팅
<br/><br/>
### ✔ 정적 라우팅 (버전 12)

❗Next.JS에서는 pages 폴더 안에 컴포넌트를 생성하면 자동으로 경로가 설정되게 됨 
```
/pages
  ㄴ-- index.tsx
  ㄴ-- hyeonTae.tsx
/public
/styles
```

👌 pages 안에 index.jsx와 hyeonTae.jsx가 있으면 별도로 라우팅 없이 /hyeonTae 경로 사용 가능


### ✔ 정적 라우팅 (버전 13)
```
/app
	ㄴ-- contents
	  ㄴ-- page.tsx
	ㄴ-- global.css
	ㄴ-- layout.tsx
	ㄴ-- page.tsx
/public

```
👌 app 폴더 안에 추가하고자 하는 페이지 폴더를 추가 후 page.tsx를 생성하여 사용
<br/>

>페이지 안에 부모 라우팅 내부에 재사용한 컴포넌트를 제공하고,로딩이나 에러 등 복잡한 처리를 해당 라우터 안에서 처리해주기 위해 13버전 부터 바뀜

<br/><br/>


![](https://velog.velcdn.com/images/htkim97/post/f3dc0dfc-fe68-48dc-aa9c-b3a69c644336/image.png)
![](https://velog.velcdn.com/images/htkim97/post/4f8622ae-896d-4868-ba52-925b61fa7464/image.png)
![](https://velog.velcdn.com/images/htkim97/post/3f8e729a-6994-4929-beea-c44d98944fe8/image.png)


<br/><br/>


