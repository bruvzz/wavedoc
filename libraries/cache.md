# 🗃️ Cache

### Clone Reference

{% code lineNumbers="true" %}
```typescript
<Instance> cloneref(<Instance.X>)
```
{% endcode %}

* Pushes `Instance.X` in a new cache.

***

### Compare Instances

{% code lineNumbers="true" %}
```typescript
<bool> compareinstances(<Instance.X>, <Instance.Y>)
```
{% endcode %}

* Compares instances internally.

***

### Invalidate

{% code lineNumbers="true" %}
```typescript
<void> cache.invalidate(<Instance>)
```
{% endcode %}

* Invalidates `Instance` in the cache within registry.

***

### Is Cached

{% code lineNumbers="true" %}
```typescript
<bool> cache.iscached(<Instance>)
```
{% endcode %}

* Returns if `Instance` is currently cached in the cache within registry.

***

### Replace

{% code lineNumbers="true" %}
```typescript
<void> cache.replace(<Instance.X>, <Instance.Y>)
```
{% endcode %}

* Replaces `Instance.X` with `Instance.Y` in the cache within registry.

***
