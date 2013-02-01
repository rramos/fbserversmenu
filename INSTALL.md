
# INSTALL #
 - Just copy the script to a executable path ex:
   - $ cp fbserversmenu /usr/local/bin/
 - Wrapp sshm 
   - $ mv /usr/bin/sshm /usr/bin/sshm.bin
   - $ cp sshm /usr/bin/sshm
 - Add menu to FluxBox
   - vi ~/.fluxbox/menu

 [submenu] (Servers)
  [include] (~/.fluxbox/servers-menu)
 [end]

 - Done :)

