# 🖥️ ImGui

### ImGui.new

* Creates a new ImGui Window.

#### Example:

{% code lineNumbers="true" %}
```typescript
local ui = ImGui.new({ title = "Example" });
```
{% endcode %}

***

### Text

* Creates a text column.

#### Example:

{% code lineNumbers="true" %}
```typescript
ui:Text({ title = "Hello", content = "Hello, this is an example script for Wave's ImGui Library."});
```
{% endcode %}

***

### TabBar

* Creates a side bar to put your tabs.

#### Example:

{% code lineNumbers="true" %}
```typescript
ui:TabBar({ title = "TabBar1"});
```
{% endcode %}

***

### TabItem

* Creates a new tab.

#### Example:

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>local tab_1 = ui:TabItem({ title = "Buttons &#x26; InputText"});
</strong></code></pre>

***

### Button

* Creates a new button.

#### Example:

<pre class="language-typescript" data-line-numbers><code class="lang-typescript"><strong>tab_1:Button({
</strong>    title = "ExampleButton1",
    callback = function()
        print("Clicked on the button in the Buttons Tab!");
    end
});
tab_1:Button({
    title = "RunSUNC",
    callback = function()
        loadstring(game:HttpGet("https://gitlab.com/sens3/nebunu/-/raw/main/HummingBird8's_sUNC_yes_i_moved_to_gitlab_because_my_github_acc_got_brickedd/sUNCm0m3n7.lua"))()
    end
});
</code></pre>

***

### InputText

* Creates a new text-box.

#### Example:

{% code lineNumbers="true" %}
```typescript
tab_1:InputText({
    title = "ExampleInputText",
    defaultText = "Input Example!"
});
```
{% endcode %}

***

### EndTabItem

* Ends any programmed code beyond the called function.

#### Example:

{% code lineNumbers="true" %}
```typescript
tab_1:EndTabItem();
```
{% endcode %}

### CheckBox

* Creates a checkbox.

#### Example:

{% code lineNumbers="true" %}
```typescript
local tab_2 = ui:TabItem({ title = "Checkbox & Slider" });
tab_2:CheckBox({ title = "ExampleCheckBox" });
```
{% endcode %}

***

### Slider

* Creates a slider.

#### Example:

{% code lineNumbers="true" %}
```typescript
tab_2:Slider({
    title = "ExampleSlider",
    min = 0,
    max = 100
});
tab_2:EndTabItem();
```
{% endcode %}

***

### ComboBox

* Creates a combo box.

#### Example:

{% code lineNumbers="true" %}
```typescript
local tab_3 = ui:TabItem({ title = "Combobox & Listbox" });
tab_3:ComboBox({ 
    title = "ExampleComboBox",
    items = {"Ex1", "Ex2", "Ex3"}
});
```
{% endcode %}

***

### ListBox

* Creates a list box.

#### Example:

{% code lineNumbers="true" %}
```typescript
tab_3:ListBox({
    title = "ExampleListBox",
    items = {"Ex1L", "Ex2L", "Ex3L"},
    currentItem = 1
});
tab_3:EndTabItem();
```
{% endcode %}

***

### ColorPicker

* Creates a colorpicker.

#### Example:

{% code lineNumbers="true" %}
```typescript
local tab_4 = ui:TabItem({ title = "Color Picker" });
tab_4:ColorPicker({
    title = "ExampleColorPicker",
    color = {25, 25, 25}
});
tab_4:EndTabItem();
```
{% endcode %}

***

### EndTabBar

* Ends any code beyond `TabBar` was called.

#### Example:

{% code lineNumbers="true" %}
```typescript
ui:EndTabBar();
```
{% endcode %}

***

### End

* Ends any code beyond `ImGui.new` was called.

#### Example:

{% code lineNumbers="true" %}
```typescript
ui:End(); -- Ends the ImGui Window!
```
{% endcode %}

***

#### Example of ImGui:

{% code lineNumbers="true" %}
```typescript
local ui = ImGui.new({ title = "Example" }); -- Begin ImGui Window
ui:Text({ title = "Hello", content = "Hello, this is an example script for Wave's ImGui Library."});

ui:TabBar({ title = "TabBar1"});

-- Tab 1
local tab_1 = ui:TabItem({ title = "Buttons & InputText"});
tab_1:Button({
    title = "ExampleButton1",
    callback = function()
        print("Clicked on the button in the Buttons Tab!");
    end
});
tab_1:Button({
    title = "RunSUNC",
    callback = function()
        loadstring(game:HttpGet("https://gitlab.com/sens3/nebunu/-/raw/main/HummingBird8's_sUNC_yes_i_moved_to_gitlab_because_my_github_acc_got_brickedd/sUNCm0m3n7.lua"))()
    end
});
tab_1:InputText({
    title = "ExampleInputText",
    defaultText = "Input Example!"
});
tab_1:EndTabItem();

-- Tab 2
local tab_2 = ui:TabItem({ title = "Checkbox & Slider" });
tab_2:CheckBox({ title = "ExampleCheckBox" });
tab_2:Slider({
    title = "ExampleSlider",
    min = 0,
    max = 100
});
tab_2:EndTabItem();

-- Tab 3
local tab_3 = ui:TabItem({ title = "Combobox & Listbox" });
tab_3:ComboBox({ 
    title = "ExampleComboBox",
    items = {"Ex1", "Ex2", "Ex3"}
});
tab_3:ListBox({
    title = "ExampleListBox",
    items = {"Ex1L", "Ex2L", "Ex3L"},
    currentItem = 1
});
tab_3:EndTabItem();

-- Tab 4
local tab_4 = ui:TabItem({ title = "Color Picker" });
tab_4:ColorPicker({
    title = "ExampleColorPicker",
    color = {25, 25, 25}
});
tab_4:EndTabItem();

ui:EndTabBar();
ui:End(); -- End the ImGui Window!
```
{% endcode %}
