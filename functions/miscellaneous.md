---
description: These are uncategorized/miscellaneous functions Wave supports.
---

# 💡 Miscellaneous

### Clear Teleport Queue

{% code lineNumbers="true" %}
```typescript
<void> clearteleportqueue(<void>)
```
{% endcode %}

* Clears all queued teleport requests for the local player.

> Alternative: `clear_teleport_queue`

***

### Decompile

{% code lineNumbers="true" %}
```typescript
<string> decompile(<Instance> Script)
```
{% endcode %}

* Decompiles `Script` and returns the decompiled output.

{% hint style="info" %}
WARNING: `decompile()` is a Premium only function.
{% endhint %}

#### Example:

{% code lineNumbers="true" %}
```lua
local LocalPlayer = game:GetService("Players").LocalPlayer 
local PlayerModule = LocalPlayer.PlayerScripts.PlayerModule
local Decompiled = decompile(PlayerModule) -- Decompiles PlayerModule
setclipboard(Decompiled) -- Copies the decompiled output to your clipboard
```
{% endcode %}

***

### Get Clipboard <a href="#get-hidden-ui" id="get-hidden-ui"></a>

{% code lineNumbers="true" %}
```typescript
<void> getclipboard(<void>)
```
{% endcode %}

* Gets the content from your clipboard.

> Alternative: `fromclipboard`

***

### Get Fast Flag <a href="#get-hidden-ui" id="get-hidden-ui"></a>

{% code lineNumbers="true" %}
```typescript
<bool> getfflag(<string flagName>)
```
{% endcode %}

* Returns the value of `flagName`.

***

### Get FPS Cap <a href="#get-hidden-ui" id="get-hidden-ui"></a>

{% code lineNumbers="true" %}
```typescript
<void> getfpscap(<void>)
```
{% endcode %}

* Gets your FPS in-game.

***

### Get Hidden UI <a href="#get-hidden-ui" id="get-hidden-ui"></a>

```typescript
<Instance> gethui(<void>)
```

* Returns the `CoreGui` service, allowing GUI's being hidden from detection in-game.

***

### Get HWID

{% code lineNumbers="true" %}
```typescript
<string> gethwid(<void>)
```
{% endcode %}

* Gets the hardware ID (HWID) of the local system.

> Alternative: `get_hwid`

***

### Get Namecall Method

{% code lineNumbers="true" %}
```typescript
<string> getnamecallmethod(<void>)
```
{% endcode %}

* Returns the namecall method if the function is called in an `__namecall` metatable hook.

***

### Get Objects <a href="#get-thread-identity" id="get-thread-identity"></a>

{% code lineNumbers="true" %}
```typescript
<table> getobjects(<string assetIdOrUri>)
```
{% endcode %}

* Loads instances from `assetIdOrUri`.

***

### Get Thread Identity <a href="#get-thread-identity" id="get-thread-identity"></a>

```typescript
<void> getthreadidentity(<value> number)
```

* Returns the current thread's identification number.

> Alternative: `getidentity`, `getcontext`, `getthreadcontext`, `get_thread_context`, `get_thread_identity`

***

### Http Get

{% code lineNumbers="true" %}
```typescript
<string> httpget(<string url>)
```
{% endcode %}

* Sends an HTTP GET request to `url` and returns the response body as a string.

***

### Identify Executor

{% code lineNumbers="true" %}
```typescript
<string, string> identifyexecutor(<void>)
```
{% endcode %}

* Returns `Wave` and the version if the current executor is Wave.

> Alternative: `getexecutorname`

***

### Is Scriptable <a href="#is-scriptable" id="is-scriptable"></a>

```typescript
<bool> isscriptable(<Instance> object)
```

* Checks if `object` can be scripted or modified by a script.

***

{% hint style="info" %}
WARNING: `saveinstance()` is a Premium only function.
{% endhint %}

### Save Instance

{% code lineNumbers="true" %}
```typescript
<void> saveinstance(<Instance?> Object, <string?> FilePath, <table?> Options)
```
{% endcode %}

* Saves the current game into your workspace folder as a `.RBXL` file.

> If `Object` is specified, it will save that object and its descendants as a `.RBXM` file.

> If `Object` is `game`, it will be saved as a `.RBXL` file.

> If `FilePath` is specified, it will write the file to the specified path.

> `FilePath` does not need to contain a file extension, only the name of the file.

#### Options:



| Name                   | Type    | Default                                | Description                                                                                                                      |
| ---------------------- | ------- | -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Decompile              | Boolean | <mark style="color:red;">false</mark>  | If enabled, `LocalScripts` and `ModuleScripts` will be decompiled.                                                               |
| DecompileTimeout       | Number  | 10                                     | If the decompilation run time exceeds this value, it will be canceled. This value is in seconds.                                 |
| DecompileIgnore        | Table   | {"Chat", "CoreGui", "CorePackages"}    | Scripts that are a descendant of the specified services will be saved but not decompiled.                                        |
| NilInstances           | Boolean | <mark style="color:red;">false</mark>  | If enabled, instances parented to `nil` will be saved.                                                                           |
| RemovePlayerCharacters | Boolean | <mark style="color:green;">true</mark> | If enabled, player characters will not be saved.                                                                                 |
| SavePlayers            | Boolean | <mark style="color:red;">false</mark>  | If enabled, Player objects and their descendants will be saved.                                                                  |
| MaxThreads             | Number  | 3                                      | The number of decompilation threads that can run at once. More threads allow for more scripts to be decompiled at the same time. |
| ShowStatus             | Boolean | <mark style="color:green;">true</mark> | If enabled, Save Instance progress will be displayed.                                                                            |
| IgnoreDefaultProps     | Boolean | <mark style="color:green;">true</mark> | If enabled, default properties will not be saved.                                                                                |
| IsolateStarterPlayer   | Boolean | <mark style="color:green;">true</mark> | If enabled, `StarterPlayer` will be cleared and the saved starter player will be placed into folders.                            |

#### Example - Saving the game to a custom folder:

{% code lineNumbers="true" %}
```lua
makefolder("MySaves")
saveinstance(game, "MySaves/Cool Game")
```
{% endcode %}

#### Example - Saving a specific object with decompiled scripts:

{% code lineNumbers="true" %}
```lua
saveinstance(workspace.CoolModel, "Cool Model", {
    Decompile = true
})
```
{% endcode %}

***

### Set Clipboard

{% code lineNumbers="true" %}
```typescript
<void> setclipboard(<string> content)
```
{% endcode %}

* &#x20;Sets `content` to the clipboard.

> Alternative: `toclipboaard`

***

### Set Fast Flag

{% code lineNumbers="true" %}
```typescript
<void> setfflag(<string> flag, <string> value)
```
{% endcode %}

* Sets `flag`'s value to `value`.

> You can find a list of all Fast Flags here: [FFlag Tracker](https://raw.githubusercontent.com/MaximumADHD/Roblox-FFlag-Tracker/main/PCDesktopClient.json)

***

### Set FPS Cap

{% code lineNumbers="true" %}
```typescript
<void> setfpscap(<uint> cap)
```
{% endcode %}

* Sets the fps cap to `cap`.

***

### Set Namecall Method

{% code lineNumbers="true" %}
```typescript
<void> setnamecallmethod(<string> method)
```
{% endcode %}

* Sets the current namecall method to the new namecall method. Must be called in a `__namecall` metatable hook.

***

### Set Roblox Clipboard

{% code lineNumbers="true" %}
```typescript
<void> setrbxclipboard(<string> content)
```
{% endcode %}

* Sets `content` to the clipboard inside of Roblox.

***

### Set Thread Identity <a href="#set-thread-identity" id="set-thread-identity"></a>

```typescript
<void> setthreadidentity(<value> number)
```

* Sets the current thread's identification `number`.

> Alternative: `setidentity`, `setcontext`, `setthreadcontext`, `set_thread_context`, `set_thread_identity`

***

### Message Box

{% code lineNumbers="true" %}
```typescript
<uint> messagebox(<string> text, <string> title, <uint> flag)
```
{% endcode %}

* Creates a message box.

> Alternative: `messageboxasync`

***

#### Flags:

|              Flag             | Value |
| :---------------------------: | :---: |
|               OK              |   0   |
|          OK / Cancel          |   1   |
|     Abort / Retry / Ignore    |   2   |
|       Yes / No / Cancel       |   3   |
|            Yes / No           |   4   |
|         Retry / Cancel        |   5   |
| Cancel / Try Again / Continue |   6   |

#### Return Values:

| Value |       Description      |
| :---: | :--------------------: |
|   1   |     OK was clicked.    |
|   2   |   Cancel was clicked.  |
|   3   |   Abort was clicked.   |
|   4   |   Retry was clicked.   |
|   5   |   Ignore was clicked   |
|   6   |    Yes was clicked.    |
|   7   |     No was clicked.    |
|   10  | Try Again was clicked. |
|   11  |  Continue was clicked. |

***

### Queue On Teleport <a href="#queue-on-teleport" id="queue-on-teleport"></a>

```typescript
<void> queue_on_teleport(<string> script)
```

* Queues `script` to be executed after the next teleport.

> Alternative `queueonteleport`

***

### Request

```typescript
<table> request(<table> a1, <bool?> Async)
```

* Creates an http request with `a1`.

> Alternative: `http_request`

***

### ZSTD Compress

{% code lineNumbers="true" %}
```typescript
<string> zstdcompress(<string data>)
```
{% endcode %}

* Compresses `data` using the Zstandard (ZSTD) compression algorithm.

***

### ZSTD Decompress

{% code lineNumbers="true" %}
```typescript
<string> zstddecompress(<string data>)
```
{% endcode %}

* Decompresses `data` that was compressed with the Zstandard (ZSTD) algorithm.

***
