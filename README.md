# Nmap Room - 10.10.49.33

## Task3 - nMap scanning
https://tryhackme.com/room/rpnmap


### 1. Let's go ahead and start with the basics and perform a syn scan on the box provided. What will this command be without the host IP address?
```
nmap -sS
```
### 2. After scanning this, how many ports do we find open under 1000?
```
2
```
### 3. What communication protocol is given for these ports following the port number?
```
tcp
```
### 4. Perform a service version detection scan, what is the version of the software running on port 22?
```
6.6.1p1
```
### 5. Perform an aggressive scan, what flag isn't set under the results for port 80?
```
httponly
```

### 6. Perform a script scan of vulnerabilities associated with this box, what denial of service (DOS) attack is this box susceptible to? Answer with the name for the vulnerability that is given as the section title in the scan output. A vuln scan can take a while to complete. In case you get stuck, the answer for this question has been provided in the hint, however, it's good to still run this scan and get used to using it as it can be invaluable. 

```
http-slowloris-check:
|   VULNERABLE:
|   Slowloris DOS attack
|     State: LIKELY VULNERABLE
|     IDs:  CVE:CVE-2007-6750
|       Slowloris tries to keep many connections to the target web server open and hold
|       them open as long as possible.  It accomplishes this by opening connections to
|       the target web server and sending a partial request. By doing so, it starves
|       the http server's resources causing Denial Of Service.
```

#### The command for vulnerabilityscanning with Nmaps built in script is
```
nmap -sV --script vuln [IP]
```
