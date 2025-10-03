---
description: These are all of the functions revolving around signals that Wave supports.
---

# 📶 Signal

### Can Signal Replicate

{% code lineNumbers="true" %}
```typescript
<bool> cansignalreplicate(<RBXScriptSignal signal>)
```
{% endcode %}

* Checks if `RBXScriptSignal` is capable of being replicated (i.e., fired to the server or across the client-server boundary).

***

### Disable Connection

{% code lineNumbers="true" %}
```typescript
<void> disableconnection(<RBXScriptConnection> Connection)
```
{% endcode %}

* Disables `Connection`.

***

### Enable Connection

{% code lineNumbers="true" %}
```typescript
<void> enableconnection(<RBXScriptConnection> Connection)
```
{% endcode %}

* Enables `Connection`.

***

### Fire Signal

{% code lineNumbers="true" %}
```typescript
<void> firesignal(<RBXScriptSignal> Signal, <variant?> Args...)
```
{% endcode %}

* Fires all signals connected to the `signal`. If given, the arguments will be used to call the function.

***

### Get All Replicate Signals

{% code lineNumbers="true" %}
```typescript
<table> getallreplicatesignals(<void>)
```
{% endcode %}

* Returns a table containing all `RBXScriptSignal` objects in the game that are capable of replication.

***

### Get Connections

{% code lineNumbers="true" %}
```typescript
<table> getconnections(<RBXScriptSignal> Signal)
```
{% endcode %}

* Returns a `table` with all connections to the given `signal`.

#### Connections:

| Connection |                Description                |
| :--------: | :---------------------------------------: |
|  .Function | The function connected to the connection. |
|   :Enable  |          Enables the connection.          |
|  :Disable  |          Disables the connection.         |
|    :Fire   |           Fires the connection.           |

***

### Get Signal Arguments

{% code lineNumbers="true" %}
```typescript
<table> getsignalarguments(<RBXScriptConnection conn>)
```
{% endcode %}

* Retrieves the arguments passed to a specific `RBXScriptConnection` when it was last fired.

***

### Hook Signal

{% code lineNumbers="true" %}
```typescript
<void> hooksignal(<RBXScriptSignal> Signal, <function> callback)
```
{% endcode %}

* Intercepts signal invocations. When the `Signal` is fired, the `callback` is called for each Lua connection with an info table and arguments. Returning <mark style="color:green;">`true`</mark> from the callback triggers the original connection.&#x20;

> Note: `hooksignal` cannot intercept C connections or CoreScript Lua connections.

***

### Is Connection Enabled

{% code lineNumbers="true" %}
```typescript
<bool> isconnectionenabled(<RBXScriptConnection> Connection)
```
{% endcode %}

* Returns <mark style="color:green;">`true`</mark> if a connection is enabled.

***

### Is Signal Hooked

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>&#x3C;void> issignalhooked(&#x3C;RBXScriptSignal> Signal)
</strong></code></pre>

* Returns <mark style="color:green;">`true`</mark> if `Signal` is hooked.

***

### Replicate Signal

{% code lineNumbers="true" %}
```typescript
<void> replicatesignal(<RBXScriptSignal signal>, <var ...args>)
```
{% endcode %}

* Fires a `RBXScriptSignal` locally, simulating its activation with the provided arguments.

***

### Unhook Signal

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>&#x3C;void> unhooksignal(&#x3C;RBXScriptSignal> Signal)
</strong></code></pre>

* Unhooks a signal hooked with `hooksignal`.

***
