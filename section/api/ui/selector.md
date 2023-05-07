# selector

## create

`ui.create_selector(name: string, reference: string, items: table, value: number or string)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
```

{% hint style="info" %}
Value is<mark style="color:purple;">`1`</mark>or<mark style="color:purple;">`Item1`</mark>as default
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:number`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
print(selector:get()) -- Item1
```

### get\_num

`:get_num()` <mark style="color:purple;">`:number`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
print(selector:get_num()) -- 1
```

### set

`:set(value: string` or `number)` <mark style="color:purple;">`:boolean`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
selector:set("Item2")
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
local set_bool = selector:set("Item2")
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, "Item2")
local set_bool = selector:set(1)
print(set_bool) -- true
```
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
slider:disable(true)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
local set_bool = selector:disable(true)
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
local set_bool = selector:disable(false)
print(set_bool) -- false
```
{% endtab %}
{% endtabs %}
