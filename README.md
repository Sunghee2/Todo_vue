# Todo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```
> 빌드를 하게 되면 `dist`폴더가 생기게 되는데 이 폴더를 나중에 배포하게 됨

`public/` : 정적 파일
`asset/` : css, 이미지들
`components/` : 모든 페이지에서 사용하는 공통적인 컴포넌트
`views` : 각 화면의 컴포넌트


- @Watch()

  괄호 내의 변수가 변경될 때마다 해당 함수 실행
  
- @Provide / @inject
  
  Prop은 직계 부모, 자식 간에만 데이터 전달 가능
  하지만 이 provide, inject는 위의 단점을 커버할 수 있지만 이 변수가 어디서 쓰이는지 직관적으로 확인하기 어려워서 잘 사용하지 않음.
