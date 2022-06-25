# eventwinlogs
---------------------------------------------------------------------
Logon Type Code Explanation
2 Logon via console (keyboard, server KVM, or virtual client)
3 Network logon
4 Batch logon – often used by Scheduled Tasks
5 Windows Service logon
7 Credentials used to lock or unlock screen; RDP session reconnect
8 Network logon sending credentials in cleartext
9 Different credentials used than logged-on user — RunAs /netonly
10 Remote interactive logon (Remote Desktop Protocol)
11 Cached credentials used to logon – system likely offline from DC
12 Cached Remote Interactive (similar to Type 10)
13 Cached unlock (similar to Type 7)

----------------------------------------------------------------------
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


A 4624 successful logon and a 4647 user-initiated logoff.
The Logon ID allows us to tie the two events together and determine theamount of time the user was logged in during this session.
Remember that 4634 successful logoff events can also be used in place of 4647 events when they exist.
