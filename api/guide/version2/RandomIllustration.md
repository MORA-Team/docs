---
description: Mora Api 랜덤일러스트 입니다.
slug: illustration
---

# 랜덤일러스트

### Templates

* API는 모두 GET 메서드를 사용합니다

* GET URL : https://mora-bot.kr/api/v2/iIller

### NodeJS

{% code lineNumbers="true" %}
```javascript
// node-fetch
const fetch = require('node-fetch')
fetch(`https://mora-bot.kr/api/v2/iIller`)
    .then(res => res.json())
    .then(json => {
        console.log(json)
    });

// request
const request = require('request');
let options = {
    url: `https://mora-bot.kr/api/v2/iIller`
}
request.get(options, function (error, response, body) {
    if (!error && response.status == 200) {
        let json = JSON.parse(body)
        console.log(`원래 값 : ${json}`);
    } else {
        console.log('error = ' + response.errorcode);
    }
});
```
{% endcode %}

### Python

{% code lineNumbers="true" %}
```python
import requests

response = requests.get("https://mora-bot.kr/api/v2/iIller")
result = response.json()

if response.status_code == 200:
  print(result)
else:
  print(f"Error Code: {result['status']}")
```
{% endcode %}
