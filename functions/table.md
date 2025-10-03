---
description: These are all of the functions revolving tables that Wave supports.
---

# 📊 Table

### Get Raw Metatable

{% code lineNumbers="true" %}
```typescript
<table> getrawmetatable(<table> a1)  
```
{% endcode %}

* Returns the `__metatable` of `a1`.

***

### Is Read Only

{% code lineNumbers="true" %}
```typescript
<bool> isreadonly(<table> a1)  
```
{% endcode %}

* Returns if `a1` is read-only.

***

### Is Writable

{% code lineNumbers="true" %}
```typescript
<bool> iswritable(<table tbl>)
```
{% endcode %}

* Checks if `tbl` is writable, i.e., if its fields can be modified.

> Alternative: `iswriteable`

***

### Make Read Only

{% code lineNumbers="true" %}
```typescript
<void> makereadonly(<table tbl>)
```
{% endcode %}

* Makes `tbl` read-only, preventing modifications to its fields.

> Alternative: `make_readonly`

***

### Make Writable

{% code lineNumbers="true" %}
```typescript
<void> makewritable(<table tbl>)
```
{% endcode %}

* Makes `tbl` writable, allowing its fields to be modified.

> Alternative: `make_writable`, `make_writeable`, `makewriteable`

***

### Set Raw Metatable

{% code lineNumbers="true" %}
```typescript
<bool> setrawmetatable(<table> a1, <table> a2)
```
{% endcode %}

* Sets the `__metatable` of `a1` to `a2`.

***

### Set Read Only

{% code lineNumbers="true" %}
```typescript
<void> setreadonly(<table> a1, <bool> a2)  
```
{% endcode %}

* Sets the read-only value of `a1` to `a2`.

***
