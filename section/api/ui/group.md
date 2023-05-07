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
