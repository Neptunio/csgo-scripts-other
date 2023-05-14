# notify

### add

`notify.add(title: string, text: string, delay: number, accent: table, bg: table)` <mark style="color:purple;">`:notify_item`</mark>

```lua
local a = notify.add("A Title", "a text")
local b = notify.add("B Title", "b text", 6)
local c = notify.add("C Title", "c text", 7, Color(150, 0, 255))
local d = notify.add("D Title", "d text", 8, Color(150, 0, 255), Color(0, 0, 0))
```

### delete

`notify.delete(notify_item: any)` <mark style="color:purple;">`:boolean`</mark>

```lua
local a = notify.add("A Title", "a text")
notify.delete(a)
```
