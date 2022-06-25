# eventwinlogs

The following Logon Type Codes can be used:[1]
2: Logon via a console (keyboard, server KVM, or virtual client like VNC)
3: Network logon (often using something like SMB for drive mapping)
4: Batch logon (Scheduled Tasks) – non-interactive
5: Windows Service logon – non-interactive
7: Lock or unlock of screen (reconnecting to an existing RDP session can also use this Logon Type)
8: Network logon sending credentials in cleartext (potentially indicative of a downgrade attack or older admin tool)
9: Different credentials used to authenticate than those currently logged on with (“RunAs /netonly” command or similar)
10: Remote interactive logon (Terminal Services/Remote Desktop Protocol)
11: Cached credentials used to log on due to system not in communication with the domain controller
12: Cached credentials used for a remote interactive logon (RDP). Previously rare, but now being seen when Microsoft “live” accounts are used for authentication on standalone workstations
13: Cached credentials used for an unlock operation
