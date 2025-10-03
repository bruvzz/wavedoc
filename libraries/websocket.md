# 📎 WebSocket

### Close

{% code lineNumbers="true" %}
```typescript
<void> Socket:Close(<void>)
```
{% endcode %}

* Closes the WebSocket connection.

***

|    Event   |                              Description                             |
| :--------: | :------------------------------------------------------------------: |
| .OnMessage | Activated when a message is receieved over the websocket connection. |
|  .OnClose  |          Activated when the websocket connection is closed.          |

***

### Connect

{% code lineNumbers="true" %}
```typescript
<bool> WebSocket.connect(<string> url)
```
{% endcode %}

* Connects with `url` and will return the instance representing the connection.

***

### Send

{% code lineNumbers="true" %}
```typescript
<void> Socket:Send(<string> text)
```
{% endcode %}

* Sends `text` to the WebSocket connection.

***
