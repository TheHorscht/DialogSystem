# DialogSystem v0.1.0 for Noita
## Installation:
Copy the files into your mod, so the structure looks like this: `mods/yourmod/lib/DialogSystem/dialog_system.lua`

Then in your mod's init.lua, initialize the library like this:
```lua
dofile_once("mods/yourmod/lib/DialogSystem/init.lua")("mods/yourmod/lib/DialogSystem")
```
Passing in the path to where you placed the library.
## Usage
Then, to open a dialog, your `LuaComponent` needs to have `enable_coroutines="1"` and in your script do this:
```lua
dofile_once("mods/yourmod/lib/DialogSystem/dialog_system.lua")
dialog = dialog_system.open_dialog({
  name = "Whatever",
  portrait = "mods/yourmod/files/npc/portrait.xml",
  animation = "talk",
  typing_sound = "one",
  text = "Hello",
})
```