# 🖍️ Drawing

### Drawing.New

{% code lineNumbers="true" %}
```typescript
<object> Drawing.new(<string> type)
```
{% endcode %}

* Creates a new drawing object with `type`. Returns the object.

***

#### Example:

<pre class="language-lua" data-line-numbers><code class="lang-lua">local circle = Drawing.new('Circle')
circle.Radius = 50
circle.Color = Color3.fromRGB(255, 255, 255)
circle.Filled = false
circle.NumSides = 32
circle.Position = Vector2.new(20, 20)
circle.Transparency = 0.9

local square = Drawing.new('Square')
square.Position = Vector2.new(20, 20)
square.Size = Vector2.new(20, 20)
square.Thickness = 2
square.Color = Color3.fromRGB(255, 255, 255)
square.Filled = true
square.Transparency = 0.9

local line = Drawing.new('Line')
line.PointA = Vector2.new(20, 20) -- Origin
line.PointB = Vector2.new(50, 50) -- Destination
line.Color = Color3.new(.33, .66, .99)
line.Thickness = 1
line.Transparency = 0.9

local text = Drawing.new('Text')
text.Text = 'Wave on Top'
text.Color = Color3.new(1, 1, 1)
text.OutlineColor = Color3.new(0, 0, 0)
text.Center = true
text.Outline = true
text.Position = Vector2.new(100, 100)
text.Size = 20
text.Font = Drawing.Fonts.Monospace -- Monospace, UI, System, Plex
text.Transparency = 0.9

<strong>local image = Drawing.new('Image')
</strong>image.Color = Color3.new(0, 0, 0)
image.Rounding = 3
image.Size = Vector2.new(256, 256)
image.Position = Vector2.new(100, 100)
image.Transparency = 0.9

local quad = Drawing.new('Quad')
quad.Color = Color3.new(.1, .2, .3)
quad.Filled = false
quad.Thickness = 2
quad.Point1 = Vector2.new(100, 0)
quad.Point2 = Vector2.new(50, 50)
quad.Point3 = Vector2.new(0, 100)
quad.Point4 = Vector2.new(100, 100)
quad.Transparency = 0.69

local triangle = Drawing.new('Triangle')
triangle.PointA = Vector2.new(50, 0)
triangle.PointB = Vector2.new(0, 50)
triangle.PointC = Vector2.new(100, 50)
triangle.Thickness = 3
triangle.Color = Color3.new(1, 0, 0)
triangle.Filled = true
triangle.Transparency = 1.0

-- Destroy All Drawings.

--for i in next, {circle, square, line, text, image, quad, triangle} do
    --i:Destroy()
--end
</code></pre>

### Clear Draw Cache

{% code lineNumbers="true" %}
```typescript
<void> cleardrawcache(<void>)
```
{% endcode %}

* Removes all drawing object(s) in the cache.

***

### Get Render Property

{% code lineNumbers="true" %}
```typescript
<variant> getrenderproperty(<Drawing>, <string>)
```
{% endcode %}

* Grabs the value of a property of a drawing object.

> Alternative: `get_render_property`, `getrenderobj`

***

### Is Render Property

{% code lineNumbers="true" %}
```typescript
<bool> isrenderproperty(<variant>)
```
{% endcode %}

* Returns if the assigned property is a valid drawing.

> Alternative: `isrenderobj`, `is_render_property`

***

### Set Render Property

{% code lineNumbers="true" %}
```typescript
<void> setrenderproperty(<Drawing>, <string>, <variant>)
```
{% endcode %}

* Sets the value of a property of a drawing object.

> Alternative: `set_render_property`, `setrenderobj`
