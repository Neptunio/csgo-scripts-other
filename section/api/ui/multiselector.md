# multiselector

## create

`ui.create_multiselector(name: string, reference: string, items: table, value: table)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
```

{% hint style="info" %}
Value is<mark style="color:purple;">**`nil`**</mark>as default
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:string`</mark>

<pre class="language-lua"><code class="lang-lua">local selector = ui.create_selector("Selector", "selector_ref", {"Item1", "Item2"})
<strong>print(selector:get()) -- Item1
</strong></code></pre>

### set

`:set(value: table)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>selector:set({"Item", nil})
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>local set_bool = selector:set({"Item1", "Item2"})
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>local set_bool = selector:set({false, true})
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>multiselector:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>local set_bool = multiselector:disable(true)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local multiselector = ui.create_multiselector("MultiSelector", "multiselector_ref", {"Item1", "Item2"})
<strong>local set_bool = multiselector:disable(false)
</strong>print(set_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}
