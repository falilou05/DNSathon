# Custom DNS root (for internal purpose)

## Tools ##
bind9, bind9utils, libbind9-140

## Configurations ##
1)we edit the file"/etc/hostname" and change the old hostname to "racine" 
2) go to the directory "/etc/bind"
3)edit the file "named.conf.default-zones"
and put that following lines:

zone "racine."{
        type master;
        file "/etc/bind/db.racine";
};

4)Edit the file"/etc/bind/db.racine" and add that following line:
$TTL	604800
.	IN	SOA	racine. ns1.racine. (
			      2		; Serial
			 604800		; Refresh
			  86400		; Retry
			2419200		; Expire
			 604800 )	; Negative Cache TTL
;
.				IN	NS	 ns1.racine.
.				IN	A	   192.168.10.10

5)Replace the root hint file"/etc/bind/db.root" on our own new parameter
;       This file holds the information on root name servers needed to
;       initialize cache of Internet domain name servers
;       (e.g. reference this file in the "cache  .  <file>"
;       configuration file of BIND domain name servers).
;
;       This file is made available by InterNIC 
;       under anonymous FTP as
;           file                /domain/named.cache
;           on server           FTP.INTERNIC.NET
;       -OR-                    RS.INTERNIC.NET
;
;       last update:    February 17, 2016
;       related version of root zone:   2016021701
;
; formerly NS.INTERNIC.NET
;
.                        3600000      NS    racine.
racine.     		 3600000      A     192.168.10.10

; End of file



