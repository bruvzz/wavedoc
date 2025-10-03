# 🐞 Debug

### Get Constant

{% code lineNumbers="true" %}
```typescript
<variant> debug.getconstant(<function> f, <int> idx)
```
{% endcode %}

* Returns the constant at index `idx` in function `f` or level `f`.

***

### Get Constants

{% code lineNumbers="true" %}
```typescript
<table> debug.getconstants(<function> f)
```
{% endcode %}

* Returns the constants in function `f` or at level `f`.

***

### Get Info

{% code lineNumbers="true" %}
```typescript
<table> debug.getinfo(<function> f)
```
{% endcode %}

* Returns a table of information about function `f`.

#### Info:

|     Name    |   Type   |                        Description                        |
| :---------: | :------: | :-------------------------------------------------------: |
|     name    |  String  |                 The name of the function.                 |
|  short\_src |  String  |                A shorter version of source.               |
|     what    |  String  | What the function is: Lua = Lua function - C = C function |
| currentline |  Integer |             The line that is currently active.            |
|     nups    |  Integer |       The number of upvalues that the function has.       |
|     func    | Function |                The function that is active.               |
|    source   |  String  |              Where the function was defined.              |

***

### Get Proto

{% code lineNumbers="true" %}
```typescript
<table, function> debug.getproto(<function> f, <int> idx, <bool?> activated)
```
{% endcode %}

* Gets the inner `function` of `f` at `index`.

***

### Get Protos

{% code lineNumbers="true" %}
```typescript
<table> debug.getprotos(<function fn>)
```
{% endcode %}

* Retrieves all prototype functions used inside `fn`.

***

### Get Registry

{% code lineNumbers="true" %}
```typescript
<table> debug.getregistry(<void>)
```
{% endcode %}

* Returns the Lua registry.

***

### Get Stack

{% code lineNumbers="true" %}
```typescript
<table> debug.getstack(<function> f, <int> idx)
```
{% endcode %}

* Gets the method stack at level or function `f`.

***

### Get Upvalue

{% code lineNumbers="true" %}
```typescript
<variant> debug.getupvalue(union<function, number> f, <number> idx)
```
{% endcode %}

* Returns the upvalue with name `idx` in function or level `f`.

***

### Get Upvalues

{% code lineNumbers="true" %}
```typescript
<table> debug.getupvalues(<function> f)
```
{% endcode %}

* Retrieve the upvalues in function `f` or at level `f`.

***

### Set Constant

{% code lineNumbers="true" %}
```typescript
<void> debug.setconstant(<function> f, <int> idx, union<number, bool, string> value)
```
{% endcode %}

* Set constant `idx` to tuple `value` at level or function `f`.

***

### Set Metatable

{% code lineNumbers="true" %}
```typescript
<table> debug.setmetatable(<table> o, <table> mt)  
```
{% endcode %}

* Set the metatable of `o` to `mt`.

***

### Set Proto

{% code lineNumbers="true" %}
```typescript
<void> debug.setproto(<function> fi, <number> index, <function> replacement)
```
{% endcode %}

* Replaces `fi` at `index` with function `replacement` at level or function `fi`.

***

### Set Stack

{% code lineNumbers="true" %}
```typescript
<void> debug.setstack(<function> f, <int> idx, <table> value)
```
{% endcode %}

* Sets the stack indice at `indice` to `value` at level or function `f`.

***

### Set Upvalue

{% code lineNumbers="true" %}
```typescript
<void> debug.setupvalue(<function> f, <int> idx, <table> value)
```
{% endcode %}

* Set upvalue `idx` to `value` at level or function `f`.

***

### Valid Level

{% code lineNumbers="true" %}
```typescript
<bool> validlevel(<function fn>, <int level>)
```
{% endcode %}

* Checks if `fn` can run at `level`.

> Alternative: `isvalidlevel`

***
