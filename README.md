### jose
---
https://jose.readthedocs.io/en/latest/

https://github.com/demonware/jose

```py
import jose

claims = {
  'iss': 'http://www.example.com',
  'exp': int(time()) + 3600,
  'sub': 42
}

jwk = {'k': 'password'}

jws = jose.sign(claims, jwk, alg='HS256')
#
jwt = jose.serialize_compact(jws)
#
jose.verify(jose.deserialize_compact(jwt), jwk, 'HS256')

```

```
```

```
```


