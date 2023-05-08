# colorpicker

### create

`ui.create_colorpicker(name: string, reference: string, value: table)` <mark style="color:purple;">`:menu_item`</mark>

{% hint style="info" %}
Default value is <mark style="color:purple;">**`Color(255, 255, 255)`**</mark>
{% endhint %}

```lua
local colorpicker = ui.create_colorpicker("Colorpicker", "colorpicker_ref")
```

### get

`:get()` <mark style="color:purple;">`:table`</mark>

<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Colorpicker", "colorpicker_ref")
<strong>print(colorpicker:get()) -- Color(255, 255, 255)
</strong></code></pre>

### set

`:set(value: table)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
<strong>colorpicker:set(Color(255, 0, 255))
</strong>print(colorpicker:get()) -- Color(255, 0, 255)
</code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref", Color(0, 255, 0))

<strong>local set_bool_one = colorpicker:set(Color(255, 255, 0))
</strong><strong>local set_bool_two = colorpicker:set(Color(45, 255, 50))
</strong>
print(set_bool_one) -- false
print(set_bool_two) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref", Color(0, 255, 0))
<strong>local set_bool = checkbox:set(Color(255, 0, 0))
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
<strong>checkbox:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")

<strong>local set_bool_one = colorpicker:disable(true)
</strong><strong>local set_bool_two = colorpicker:disable(false)
</strong>
print(set_bool_one) -- true
print(set_bool_two) -- false
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local colorpicker = ui.create_colorpicker("Checkbox", "checkbox_ref")
<strong>local set_bool = colorpicker:disable(false)
</strong>print(set_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}
