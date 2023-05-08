# group

### ui.create\_group

`ui.create_group(name: string, reference: string)` <mark style="color:purple;">`:menu_item`</mark>

<pre class="language-lua"><code class="lang-lua"><strong>local group = ui.create_group("Window", "window_ref")
</strong>print(group:get()) -- nil
</code></pre>

### attach

`:attach(item: menu_item)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")
<strong>group:attach(checkbox)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local group_one = ui.create_group("Window1", "window1_ref")
local group_two = ui.create_group("Window2", "window2_ref")
local checkbox = ui.create_checkbox("Checkbox", "checkbox_ref")

<strong>local attach_one = group_one:attach(checkbox)
</strong><strong>local attach_two = group_two:attach(checkbox)
</strong>
print(attach_one) -- false
print(attach_two) -- true
</code></pre>
{% endtab %}
{% endtabs %}

### disable

`:disable(item: menu_item, state: boolean)` <mark style="color:purple;">`:boolean`</mark>

<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
<strong>group:disable(true)
</strong></code></pre>

{% tabs %}
{% tab title="Variation 1" %}
<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
<strong>local disable_bool = group:disable(true)
</strong>print(disable_bool) -- true
</code></pre>
{% endtab %}

{% tab title="Variation 2" %}
<pre class="language-lua"><code class="lang-lua">local group = ui.create_group("Window", "window_ref")
<strong>local disable_bool = group:disable(false)
</strong>print(disable_bool) -- false
</code></pre>
{% endtab %}
{% endtabs %}
