# selector

## create

`ui.create_selector(name: string, reference: string, items: table, value: number or string)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
```

{% hint style="info" %}
Value is<mark style="color:purple;">**`1`**</mark>or<mark style="color:purple;">**`Item1`**</mark>as default
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:number`</mark>

<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
<strong>print(selector:get()) -- Item1
</strong></code></pre>

### get\_num

`:get_num()` <mark style="color:purple;">`:number`</mark>

<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
<strong>print(selector:get_num()) -- 1
</strong></code></pre>

### set

`:set(value: string` or `number)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
<strong>selector:set("Item2")
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
<strong>local set_bool = selector:set("Item2")
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, "Item2")
<strong>local set_bool = selector:set(1)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
<strong>slider:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
<strong>local set_bool = selector:disable(true)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"}, 2)
<strong>local set_bool = selector:disable(false)
</strong>print(set_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}
