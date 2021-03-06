# DNSathon 2017 #

The 1st DNS Hackathon was held November 23-24, 2017 as part of Benin DNS Forum activities in Cotonou, BJ. 

In each subdirectory contains the materials submitted and archived by the participants organized by team name.

## Infrastructure ##

### Network ###
We have used two Cisco-XXXX swicthes and one Mikrotik-XXX as router. Patch cable has been used to connect all components: Raspberry-pi, team member laptop, switches and routers. 

#### Transit ####
International connectivity has been assured by our gold sponsor SudTelecom.

#### Servers #####
We use Raspberry-Pi 3-XX as server. For each server, we assign IP based on following IP adressing plan:


| Id | Role | # | Hostname | IP | GW | Vlan | Resolvers |
| ----- | --- | ----- | --- | ---- | --- | -- | --- |
| 1 | **Root** | 1 | `pi-root` | 192.168.10.10/24 | 192.168.10.1 | 10 | 192.168.40.10 & 192.168.40.20 |
| 2 | **Registry** | 1 | `pi-registry-1` | 192.168.20.10/24 | 192.168.20.1 | 20 | 192.168.40.10 & 192.168.40.20 |
| 3 | **Registry** | 2 | `pi-registry-2` | 192.168.20.20/24 | 192.168.20.1 | 20 | 192.168.40.10 & 192.168.40.20 |
| 4 | **Registrar** | 1 | `pi-registrar-1` | 192.168.30.10/24 | 192.168.30.1 | 30 | 192.168.40.10 & 192.168.40.20 |
| 5 | **Registrar** | 2 | `pi-registrar-2` | 192.168.30.20/24 | 192.168.30.1 | 30 | 192.168.40.10 & 192.168.40.20 |
| 6 | **Resolver** | 1 | `pi-resolver-1` | 192.168.40.10/24 | 192.168.40.1 | 40 | 127.0.0.1 |
| 7 | **Resolver** | 2 | `pi-resolver-2` | 192.168.40.20/24 | 192.168.40.1 | 40 | 127.0.0.1 |


#### Design ####
In a nutshell, we have setup following network design
![Infrastructure Overview](https://raw.githubusercontent.com/AlfredArouna/DNSathon/master/2017/bdf_hackathon.jpg)



### Servers ###

#### Materials ####

#### Services ####


## Teams ##

### Root ####

### Registry ###

### Registrars ###

### ISP (Resolvers) ###

### Communication ###


## Support & Logistiq ##
* Mr. Yaovi Atohoun
* Mr. Carl Aniambossou, DC & Ms. (from SudTelecom)
* Hotel ?
* Yazid 
* Jeremy
* Ramanou
* Alfred
