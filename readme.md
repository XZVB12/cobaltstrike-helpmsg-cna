# CobaltStrike Helpmsg CNA

This cna contains error messages for Win32 error codes, HRESULT defintions, and NTSTATUS definitions. This cna can be helpful for those operating out of linux/mac clients without access to the net.exe program, or as a quick way to looking hresult/ntstatus codes without having to do a google search.

## Example

```
beacon> help helpmsg

Usage: helpmsg <code> [mode]
   code: The numerical code to search for. Prepend '0x' to the code to treat the code as a hex value
   mode: Can be 'win32', 'hresult', 'or 'ntstatus'. Default = 'win32'

beacon> helpmsg 53
[+] 

Code  : 53 [0x35]
Type  : Win32Error
Value : ERROR_BAD_NETPATH
Desc  : The network path was not found.

beacon> helpmsg 0xc0000022 ntstatus
[+] 

Code  : 0xc0000022
Type  : NTSTATUS
Value : STATUS_ACCESS_DENIED
Desc  : {Access Denied} A process has requested access to an object but has not been granted those access rights.
```