# ui

### ui.get

`ui.get(item: string)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local item = ui.create(1, "Checkbox", "checkbox_ref", true)
local get = ui.get("checkbox_ref")
print(get) -- true
```

### ui.set

`ui.set(item: string, value: any)` <mark style="color:purple;">`:boolean`</mark>

```lua
local item = ui.create(1, "Checkbox", "checkbox_ref")
item:set(true)
print(item:get()) -- true
```

### ui.create

`ui.create(item: number, name: string, reference: string, value: any)`` `<mark style="color:purple;">`:menu_item`</mark>

<table data-view="cards"><thead><tr><th data-type="number">number</th><th>value</th><th data-type="content-ref">item</th></tr></thead><tbody><tr><td>0</td><td><mark style="color:purple;"><code>any</code></mark></td><td><a href="group.md">group.md</a></td></tr><tr><td>1</td><td><mark style="color:purple;"><code>boolean</code></mark></td><td><a href="checkbox.md">checkbox.md</a></td></tr><tr><td>2</td><td><mark style="color:purple;"><code>table</code></mark></td><td><a href="colorpicker.md">colorpicker.md</a></td></tr><tr><td>3</td><td>min, max, default <mark style="color:purple;"><code>number</code></mark></td><td><a href="slider.md">slider.md</a></td></tr><tr><td>4</td><td>items <mark style="color:purple;"><code>table</code></mark>, selected default <mark style="color:purple;"><code>number</code></mark></td><td><a href="selector.md">selector.md</a></td></tr><tr><td>5</td><td>items <mark style="color:purple;"><code>table</code></mark>, selected items <mark style="color:purple;"><code>table</code></mark></td><td><a href="multiselector.md">multiselector.md</a></td></tr></tbody></table>

```lua
local group = ui.create(0, "Window Name", "window_ref", true)
local checkbox = ui.create(1, "Checkbox", "checkbox_ref", true)
local color_picker = ui.create(2, "Colorpicker", "colorpicker_ref", Color(255, 255, 255))
local slider = ui.create(3, "Slider", "slider_ref", 0, 255, 200)
local selector = ui.create(4, "Selector", "selector_ref", {"Item1", "Item2"}, 2)
local multiselector = ui.create(5, "MultiSelector", "multiselector_ref", {"Item1", "Item2"}, {false, true})
```

{% tabs %}
{% tab title="Multiselector Variation 1" %}
```lua
local multiselector = ui.create(5, "MultiSelector", "multiselector_ref", {"Item1", "Item2"}, {true, false})
```
{% endtab %}

{% tab title="Multiselector Variation 2" %}
```lua
local multiselector = ui.create(5, "MultiSelector", "multiselector_ref", {"Item1", "Item2"}, {nil, "Item2"})
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Returns menu\_item on create
{% endhint %}

### ui.add\_color

`ui.add_color(item: string, color: table)` <mark style="color:purple;">`:menu_item`</mark>

<pre class="language-lua"><code class="lang-lua">local item, bool = ui.create(1, "Name", "reference", true)
<strong>local col = ui.add_color(item, Color(255, 255, 255))
</strong>
print(item:get()) -- checkbox value
print(col:get()) -- colorpicker value
print(ui.get("reference")) -- checkbox, colorpicker value
</code></pre>

### ui.attach

`ui.attach(item: menu_item, attach_item: menu_item)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local group = ui.create(0, "Window", "window_reference")
<strong>local checkbox = ui.create(1, "Checkbox", "checkbox_ref")
</strong>ui.attach(group, checkbox)
</code></pre>

### ui.disable

`ui.disable(item: menu_item, state: boolean)` <mark style="color:purple;">`:menu_item`</mark>

<pre class="language-lua"><code class="lang-lua">local item, bool = ui.create(1, "Name", "reference", true)
<strong>local col = ui.add_color(item, Color(255, 255, 255))
</strong>
print(item:get()) -- checkbox value
print(col:get()) -- colorpicker value
print(ui.get("reference")) -- checkbox, colorpicker value
</code></pre>
