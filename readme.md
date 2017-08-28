# axios的jsonp适配器

## 支持promise，支持cancel，用法与xhr一致

## 安装

```script
npm install axios-jsonp
```

## 用法

```script
let axios = require('axios');
let jsonpAdapter = require('axios-jsonp');

axios({
    url: '/jsonp',
    adapter: jsonpAdapter
}).then((res) => {

});
```