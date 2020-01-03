# lua-logilights
lua-logilights is a wrapper around Logitech Lightsync APIs, with LuaJIT/Love2D applications in mind.

## Install
You **need** the DLL from a clean install of Logitech G HUB to use lua-logilights. The DLL can be located at `C:\Program Files\LGHUB\sdk_legacy_led_x64.dll` for 64-bit systems, and `C:\Program Files\LGHUB\sdk_legacy_led_x86.dll` for 32-bit systems. lua-logilights will automatically load the matching DLL for your system.

## Usage
All functions except `logitech.shutdown()` return a boolean.  
Call `logitech.init()` to set up the SDK, then wait a bit for the Logitech SDK to initialise itself.  
Call `logitech.setLightingForKey(keyName, r, g, b)` to set the specified key to the colour represented by r, g, b. RGB values are within 0 and 100.  
Call `logitech.setLighting(r, g, b)` to set the *entire device*'s lighting to the colour represented by r, g, b. I don't currently have a way to test this.  
Call `logitech.shutdown()` to shut the library down. You should always do this.  

Logitech DLL functions can be accessed via `logitech.lib`.

## Credits
Library by [ry00001](https://github.com/ry00001).  
Requested by [Oshisaure](https://twitter.com/oshisaure).  
Used in [Plumino^2](https://github.com/plumino/plumino2).