# multiselector

## create

`ui.create_multiselector(name: string, reference: string, items: table, value: table)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
```

{% hint style="info" %}
Value is<mark style="color:purple;">`nil`</mark>as default
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:string`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
print(selector:get()) -- Item1
```

### set

`:set(value: string)` <mark style="color:purple;">`:boolean`</mark>

```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
selector:set("Item2")
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
local set_bool = selector:set({"Item1", "Item2"})
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
local set_bool = selector:set({false, true})
print(set_bool) -- true
```
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
multiselector:disable(true)
```

{% tabs %}
{% tab title="Variation 1" %}
```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
local set_bool = multiselector:disable(true)
print(set_bool) -- true
```
{% endtab %}

{% tab title="Variation 2" %}
```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
local set_bool = multiselector:disable(false)
print(set_bool) -- false
```
{% endtab %}
{% endtabs %}
