# ui

### ui.get

`ui.get(item: string)`: menu\_item

{% hint style="info" %}
Returns menu\_item (not value)
{% endhint %}

### ui.set

`ui.set(item: string, value: any)`: bool

{% hint style="info" %}
Returns boolean on set
{% endhint %}

### ui.create

`ui.create(item: number, name: string, reference: string, value: any)`: menu\_item

<table data-view="cards"><thead><tr><th>item</th><th data-type="number">number</th><th>value</th></tr></thead><tbody><tr><td>group</td><td>0</td><td>any</td></tr><tr><td>checkbox</td><td>1</td><td>boolean</td></tr><tr><td>colorpicker</td><td>2</td><td>table</td></tr><tr><td>slider</td><td>3</td><td>min, max, default <code>number</code></td></tr><tr><td>selector</td><td>4</td><td>items <code>table</code>, selected default <code>number</code></td></tr><tr><td>multiselector</td><td>5</td><td>items <code>table</code>, selected items <code>table</code></td></tr></tbody></table>

```lua
local group = ui.create(0, "Window Name", "window_ref", true)
local checkbox = ui.create(1, "Checkbox", "checkbox_ref", true)
local color_picker = ui.create(2, "Colorpicker", "colorpicker_ref", Color(255, 255, 255))
local slider = ui.create(3, "Slider", "slider_ref", 0, 255, 200)
local selector = ui.create(4, "Selector", "selector_ref", {"Item1", "Item2"}, 2)
local multiselector = ui.create(5, "MultiSelector", "multiselector_ref", {"Item1", "Item2"}, {false, true})
```

MultiSelector Variations

```lua
local multiselector_one = ui.create(5, "MultiSelector1", "multiselector1_ref", {"Item1", "Item2"}, {true, false}), {false, true})
local multiselector_two = ui.create(5, "MultiSelector2", "multiselector2_ref", {"Item1", "Item2"})
```

{% hint style="info" %}
Returns menu\_item on create
{% endhint %}

### ui.add\_color

`ui.add_color(item: string, color: table)`: menu\_item

<pre class="language-lua"><code class="lang-lua">local item, bool = ui.create(1, "Name", "reference", true)
<strong>local col = ui.add_color(item, Color(255, 255, 255))
</strong>
print(item:get()) -- checkbox value
print(col:get()) -- colorpicker value
print(ui.get("reference")) -- checkbox, colorpicker value
</code></pre>

### ui.attach

`ui.attach(item: menu_item, attach_item: menu_item)`: bool

<pre class="language-lua"><code class="lang-lua">local group = ui.create(0, "Window", "window_reference")
<strong>local checkbox = ui.create(1, "Checkbox", "checkbox_ref")
</strong>ui.attach(group, checkbox)
</code></pre>
