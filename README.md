# redux-preloader
A Higher Order Component that helps to initialize data.


## Installation
```npm install --save redux-preloader```

## API
```preLoader(config: Object)```

### Config Properties
* `preLoader(props, nextProps, dispatch): Function`
```willMount```나 ```willReceiveProps```때 호출됩니다. 이 때 사용자는 ```props```, ```nextProps```를 통해 비동기적 액션을 생성할 수 있습니다. 때때로 비동기적 액션을 생성한 뒤 명시적으로 현재 컴포넌트를 Unmount한 뒤 LoadingComponent를 보여주고 싶을 수 있습니다. 이 때 ```preLoader```함수에서 ```true```를 반환 한다면 명시적로 현재 컴포넌트를 Loading컴포넌트로 변경할 수 있습니다. 이 외의 경우에는 ```false```를 반환하시면 됩니다.
