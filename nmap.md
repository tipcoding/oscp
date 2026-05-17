```
IP="10.129.227.181"
nmap -sC -sV $IP -oN nmap.txt
nmap -p- -sS -T4 --open $IP -oN qFports.txt
sudo nmap -sU -p- -Pn --min-rate 10000 -oA alludp $IP
```

nmap -p- --min-rate 4000 192.168.175.61 

Tiep theo:

- Then on the open ports run: `nmap -sV --version-intensity 2 -O -Pn -T4 -p <ports> target`

nmap -sV --version-intensity 2 -O -Pn -T4 -p 2112 192.168.173.101

- Or run selected NSE scripts only: `-script=http-enum,ssl-cert` (instead of all default scripts).

nmap -p- -sC -sV 192.168.191.74 ⇒ scan all ports (very slow)

nmap -p- -A 192.168.219.94 (OK)
nmap -p- -A 192.168.152.10 -Pn -sT  -v  --open -T 4 -oN nmap.txt

I normally break down the scan into two parts, a general catch all scan on all TCP ports (using the `-p-` flag) and then an aggressive (`-A`) pin-pointed scan.
