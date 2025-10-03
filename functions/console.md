---
description: These are all of the functions revolving the console that Wave supports.
---

# 🎮 Console

### Clear

{% code lineNumbers="true" %}
```typescript
<void> rconsoleclear(<void>)
```
{% endcode %}

* Clears all text from the console.

***

### Close

{% code lineNumbers="true" %}
```typescript
<void> rconsoleclose(<void>)
```
{% endcode %}

* Closes the console.

> Alternative: `rconsoledestroy`

***

### Create

{% code lineNumbers="true" %}
```typescript
<void> rconsolecreate(<void>)
```
{% endcode %}

* Creates a new console window for logging and interaction.

***

### Debug

{% code lineNumbers="true" %}
```typescript
<void> rconsoledebug(<string text>)
```
{% endcode %}

* Prints a debug message to the console in a distinct debug color/style.

***

### Error

{% code lineNumbers="true" %}
```typescript
<void> rconsoleerr(<string> text)
```
{% endcode %}

* Prints `text` into the console, with <mark style="color:red;">`[ERROR]`</mark> written before it.

***

### Info

{% code lineNumbers="true" %}
```typescript
<void> rconsoleinfo(<string> text)
```
{% endcode %}

* Prints `text` into the console, with <mark style="color:yellow;">`[INFO]`</mark> written before it.

***

### Input

{% code lineNumbers="true" %}
```typescript
<string> rconsoleinput(<void>)
```
{% endcode %}

* Yields the current thread until the user inputs text and presses `Enter`. Returns the input they put in.

***

### Name

{% code lineNumbers="true" %}
```typescript
<void> rconsolename(<string> title)
```
{% endcode %}

* Sets the console's title to `title`.

> Alternative: `rconsolesettitle`

***

### Print

{% code lineNumbers="true" %}
```typescript
<void> rconsoleprint(<string> text)
```
{% endcode %}

* Prints `text` into the console.

***

### Print Console

{% code lineNumbers="true" %}
```typescript
<void> printconsole(<string> message, <byte> red, <byte> green, <byte> blue)
```
{% endcode %}

* Prints `message` into the internal and integrated console with RGB value.

***

#### Console Colors:

|      Name     |        Type        |
| :-----------: | :----------------: |
|     Black     |      @@BLACK@@     |
|      Blue     |      @@BLUE@@      |
|     Green     |      @@GREEN@@     |
|      Cyan     |      @@CYAN@@      |
|      Red      |       @@RED@@      |
|    Magenta    |     @@MAGENTA@@    |
|   Light Gray  |   @@LIGHT\_GRAY@@  |
|   Dark Gray   |   @@DARK\_GRAY@@   |
|   Light Blue  |   @@LIGHT\_BLUE@@  |
|  Light Green  |  @@LIGHT\_GREEN@@  |
|   Light Cyan  |   @@LIGHT\_CYAN@@  |
|   Light Red   |   @@LIGHT\_RED@@   |
| Light Magenta | @@LIGHT\_MAGENTA@@ |
|     Yellow    |     @@YELLOW@@     |
|     White     |      @@WHITE@@     |

Example:

{% code lineNumbers="true" %}
```lua
rconsolename("console") -- Sets the name of the console to 'console'
rconsoleprint("gamer\n")
rconsoleprint("@@YELLOW@@") -- Changes the text color to Yellow
rconsoleprint("gamer but yellow\n")
rconsoleerr("omg error!")
rconsolewarn("omg warning!")
wait(3)
rconsoleclear() -- Clears all text
wait(1)
rconsoleclose() -- Closes the console
```
{% endcode %}

You must use `\n` at the end of `rconsoleprint` to make a new line.

`rconsoleinfo`, `rconsolewarn`, and `rconsoleerr` do this automatically.\


***
