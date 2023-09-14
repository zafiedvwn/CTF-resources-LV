# CTF Resources Compilation

## Links

**from github**


- [ctf-awesome-resources by devploit](https://github.com/devploit/ctf-awesome-resources)

- [awesome-ctf by apsdehal](https://github.com/apsdehal/awesome-ctf)

- [Hacking Cheat Sheet by hasamba](https://github.com/hasamba/Hacking-and-CTF-Cheat-Sheet/blob/main/Hacking%20Cheat%20Sheet.md#hacking-cheat-sheet)

- [Owasp Cheat Sheet Series by mansoorr123](https://github.com/OWASP/CheatSheetSeries/tree/master/cheatsheets)

---

**from other resources links**

*[Cheatography](https://cheatography.com)*

- [Ethical Hacking by prolixgal](https://cheatography.com/prolixgal/cheat-sheets/ethical-hacking/)
- [Web Application Hacking by fahad](https://cheatography.com/fahad/cheat-sheets/web-application-hacking/)
- [Linux | Windows Privilege Escalation](https://cheatography.com/blacklist/cheat-sheets/linux-windows-privilege-escalation/)
- [nmap by netwrkspider](https://cheatography.com/netwrkspider/cheat-sheets/nmap-cheatsheet/)
- [ncat by flacman](https://cheatography.com/flacman/cheat-sheets/ncat-cheat-sheet/)
- [wifi-hacking by astronaut3301](https://cheatography.com/astronaut3301/cheat-sheets/wifi-hacking/)
- [meatasploit by alexismon](https://cheatography.com/alexismon/cheat-sheets/metasploit-cheat-sheet/)

---

**[Roppers](https://www.roppers.org/)**

### Encoding and Classic Encryption

- [ASCII](https://catonmat.net/ascii-cheat-sheet)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [Index of Coincidence Converter](https://www.dcode.fr/index-coincidence)
- [Caesar Cipher Converter](https://www.dcode.fr/caesar-cipher)
- [Mono-alphabetic Substitution Converter](https://www.dcode.fr/monoalphabetic-substitution)
- [Frequency Analysis](https://www.dcode.fr/frequency-analysis)
- [Vignere Cipher Decoder and Solver](https://www.boxentriq.com/code-breaking/vigenere-cipher)
- [Vignere Cipher](https://www.dcode.fr/vigenere-cipher)
- [RapidTables](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html)

### File Forensics

- [RFC2083](https://tools.ietf.org/html/rfc2083)
- [xxd command](https://linuxhandbook.com/xxd-command/)
- [bless hexeditor](https://miloserdov.org/?p=5666)
- [base64 in cmd](https://www.serverlab.ca/tutorials/linux/administration-linux/how-to-base64-encode-and-decode-from-command-line/)
- [create jar file](https://github.com/macagua/example.java.helloworld)
- [pngcheck](http://www.libpng.org/pub/png/apps/pngcheck.html) - verifies integrity of png file
- [exiftool](https://exiftool.org) - checks the meta information
- [scalpel file recovery tool](https://www.kali.org/tools/scalpel/)
- [Steganography Checklist](https://stegonline.georgeom.net/checklist)
- [Stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve)
- [steghide](https://steghide.sourceforge.net/documentation.php)
- [foremost carving tool](https://linuxconfig.org/how-to-recover-deleted-files-with-foremost-on-linux)

- [binwalk tool](https://github.com/briankip/binwalk-tutorial)
- [PDF Tools](https://blog.didierstevens.com/programs/pdf-tools/)
- [pdf-parser](https://www.aldeid.com/wiki/Pdf-parser)
- [QPDF](https://github.com/qpdf/qpdf)
- [tail command](https://www.howtogeek.com/481766/how-to-use-the-tail-command-on-linux/) - shows data from the end of a file
- [P7zip](https://www.kali.org/tools/p7zip/)
- [strings command](https://www.howtogeek.com/427805/how-to-use-the-strings-command-on-linux/)
- [Free File Camouflage](https://www.addictivetips.com/windows-tips/hide-password-protect-your-files-in-images-with-free-file-camouflage/#:~:text=Free%20File%20Camouflage%20has%20two%20basic%20tabs%3A%20Camouflage,want%20to%20hide.%20Then%2C%20choose%20a%20JPEG%20image.) - hide and password protect files

### Miscellaneous

- [pwntools](https://github.com/Gallopsled/pwntools)
- [gitsanity](https://jaimelightfoot.com/blog/tuctfs-ready-player-one-challenges-hint-git-is-your-friend/)
- [Esoteric programming language](https://en.wikipedia.org/wiki/Esoteric_programming_language) - for language problems
- [Language Problem Example Write-up](https://medium.com/@naveenramesh915/sunshine-ctf-2019-write-ups-648b104d2893)
- [Cryptocurrency Writeup](https://blog.coinbase.com/capture-the-coin-blockchain-category-solutions-9aef880d7e00)
- [Reverse Image Search](https://tineye.com/)
	- [Google](https://support.google.com/websearch/answer/1325808?hl=en&co=GENIE.Platform%3DDesktop)
- [QR Codes](https://www.thonky.com/qr-code-tutorial/)
- [Cracking(fcrackzip)](https://www.geeksforgeeks.org/fcrackzip-tool-crack-a-zip-file-password-in-kali-linux/)

### Web Exploitation

**Basic Methodology**
Now, here's my basic methodology... It's over simplified for hard stuff, but is very useful for someone who is doing basic web things. 

Step 1: Open up Chrome Dev Tools

Step 2: Use the site as intended

Step 3: See what happens. 



While playing around, check out these basic tips for finding weirdness.



**Dummy Stuff**
- Find all login pages
  - Many bugs, however complicated their root cause might be, display themselves as a normal user having powers that were meant only for admin
  - Generally, anything that "admin" is the only group allowed to do that "user" has access to is considered bad. Test everything, attack admin functionality as a normally priv'd user.
  - If you see the word admin, you're probably on the right track.
  - Also, always try admin:admin on everything you touch.
  - As a near general rule, you will not bruteforce logins during CTFs, so don't do it without permission from organizers. If you are bruteforcing, you are likely wrong.

- Find all upload/content send mechanisms
- View source of pages
- Check out cookies (base 64/ plaintext)
  - The most common way sessions are maintained is with cookies.
  - Always check the cookies on a web page, either with a cookie editing tool or using browser DevTools
  - Cookies can be (Will be) encoded so don't be discouraged if they are random alphanumerics, always make sure to check Base64 and other common encodings.
- Look at URLs
  - If the URL looks like it has a number at the end, try incrementing the number.
  - If the URL has your username at the end, change the username.
- Look for Robots.txt

**Attack login pages**
- try baby SQL inject on each one
- try baby command inject on each one

**Attack input pages**
- try baby command inject on each one
- run an XSS scan

**Recon**
- Nmap -A
  - Services on weird ports are common
- Dirbust for 2 minutes if nothing against it.
  - Admin panels might pop up
- Vuln scan with Nikto. If you have a real commercial one, hit it, but you probably won't find anything. CTF challenges aren't supposed to be solved by a scanner.

Always remember to use cheatsheets: https://github.com/OWASP/CheatSheetSeries/tree/master/cheatsheets

 Fake it from there.


 - [Command Injection](https://ctf101.org/web-exploitation/command-injection/what-is-command-injection/)
 - [SQL Injection](https://ctf101.org/web-exploitation/sql-injection/what-is-sql-injection/)
 - [Directory Traversal](https://ctf101.org/web-exploitation/directory-traversal/what-is-directory-traversal/)
 - [Javascript for Hackers(aka XSS)Tutorial](https://www.hacker101.com/sessions/javascript_for_hackers)


