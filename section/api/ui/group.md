# group

### ui.create\_group

`ui.create_group(name: string, reference: string)`

```lua
local group = ui.create_group("Window", "window_ref")
print(group:get()) -- nil
```

### attach

`:attach(item: menu_item)`

<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>group:attach(checkbox)
</strong></code></pre>

### disable

`:disable(item: menu_item, state: boolean)`<mark style="color:blue;">**: boolean**</mark>

```lua
local group = ui.create_group("Window", "window_ref")
group:disable(true)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local group = ui.create_group("Window", "window_ref")
local disable_bool = group:disable(true)
print(disable_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local group = ui.create_group("Window", "window_ref")
local disable_bool = group:disable(false)
print(disable_bool) -- false
```
{% endtab %}
{% endtabs %}
