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

pub_jwk={'k': key.publickey().exportKey('PEM')}

jwe = jose.encrypt(claims, pub_jwk)
# JWE(header='xxx',
# cek='xxx',
# iv='xxx',
#ciphertext='xxx',
#tag='xxx')

jwt = jose.serialize_compact(jwe)
priv_jwk = {'k': key.exportKey('PEM')}
jwt = jose.decrypt(jose.deserialize_compact(jwt), priv_jwk)
# JWT(header={u'alg': u'RSA-OAEP', u'enc': u'xxx'},
#claims={u'iss': u'http://www.example.com', u'sub': 42, u'exp': 0000})

jwk = {'k': 'password'}
jws = jose.sign(claims, jwk, alg='HS256')
jwt = jose.serialize_compact(jws)
jose.verify(jose.deserialize_compact(jwt), jwk, 'HS256')

```

```
```

```
```


