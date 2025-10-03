---
description: >-
  These are all of the functions revolving the Roblox environment that Wave
  supports.
---

# 🌎 Environment

### Add Spy Callback

{% code lineNumbers="true" %}
```typescript
<void> addspycallback(<function callback>)
```
{% endcode %}

* Registers a `callback` that will be executed whenever a RemoteEvent or function is invoked, allowing you to inspect or log the call.

***

### Create Secure Folder

```typescript
<void> createsecurefolder(<string> path)
```

* Creates a new secure folder to `path`.

> Note: The folder itself won't be able to be found by the game. This means you don't need to set the security of the instances within it.

> Alternative:  `create_secure_folder`

### Fire Click Detector

{% code lineNumbers="true" %}
```typescript
<void> fireclickdetector(<ClickDetector> ClickDetector, <number?> Distance = 0, <string?>)
```
{% endcode %}

* Fires the `ClickDetector`. If no distance supplied, it will default to `0`.

***

### Fire Proximity Prompt

{% code lineNumbers="true" %}
```typescript
<void> fireproximityprompt(<ProximityPrompt> Prompt)
```
{% endcode %}

* Fires the `ProximityPrompt` trigger.

***

### Fire Touch Interest

{% code lineNumbers="true" %}
```typescript
<void> firetouchinterest(<BasePart> totouch, <BasePart> Part, <uint?> toggle)
```
{% endcode %}

* Touches part with `totouch`.

#### Actions:

|       Action      | Toggle |
| :---------------: | :----: |
| Begins the touch. |    0   |
|  Ends the touch.  |    1   |

***

### Get Instances

{% code lineNumbers="true" %}
```typescript
<table> getinstances(<void>)
```
{% endcode %}

* Returns a `table` with instances.

> Alternative: `get_instances`

***

### Get Nil Instances

{% code lineNumbers="true" %}
```typescript
<table> getnilinstances(<void>)
```
{% endcode %}

* Returns a `table` with instances parented to `nil`.

> Alternative: `get_nil_instances`

***

### Is Secured Instance

```typescript
<void> issecuredinstance(<Instance> Instance)
```

* Returns <mark style="color:green;">`true`</mark>/<mark style="color:red;">`false`</mark> if `Instance` is secured/not secured.

> Alternative: `is_secured_instance`

***

### Protect Instance

{% code lineNumbers="true" %}
```typescript
<void> protectinstance(<Instance obj>)
```
{% endcode %}

* Marks `obj` as protected, preventing it from being tampered with or detected by certain internal checks.

***

### Set Normal Instance

```typescript
<table> setnormalinstance(<Instance> Instance)
```

* Sets `Instance` back to its normal state. Returns <mark style="color:red;">`false`</mark> if `Instance` is back to normal.

> Alternative: `set_normal_instance`

***

### Set Simulation Radius

{% code lineNumbers="true" %}
```typescript
<void> setsimulationradius(<number radius>)
```
{% endcode %}

* Sets the simulation `radius` for the local player, controlling how far physics and character updates are processed around the player.

***

### Set Secure Instance

```typescript
<table> setsecureinstance(<Instance> Instance)
```

* Secures `Instance`. Returns <mark style="color:red;">`false`</mark> if `Instance` is secured.

> Alternative: `set_secure_instance`
