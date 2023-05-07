# slider

## create

`ui.create_slider(name: string, reference: string, default: number, min: number, max: number)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
```

{% hint style="info" %}
### Defaults

Min is<mark style="color:purple;">`0`</mark>

Max is<mark style="color:purple;">`1`</mark>

Default value is<mark style="color:purple;">`0`</mark>
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:string`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
print(slider:get()) -- 0
```

### min

`:min()` <mark style="color:purple;">`:number`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
print(slider:min()) -- 0
```

### max

`:max()` <mark style="color:purple;">`:number`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
print(slider:max()) -- 1
```

### set

`:set(value: table)` <mark style="color:purple;">`:boolean`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
slider:set(1, -5, 5)
print(slider:get()) -- 1
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local slider = ui.create_slider("Slider", "slider_ref", 2, 1, 5)
local set_bool = slider:set(1, -5, -5)
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local slider = ui.create_slider("Slider", "slider_ref")
local set_bool = slider:set(1, -5, -5)
print(set_bool) -- true
```
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
slider:disable(true)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local slider = ui.create_slider("Slider", "slider_ref")
local set_bool = slider:disable(true)
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local slider = ui.create_slider("Slider", "slider_ref")
local set_bool = slider:disable(false)
print(set_bool) -- false
```
{% endtab %}
{% endtabs %}
