# colorpicker

## create

`ui.create_colorpicker(name: string, reference: string, value: table)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local colorpicker = ui.create_colorpicker("Colorpicker", "colorpicker_ref")
```

### get

`:get()` <mark style="color:purple;">`:table`</mark>

```lua
local colorpicker = ui.create_colorpicker("Colorpicker", "colorpicker_ref")
print(colorpicker:get()) -- Color(255, 255, 255)
```

### set

`:set(value: table)` <mark style="color:purple;">`:boolean`</mark>

```lua
local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
colorpicker:set(Color(255, 0, 255))
print(colorpicker:get()) -- Color(255, 0, 255)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref", Color(0, 255, 0))
local set_bool = colorpicker:set(Color(255, 255, 0))
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local checkbox = ui.create_colorpicker("Checkbox", "checkbox_ref")
local set_bool = checkbox:set(Color(255, 0, 0))
print(set_bool) -- true
```
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

```lua
local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
checkbox:disable(true)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
local set_bool = colorpicker:disable(true)
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
local set_bool = colorpicker:disable(false)
print(set_bool) -- false
```
{% endtab %}
{% endtabs %}
