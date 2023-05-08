# slider

## create

`ui.create_slider(name: string, reference: string, default: number, min: number, max: number)` <mark style="color:purple;">`:menu_item`</mark>

```lua
local slider = ui.create_slider("Slider", "slider_ref")
```

{% hint style="info" %}
### Defaults

Min is<mark style="color:purple;">**`0`**</mark>

Max is<mark style="color:purple;">**`1`**</mark>

Default value is<mark style="color:purple;">**`0`**</mark>
{% endhint %}

### get

`:get()` <mark style="color:purple;">`:number`</mark>

<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>print(slider:get()) -- 0
</strong></code></pre>

### min

`:min()` <mark style="color:purple;">`:number`</mark>

<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>print(slider:min()) -- 0
</strong></code></pre>

### max

`:max()` <mark style="color:purple;">`:number`</mark>

<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>print(slider:max()) -- 1
</strong></code></pre>

### set

`:set(value: number, min: number, max: number)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>slider:set(1, -5, 5)
</strong>print(slider:get()) -- 1
</code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref", 2, 1, 5)
<strong>local set_bool = slider:set(1, -5, -5)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>local set_bool = slider:set(1, -5, -5)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(state: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>slider:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>local set_bool = slider:disable(true)
</strong>print(set_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local slider = ui.create_slider("Slider", "slider_ref")
<strong>local set_bool = slider:disable(false)
</strong>print(set_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}
