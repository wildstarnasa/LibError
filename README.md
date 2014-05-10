LibError
========

Wildstar Library - Super simplistic Error catcher for when you are using xpcall

Example Usage:
```lua
local tLibError = Apollo.GetPackage("Gemini:LibError-1.0")
local fnErrorHandler = tLibError and tLibError.tPackage.Error or Print

xpcall(function() Print("A" +  2) end, fnErrorHandler)
```

This causes the normal Addon Error screen to appear.
