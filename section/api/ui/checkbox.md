# ✅ checkbox

### create

`ui.create_checkbox(name: string, reference: string, value: boolean)`

```lua
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
```

{% hint style="info" %}
Value is `false` as default
{% endhint %}

### get

`:get()`<mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>print(checkbox:get()) -- false
</strong></code></pre>

### set

`:set(value: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>checkbox:set(true)
</strong>print(checkbox:get()) -- true
</code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>local set_bool = checkbox:set(true)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref", true)
<strong>local set_bool = checkbox:set(false)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:blue;">**: boolean**</mark>

<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>checkbox:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>local set_bool = checkbox:disable(true)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>local set_bool = checkbox:disable(false)
</strong>print(set_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}

