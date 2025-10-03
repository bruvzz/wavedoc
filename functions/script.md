---
description: These are all of the functions revolving scripts that Wave supports.
---

# 🕹️ Script

### Filter Garbage Collection

{% code lineNumbers="true" %}
```typescript
<table> filtergc(<any search, bool includeTables>)
```
{% endcode %}

* Searches the garbage collector for objects matching `search`.

> Alternative: `filter_gc`

***

### Get Calling Script

{% code lineNumbers="true" %}
```typescript
<Instance> getcallingscript(<void>)
```
{% endcode %}

* Gets the script that is calling this function.

> Alternative: `get_calling_script`, `getscriptcaller`, `getcaller`

***

### Get Garbage Collection <a href="#get-loaded-modules" id="get-loaded-modules"></a>

{% code lineNumbers="true" %}
```typescript
<table> getgc(<bool includeTables>)
```
{% endcode %}

* Returns all objects currently tracked by the garbage collector.

> Alternative: `get_gc_objects`

***

### Get Function Hash

{% code lineNumbers="true" %}
```typescript
<string> getfunctionhash(<function fn>)
```
{% endcode %}

* Returns a hash from `fn`.

***

### Get Global Environment

{% code lineNumbers="true" %}
```typescript
<table> getgenv(<void>)
```
{% endcode %}

* Returns the `environment` that will be applied to each script ran by Wave.

***

### Get Loaded Modules <a href="#get-loaded-modules" id="get-loaded-modules"></a>

```typescript
<table> getloadedmodules(<void>)
```

* Returns a `table` with all loaded `modules` currently in game.

> Alternative: `get_loaded_modules`

***

### Get Modules

{% code lineNumbers="true" %}
```typescript
<table> getmodules(<Instance parent>)
```
{% endcode %}

* Returns all ModuleScripts that are children of `parent`.

> Alternative: `get_modules`

***

### Get Roblox Environment

{% code lineNumbers="true" %}
```typescript
<table> getrenv(<void>)
```
{% endcode %}

* Returns the Roblox environment.

***

### Get Roblox Environment Global

{% code lineNumbers="true" %}
```typescript
<any> getrenvglobal(<string name>)
```
{% endcode %}

* Returns the value of a global variable in the Roblox environment (`renv`).

***

### Get Roblox Environment Shared

{% code lineNumbers="true" %}
```typescript
<any> getrenvshared(<string name>)
```
{% endcode %}

* Returns the value of a shared variable in the Roblox environment (`renv`).

***

### Get Running Scripts <a href="#get-running-scripts" id="get-running-scripts"></a>

```typescript
<table> getrunningscripts(<void>)
```

* Returns a list of scripts that are running in the environment. Returns `nil` if there are no scripts running.

***

### Get Scripts <a href="#get-scripts" id="get-scripts"></a>

```typescript
<table> getscripts(<void>)
```

* Returns a list of scripts within the global state of the caller.

> Alternative: `get_scripts`

***

### Get Script Bytecode

{% code lineNumbers="true" %}
```typescript
<string> getscriptbytecode(<Instance> Script)
```
{% endcode %}

* Returns the bytecode of the given script. This can be used in a dissassembler.

> Alternative: `dumpstring`

***

### Get Script Closure

{% code lineNumbers="true" %}
```typescript
<function> getscriptclosure(<Instance> Script)
```
{% endcode %}

* Returns the closure from the given script, can be used to gather `upvalues` or `constants`.

> Alternative: `getscriptfunction`, `get_script_function`

***

### Get Script Environment

{% code lineNumbers="true" %}
```typescript
<table> getsenv(<LocalScript, ModuleScript> Script)
```
{% endcode %}

* Returns the global environment of the given script.

> Alternative: `getmenv`

***

### Get Script Hash

{% code lineNumbers="true" %}
```typescript
<string> getscripthash(<Instance> Script)
```
{% endcode %}

* Returns a SHA384 hash of the scripts bytecode. You can use this to detect changes of a script.

***

### Get Table Environment

{% code lineNumbers="true" %}
```typescript
<table> gettenv(<void>)
```
{% endcode %}

* Returns the environment table of the current script.

> Alternative: `getstateenv`

***

### Get Thread Script

{% code lineNumbers="true" %}
```typescript
<Instance> getthreadscript(<thread thrd>)
```
{% endcode %}

* Returns the `LocalScript` or `ModuleScript` instance that the given thread originated from.

***

### Is Local Source Container

{% code lineNumbers="true" %}
```typescript
<bool> islocalsourcecontainer(<Instance obj>)
```
{% endcode %}

* Checks if `obj` is a local source container (like a LocalScript).

***

### Require

{% code lineNumbers="true" %}
```typescript
<any> require(<Instance ModuleScript>)
```
{% endcode %}

* Loads and returns the value of `ModuleScript`.

***

### Set Closure Identity

{% code lineNumbers="true" %}
```typescript
<void> setclosureidentity(<function fn>, <int identity>)
```
{% endcode %}

* Sets the security identity of a function closure.

> Alternative: `setclosurecaps`

***
