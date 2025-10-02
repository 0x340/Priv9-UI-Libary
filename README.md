## How 2 Use
Loading the Library

```lua
local library, notifications = loadstring(game:HttpGet("https://raw.githubusercontent.com/i77lhm/Libraries/refs/heads/main/Priv9/Library.lua"))(
)
```

library → Main UI library object

notifications → Notification manager object

Window
```lua
local window = library:window({
name = <sting> -- window name
})
```



Notifications
```lua
notifications:create_notification({
name = <string> -- notification text
})
```

Tabs
```lua
local tab = window:tab({
name = <string> -- 
})
```

Field	Type	Description
name	<string>	Tab’s display name.

Returns: tab object

Columns
```lua
local column = tab:column({})
```


Sections
```lua
local section = column:section({
name = <string>,
auto_fill = <boolean>,
size = <number>
})
```

Creates a toggle switch.

```lua
section:toggle({
name = <string>,
flag = <string>
})
```

Field	Type	Description
name	<string>	Toggle’s label.
flag	<string>	Internal flag name.



Keybind
```lua
section:keybind({
name = <string>
})
```

Field	Type	Description
name	<string>	Label for keybind.

Returns: keybind object

Sliders
```lua
section:slider({
name = <string>,
min = <number>,
max = <number>,
default = <number>,
interval = <number>,
suffix = <string>
})
```

Field	Type	Description
name	<string>	Label for slider.
min	<number>	Minimum value.
max	<number>	Maximum value.
default	<number>	Default value.
interval	<number>	Step interval.
suffix	<string>	Text suffix (e.g. %, px).


Dropdown
```lua
section:dropdown({
name = <string>,
flag = <string>,
items = {<string>, <string>},
default = <string>
})
```

Field	Type	Description
name	<string>	Label for dropdown.
flag	<string>	Internal flag name.
items	<table>	List of <string> items.
default	<string>	Default selected item.



Button
```lua
section:button({
name = <string>,
callback = <function>
})
```

Field	Type	Description
name	<string>	Button text.
callback	<function>	Function called on click.



Config
```lua
library:init_config(window)
```

Argument	Type	Description
window	<window>	The window to configure.

Returns: nil
