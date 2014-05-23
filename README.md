LibError
========

Wildstar Library - Super simplistic Error catcher for when you are using xpcall

Example Usage:
```lua
local tLibError = Apollo.GetPackage("Gemini:LibError-1.0")
local fnErrorHandler = tLibError and tLibError.tPackage and tLibError.tPackage.Error or Print

xpcall(function() Print("A" +  2) end, fnErrorHandler)
```

This causes the normal Addon Error screen to appear when an error is encountered in the
protected call.  Using error as the second argument of xpcall does not work as expected and
using Print will not display any errors that occur before the ChatLog is loaded.
