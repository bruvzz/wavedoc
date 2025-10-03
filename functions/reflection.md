---
description: These are all of the functions revolving reflections that Wave supports.
---

# 🪞 Reflection

### Check Caller

{% code lineNumbers="true" %}
```typescript
<bool> checkcaller(<void>)  
```
{% endcode %}

* Returns `true` if the current thread was created by Wave.

***

### Get Hidden Property

{% code lineNumbers="true" %}
```typescript
<variant> gethiddenproperty(<Instance> Object, <string> Property)
```
{% endcode %}

* Returns the `value` of the property that cannot be accessed through Lua.

***

### Is Executor Closure <a href="#is-executor-closure" id="is-executor-closure"></a>

```typescript
<bool> isexecutorclosure(<function> a1)
```

* Returns `true` if `a1` was created by Wave.

> Alternative: `isourclosure`, `is_our_closure`, `is_executor_closure`, `checkclosure`

***

### Is C Closure

{% code lineNumbers="true" %}
```typescript
<bool> iscclosure(<function fn>)
```
{% endcode %}

* Returns true if `fn` is a C closure (a function implemented in C, not Lua).

> Alternative: `is_c_closure`

***

### Is Line Info

{% code lineNumbers="true" %}
```typescript
<bool> islineinfo(<function fn>)
```
{% endcode %}

* Checks if `fn` contains Lua line information (debug metadata such as source file and line numbers).

***

### Is Lua Closure

{% code lineNumbers="true" %}
```typescript
<bool> islclosure(<function> a1)
```
{% endcode %}

* Returns `true` if `a1` is an L closure.

> Alternative: `is_l_closure`

***

### Loadstring

{% code lineNumbers="true" %}
```typescript
<function> loadstring(<string> chunk, <string?> chunkName)
```
{% endcode %}

* Loads `chunk` as a Lua function with optional `chunkName` and returns it.

***

### Set Hidden Property

{% code lineNumbers="true" %}
```typescript
<void> sethiddenproperty(<Instance> Object, <string> Property, <variant> Value)
```
{% endcode %}

* Sets the given property to new `value`.

***

### Set Scriptable

{% code lineNumbers="true" %}
```typescript
<void> setscriptable(<Instance> Object, <string> Property, <bool> toggle)
```
{% endcode %}

* Sets the property's scriptable state to `toggle`.

***
