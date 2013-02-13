# fbserversmenu  

Dynamic Servers Menu generator for FluxBox

## Description ##
fbserversmenu is set of script files for generating dynamic menus for FluxBox, in conjunction with sshm for rapid SSH/RDP connetions.

## Requirements ##
 - Perl
 
## Instalation ##
 - For install options follow read INSTALL file.

## Using ##
  Current version parses user ~/.sshm file and generates FluxBox Menus according to the following syntax.

```
     Level1_Level2_Level3_server	user	IP	PORT
```
  Ex:
```
    org_servicex_prod_server1	user	192.168.1.1	22
    org_servicex_prod_server2	user	192.168.1.2	22
    org_servicex_dev_server3	user	192.168.1.3	22
    org_servicey_server4	user	192.168.1.4	22
```
 Would result in the following menu:

```
 [submenu] (ORG)
   [submenu] (SERVICEX)
    [submenu] (PROD)
      [exec] (server1) { $terminal -e 'ssh -p 22 user@192.168.1.1}
      [exec] (server2) { $terminal -e 'ssh -p 22 user@192.168.1.2}
    [end] 
    [submenu] (DEV)
      [exec] (server3) { $terminal -e 'ssh -p 22 user@192.168.1.3}
    [end]
   [end]
   [submenu] (SERVICEY)
     [exec] (server4) { $terminal -e 'ssh -p 22 root@193.137.35.171}
   [end]
 [end]
```






