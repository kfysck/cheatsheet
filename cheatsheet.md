Nmap
sudo nmap -sV {IP}
sudo nmap -sT 10.129.107.120 -top-ports 1000 -d
sudo nmap -p- --min-rate=1000 -sV {IP}  #all ports range, or specific ports, min-rate specific min send packets per sec.

Telnet
telnet open {IP}

FTP
ftp anonymous@{IP}
Press Entry button if password is null

SMB
smbclient -L {IP}
smbclient \\\\{IP}\\{DIR}

Redis
info # see all info
info server # see server info
select {db}
keys *
dbsize

RDP
xfreerdp3 /v:{HOST} /u:{USERNAME}

WEB
wordlist
https://raw.githubusercontent.com/danielmiessler/SecLists/master/Discovery/Web-Content/common.txt
gobuster
gobuster dir -u 10.129.70.58 -w wordlist.txt

MongoDB
curl -O https://downloads.mongodb.com/compass/mongosh-2.3.2-linux-x64.tgz
./mongosh mongodb://{IP}:{PORT}
show dbs;
show tables;
db.{TALBENAME}.find().pretty()

Rsync
default port 873
rsync --list-only {IP}::public
rsync {IP}::public/flag.txt flag.txt
