# cmd_admin_here.reg

Run cmd with Administrators rights from any folder by mouse right click menu

```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\runas]
@="Open CMD here as Administrator"
"HasLUAShield"=""
"Icon"="cmd.exe"

[HKEY_CLASSES_ROOT\Directory\Background\shell\runas\command]
@="powershell.exe -windowstyle hidden -command \"Start-Process cmd.exe -ArgumentList '/s,/k,pushd,%V' -Verb RunAs\""
```
