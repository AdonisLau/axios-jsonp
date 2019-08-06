# A jsonp adapter for axios

## support promise，support cancel，same as xhr

## install

```script
npm install axios-jsonp
```

## usage

```script
let axios = require('axios');
let jsonpAdapter = require('axios-jsonp');

const instance = axios.create()

instance.interceptors.request.use(config => ({
  ...config,
  callbackParamName: 'c' // optional, 'callback' by default
}), err => Promise.reject(err))

instance.get({
    url: '/jsonp',
    adapter: jsonpAdapter,
}).then((res) => {

});
```
