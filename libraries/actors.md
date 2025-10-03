# 👨‍🎤 Actors

{% hint style="info" %}
Actors Library is Premium only!
{% endhint %}

### Create Communication Channel

{% code lineNumbers="true" %}
```typescript
<any> create_comm_channel(<string channelName>)
```
{% endcode %}

* Creates a communication channel for sending and receiving messages.

***

### Get Actors

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>&#x3C;string> getactors(&#x3C;void>)
</strong></code></pre>

* Returns all the actors in the game, example above will return `0` if there are no actors in the game.

> Alternative: `get_actors`

***

### Get Actor From Thread

{% code lineNumbers="true" %}
```typescript
<any> get_actor_from_thread(<thread thrd>)
```
{% endcode %}

* Returns the actor (script or environment) associated with `thrd`.

> Alternative: `getactorfromthread`, `getthreadactor`, `get_thread_actor`

***

### Get Communication Channel

{% code lineNumbers="true" %}
```typescript
<any> get_comm_channel(<string channelName>)
```
{% endcode %}

* Retrieves an existing communication channel by `channelName`.

***

### Get Current Actor

```typescript
<string> get_current_actor(<void>)
```

* Returns the actor instance of the current running thread.

> Alternative: `getcurrentactor`

***

### Get Deleted Actors

```typescript
<string> getdeletedactors(<void>)
```

* Checks actor threads specifically connected to an expired actor instance.&#x20;

> Note: This function does not return the actor instance directly. Instead, it returns a lightuserdata that can be passed to `run_on_actor`.

> Alternative: `get_deleted_actors`

***

### Is Parallel

{% code lineNumbers="true" %}
```typescript
<string> is_parallel(<void>)
```
{% endcode %}

* Returns if the thread is parallel or not.

***

### Run On Actor

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>&#x3C;string> run_on_actor(&#x3C;ActorState>, &#x3C;Script>)
</strong></code></pre>

* Will run the script on an actor state.

{% code lineNumbers="true" %}
```lua
local id, channel = create_comm_channel()
channel.Event:Connect(print) -- .Event returns channel, so we are connecting directly to channel

run_on_actor(Instance.new("Actor"), [[
local s = get_comm_channel(...)
s:Fire("hello from actor")
]], id)
```
{% endcode %}

***
