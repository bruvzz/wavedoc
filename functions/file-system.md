---
description: These are all of the functions revolving the file system that Wave supports.
---

# 📂 File System

### Append File

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>&#x3C;void> appendfile(&#x3C;string> path, &#x3C;string> content)
</strong></code></pre>

Appends `content` to the file contents at `path`.

***

### Delete File

{% code lineNumbers="true" %}
```typescript
<void> delfile(<string> path)
```
{% endcode %}

* Deletes the file located at `path`.

> Alternative: `deletefile`

***

### Delete Folder

{% code lineNumbers="true" %}
```typescript
<void> delfolder(<string> path)
```
{% endcode %}

* Deletes the folder located at `path`.

> Alternative: `deletefolder`

***

### Get Custom Asset <a href="#get-custom-asset" id="get-custom-asset"></a>

```typescript
<string> getcustomasset(<string> path)
```

* Provides a content string suitable for use with GUI elements, sounds, meshes, and other assets to reference an item in the workspace folder.

***

### Is File

{% code lineNumbers="true" %}
```typescript
<bool> isfile(<string> path)
```
{% endcode %}

* Returns `true` if `path` is a file.

***

### Is Folder

{% code lineNumbers="true" %}
```typescript
<bool> isfolder(<string> path)
```
{% endcode %}

* Returns `true` if `path` is a folder.

***

### List Files

{% code lineNumbers="true" %}
```typescript
<table> listfiles(<string> folder)
```
{% endcode %}

* Returns a table of all files in `folder`.

***

### Load File

{% code lineNumbers="true" %}
```typescript
<function> loadfile(<string> path)
```
{% endcode %}

* Loads the contents of the file located at `path` as a Lua function and returns it.

***

### Make Folder

{% code lineNumbers="true" %}
```typescript
<void> makefolder(<string> path)
```
{% endcode %}

* Creates a new folder at `path`.

***

### Read File

{% code lineNumbers="true" %}
```typescript
<string> readfile(<string> path)
```
{% endcode %}

* Returns the contents of the file located at `path`.

***

### Write Custom Asset

{% code lineNumbers="true" %}
```typescript
<string> writecustomasset(<string filename>, <string data>)
```
{% endcode %}

* Creates a custom asset file that can be loaded into Roblox, writing the given `data` into the specified `filename`.

***

### Write File

{% code lineNumbers="true" %}
```typescript
<void> writefile(<string> path, <string> content)
```
{% endcode %}

* Writes `content` to the supplied `path`.

***
