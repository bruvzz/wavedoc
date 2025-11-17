---
description: These are all of the functions revolving hooking that Wave supports.
---

# 🪝 Hooking

### Clone Function <a href="#clone-function" id="clone-function"></a>

{% code lineNumbers="true" %}
```typescript
<function> clonefunction(<function> a1)
```
{% endcode %}

* Clones function `a1`.

> Alternative: `clonefunc`

***

### Get Callback Value

{% code lineNumbers="true" %}
```typescript
<any> getcallbackvalue(<function fn>)
```
{% endcode %}

* Retrieves the current value or reference of `fn` that has been set or hooked.

***

### Hook Function

{% code lineNumbers="true" %}
```typescript
<function> hookfunction(<function> old, <function> new)  
```
{% endcode %}

* Hooks function `old`, replacing it with the function `new`. The `old` function is returned, you _must_ use this function in order to call the original function.

> Alternative: `replaceclosure`, `hookfunc`, `replacefunction`, `replacefunc`, `detourfunction`, `replaceclosure`, `detour_function`

***

### Hook Metamethod

{% code lineNumbers="true" %}
```typescript
<function> hookmetamethod(<Object> object, <string> metamethod, <function> a1)  
```
{% endcode %}

* Hooks the `metamethod` passed in `object`'s metatable with `a1`.

***

### Is Hooked

{% code lineNumbers="true" %}
```typescript
<bool> ishooked(<function fn>)
```
{% endcode %}

* Checks if `fn` has been hooked (i.e., replaced or wrapped by a hook).

> Alternative: `isfunctionhooked`

***

### Is Our Call Stack

{% code lineNumbers="true" %}
```typescript
<bool> isourcallstack(<int level>)
```
{% endcode %}

* Checks the entire callstack to see if it is from Wave or Roblox.

***

### New C Closure

{% code lineNumbers="true" %}
```typescript
<function> newcclosure(<function> a1)  
```
{% endcode %}

* Pushes a new C Closure that invokes the function `a1` upon call.

***

### New Lua Closure

{% code lineNumbers="true" %}
```typescript
<function> newlclosure(<function fn>)
```
{% endcode %}

* Pushes a new L Closure that invokes the function `fn` upon call.

***

### Protect Closure

{% code lineNumbers="true" %}
```typescript
<void> protectclosure(<function fn>)
```
{% endcode %}

* Prevents `fn` from being hooked or modified by external code.

> Alternative: `protectfunction`

***

### Restore Closure

{% code lineNumbers="true" %}
```typescript
<void> restoreclosure(<function fn>)
```
{% endcode %}

* Restores `fn` back to its original, unmodified closure.

> Alternative: `restorefunction`, `restorefunc`
