# 👾 Crypt

### Base64 Decode

{% code lineNumbers="true" %}
```typescript
<string> base64_decode(<string> data)  
```
{% endcode %}

* Decodes `data` with base64.

> Alternative: `base64decode`

***

### Base64 Encode

{% code lineNumbers="true" %}
```typescript
<string> base64_encode(<string> data)  
```
{% endcode %}

* Encodes `data` with base64.

> Alternative: `base64encode`

***

### Decrypt

{% code lineNumbers="true" %}
```typescript
<string> crypt.decrypt(<string> data, <string> key)  
```
{% endcode %}

* Decrypts `data` with `key`.

***

### Derive

{% code lineNumbers="true" %}
```typescript
<string> crypt.derive(<string> value, <uint> length)
```
{% endcode %}

* Derives a secret key from `value` with the length of `length`.

***

### Encrypt

{% code lineNumbers="true" %}
```typescript
<string> crypt.encrypt(<string> data, <string> key)  
```
{% endcode %}

* Encrypts `data` with `key`.

***

### Generate Bytes

```typescript
<string> crypt.generatebytes(<string> value)
```

* Generates random bytes based off `value`.

***

### Generate Key

```typescript
<string> crypt.generatekey(<string> value)
```

* Generates a random key based off `value`.

***

### Hash

{% code lineNumbers="true" %}
```typescript
<string> crypt.hash(<string> data)
```
{% endcode %}

* Hashes `data` with SHA-384.

***

### LZ4 Compress <a href="#lz4-compress" id="lz4-compress"></a>

```typescript
<string> lz4_compress(<string> data)
```

* Compresses `data` using lz4.

***

### LZ4 Decompress <a href="#lz4-decompress" id="lz4-decompress"></a>

```typescript
<string> lz4_decompress(<string> data)
```

* Decompresses `data` using lz4.

***

### Random

{% code lineNumbers="true" %}
```typescript
<string> crypt.random(<uint> size)
```
{% endcode %}

* Generates a random string with `size` (cannot be negative or exceed 1024).

***
