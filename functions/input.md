---
description: These are all of the functions revolving inputs that Wave supports.
---

# 🖱️ Input

### Is Roblox Active

{% code lineNumbers="true" %}
```typescript
<bool> isrbxactive(<void>)
```
{% endcode %}

* Returns `true` if the game window is in focus.

***

### Keyboard

{% code lineNumbers="true" %}
```typescript
<void> keydown(<uint> keycode)  
```
{% endcode %}

* Simulates a key press for the specified keycode. You can find a list of codes [here](https://docs.microsoft.com/en-us/windows/desktop/inputdev/virtual-key-codes).

> Alternative: `keypress`

{% code lineNumbers="true" %}
```typescript
<void> keytap(<int keycode>)
```
{% endcode %}

* Simulates a single press and release of the specified keycode.

{% code lineNumbers="true" %}
```typescript
<void> keyup(<uint> key)  
```
{% endcode %}

* Releases `key` on the keyboard.

> Alternative: `keyrelease`

***

### Left Click

{% code lineNumbers="true" %}
```typescript
<void> mouse1click(<void>)  
```
{% endcode %}

* Simulates a full left mouse button press.

{% code lineNumbers="true" %}
```typescript
<void> mouse1press(<void>)  
```
{% endcode %}

* Simulates a left mouse button press without releasing it.

{% code lineNumbers="true" %}
```typescript
<void> mouse1release(<void>)  
```
{% endcode %}

* Simulates a left mouse button release.

***

### Mouse Movement

{% code lineNumbers="true" %}
```typescript
<void> mousescroll(<number> number)  
```
{% endcode %}

* Scrolls the mouse wheel virtually by `number` pixels.

{% code lineNumbers="true" %}
```typescript
<void> mousemoverel(<number> a1, <number> a2)  
```
{% endcode %}

* Moves the mouse cursor relatively to the current mouse position by coordinates `a1` and `a2`.

{% code lineNumbers="true" %}
```typescript
<void> mousemoveabs(<number> a1, <number> a2)  
```
{% endcode %}

* Move's your mouse to the `a1` and `a2` coordinates in pixels from top left of the window.

***

### Right Click

{% code lineNumbers="true" %}
```typescript
<void> mouse2click(<void>)
```
{% endcode %}

* Simulates a full right mouse button press.

{% code lineNumbers="true" %}
```typescript
<void> mouse2press(<void>)  
```
{% endcode %}

* Clicks down on the right mouse button.

{% code lineNumbers="true" %}
```typescript
<void> mouse2release(<void>)  
```
{% endcode %}

* Simulates a right mouse button release.

***
