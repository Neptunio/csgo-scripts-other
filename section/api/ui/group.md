# 🕍 group

### ui.create\_group

`ui.create_group(name: string, reference: string)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local group = ui.create_group("Window", "window_ref")
print(group:get()) -- nil
```

### attach

`:attach(item: menu_item)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>group:attach(checkbox)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
```lua
local group_one = ui.create_group("Window1", "window1_ref")
local group_two = ui.create_group("Window2", "window2_ref")
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")

local attach_one = group_one:attach(checkbox)
local attach_two = group_two:attach(checkbox)

print(attach_one) -- false
print(attach_two) -- true
```
{% endtab %}
{% endtabs %}

### disable

`:disable(item: menu_item, state: boolean)` <mark style="color:purple;">`:boolean`</mark>

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
