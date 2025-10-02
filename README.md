## How 2 Use
📥 Loading the Library

```lua
local library, notifications = loadstring(game:HttpGet("https://raw.githubusercontent.com/i77lhm/Libraries/refs/heads/main/Priv9/Library.lua"))(
)
```

library → Main UI library object

notifications → Notification manager object

🪟 Window

Creates a new window.

```lua
local window = library:window({
name = <string>
})
```

Field	Type	Description
name	<string>	Title of the window.

Returns: window object

🔔 Notifications

Creates a notification.

```lua
notifications:create_notification({
name = <string>
})
```

Field	Type	Description
name	<string>	Text to display.

Returns: nil

📑 Tabs

Adds a tab to the window.

```lua
local tab = window:tab({
name = <string>
})
```

Field	Type	Description
name	<string>	Tab’s display name.

Returns: tab object

🧱 Columns

Adds a column inside a tab.

```lua
local column = tab:column({})
```

Field	Type	Description
(none required)	–	Creates a column container.

Returns: column object

📦 Sections

Adds a section inside a column.

```lua
local section = column:section({
name = <string>,
auto_fill = <boolean>,
size = <number>
})
```

Field	Type	Description
name	<string>	Section title.
auto_fill	<boolean>	Auto-fill remaining space.
size	<number>	Section size ratio (0–1).

Returns: section object

✅ Toggles

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

Returns: toggle object

⌨️ Keybind

Creates a keybind selector.

```lua
section:keybind({
name = <string>
})
```

Field	Type	Description
name	<string>	Label for keybind.

Returns: keybind object

🎚️ Sliders

Creates a slider control.

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

Returns: slider object

📜 Dropdown

Creates a dropdown selector.

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

Returns: dropdown object

🖲️ Button

Creates a clickable button.

```lua
section:button({
name = <string>,
callback = <function>
})
```

Field	Type	Description
name	<string>	Button text.
callback	<function>	Function called on click.

Returns: button object

⚙️ Config

Initializes configuration saving/loading for the specified window.

```lua
library:init_config(window)
```

Argument	Type	Description
window	<window>	The window to configure.

Returns: nil
