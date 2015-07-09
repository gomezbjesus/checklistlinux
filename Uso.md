# Uso de la aplicación #

Uso: checklist-linux.pl opciones

- La ejecución de la aplicación corre bajo su propia responsabilidad y debe ser en un ambiente controlado.

opciones Analisis que vamos a ejecutar

> --usuariodefault Analizamos que los usuarios default del SO. no estan creados

> --permisosAD Analizamos los permisos de los archivos/directorios criticos

> --suidguidsticky Analizamos permisos especiales en todo el sistema

> --sinownergroup Buscamos en el sistema archivos/directorios sin owner

> --writeparatodos Buscamos en el sistema archivos/directorios con escritura

> --syslog Verificamos que este configurado un syslog externo

> --usuariosgrupos Asociamos los usuarios del sistema a sus respectivos grupos

> --expiracionUsuarios Verificamos las variables de expiracion de las cuentas de usuarios

> --seguridadnet Verificamos las variables de expiracion de las cuentas de usuarios

> --seguridadssh Verificamos las variables del servicio sshd

> --todos Ejecutamos todos los analisis


## --usuariodefault ##
situ@tux ~/ $ perl checklist-linux.pl --usuariodefault

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Verificacion de usuarios default

---

Negativo: El usuario lp existe

Negativo: El usuario uucp existe

Negativo: El usuario games existe


## --permisosAD ##
situ@tux ~/ $ perl checklist-linux.pl --permisosAD

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Verificar permisos en archivos y directorios

---

Negativo: El archivo /bin/ tiene como permiso 0755

Negativo: El archivo /boot/ tiene como permiso 0755

Negativo: El archivo /etc/ tiene como permiso 0755

Negativo: El archivo /etc/cron.daily/ tiene como permiso 0755

Negativo: El archivo /etc/cron.hourly/ tiene como permiso 0755

Negativo: El archivo /etc/cron.weekly/ tiene como permiso 0755

No existe El archivo /etc/exports no existe en el sistema o no puede ser accedido

No existe El archivo /etc/inittab no existe en el sistema o no puede ser accedido

Negativo: El archivo /etc/motd tiene como permiso 0666

No existe El archivo /etc/syslog.conf no existe en el sistema o no puede ser accedido

Negativo: El archivo /home/ tiene como permiso 0755

Negativo: El archivo /lib/ tiene como permiso 0755

Negativo: El archivo /mnt/ tiene como permiso 0755

No leible El archivo /root/ no puede ser leido

Negativo: El archivo /root/ tiene como permiso 0700

Negativo: El archivo /sbin/ tiene como permiso 0755

Negativo: El archivo /tmp/ tiene como permiso 1777

Negativo: El archivo /usr/ tiene como permiso 0755

Negativo: El archivo /usr/bin/ tiene como permiso 0755

Negativo: El archivo /var/ tiene como permiso 0755



## --suidguidsticky ##
situ@tux ~/ $ perl checklist-linux.pl --suidguidsticky

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Verificacion de Suid Bit / Guid Bit / Sticky Bit

---

Informacion: Se detecto suid/gsid en /srv/cvs

Informacion: Se detecto suid/gsid en /srv/cvs/CVSROOT

Informacion: Se detecto suid/gsid en /srv/cvs/CVSROOT/Emptydir

Informacion: Se detecto suid/gsid en /bin/ping6

Informacion: Se detecto suid/gsid en /bin/umount

Informacion: Se detecto suid/gsid en /bin/su

Informacion: Se detecto suid/gsid en /bin/mount

Informacion: Se detecto suid/gsid en /bin/ping

Informacion: Se detecto suid/gsid en /bin/fusermount

Informacion: Se detecto sticky bit en /var/spool/samba

Informacion: Se detecto sticky bit en /var/spool/cups/tmp

Informacion: Se detecto sticky bit en /var/spool/cups-pdf/ANONYMOUS

Informacion: Se detecto sticky bit en /var/spool/cron/atspool

Informacion: Se detecto sticky bit en /var/spool/cron/crontabs

Informacion: Se detecto sticky bit en /var/spool/cron/atjobs

Informacion: Se detecto sticky bit en /var/spool/postfix/maildrop

Informacion: Se detecto suid/gsid en /var/spool/postfix/public

Informacion: Se detecto sticky bit en /var/crash

Informacion: Se detecto sticky bit en /var/log/gdm

Informacion: Se detecto suid/gsid en /var/log/exim4

Informacion: Se detecto suid/gsid en /var/log/nagios3

Informacion: Se detecto suid/gsid en /var/log/nagios3/archives

Informacion: Se detecto suid/gsid en /var/log/mysql

## --sinownergroup ##
situ@tux ~/ $ perl checklist-linux.pl --sinownergroup

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Archivos sin owner y group

---

Negativo: Archivo sin owner/group /usr/lib/gtk-2.0/2.10.0/engines/libaurora.so

Negativo: Archivo sin owner/group /usr/share/themes/Aurora

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/menu\_prelight.png

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/maximize\_prelight.png

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/restore.png

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/minimize\_prelight.png

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/metacity-theme-2.xml

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/menu\_small.png

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/metacity-theme-2.xml~

Negativo: Archivo sin owner/group /usr/share/themes/Aurora/metacity-1/close.png


## --writeparatodos ##
situ@tux ~/ $ perl checklist-linux.pl --writeparatodos

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Verificar Archivos con write para todos los usuarios

---

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/180.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/32.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/74.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/45.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/166.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/103.gif

Negativo: Archivo con write para todos los usuarios /var/www/monitoreo/cimg/50.gif

## --syslog ##
situ@tux ~/ $ perl checklist-linux.pl --syslog

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Eventos mediante Syslog - AUTHPRIV

---

No existe El archivo /etc/syslog.conf no existe en el sistema o no puede ser accedido

## --usuariosgrupos ##
situ@tux ~/ $ perl checklist-linux.pl --usuariosgrupos

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Comprobacion de Usuarios/Grupos

---

Informacion: El usuario www-data pertenece al grupo www-data (33)

Informacion: El usuario postfix pertenece al grupo postfix (126)

Informacion: El usuario messagebus pertenece al grupo messagebus (106)

Informacion: El usuario lp pertenece al grupo lp (7)

Informacion: El usuario bin pertenece al grupo bin (2)

Informacion: El usuario nagios pertenece al grupo nagios (128)

Informacion: El usuario daemon pertenece al grupo daemon (1)

## --expiracionUsuarios ##
situ@tux ~/ $ perl checklist-linux.pl --expiracionUsuarios

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Variables de expiracion de cuentas de usuarios

---

Negativo: El valor del parametro PASS\_MAX\_DAYS es incorrecto: 99999 != 90

Negativo: El valor del parametro PASS\_MIN\_DAYS es incorrecto: 0 != 7

Negativo: El valor del parametro PASS\_WARN\_AGE es incorrecto: 7 != 28

## --seguridadnet ##
situ@tux ~/ $ perl checklist-linux.pl --seguridadnet

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Variables de seguridad en la red

---

No existe el parametro net.ipv4.conf.all.accept\_redirects= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.all.accept\_source\_route0 en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.all.rp\_filter= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.all.secure\_redirects= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.default.accept\_redirects= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.default.accept\_source\_route= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.default.rp\_filter= en /etc/sysctl.conf

No existe el parametro net.ipv4.conf.default.secure\_redirects= en /etc/sysctl.conf

No existe el parametro net.ipv4.icmp\_echo\_ignore\_broadcasts= en /etc/sysctl.conf

No existe el parametro net.ipv4.tcp\_max\_syn\_backlog= en /etc/sysctl.conf

Positivo: El valor del parametro net.ipv4.tcp\_syncookies= es correcto

## --seguridadssh ##
situ@tux ~/ $ perl checklist-linux.pl --seguridadssh

---

Sistema Operativo: Linux

Release del Kernel: 2.6.31-21-generic

Hostname: tux

Datos Adicionales: Linux tux 2.6.31-21-generic #59-Ubuntu SMP Wed Mar 24 07:28:56 UTC 2010 i686 GNU/Linux

---

> -- Variables de seguridad en el servicio ssh

---

Negativo: El valor del parametro PermitRootLogin es incorrecto: yes != no

Positivo: El valor del parametro Protocol es correcto

Positivo: El valor del parametro UsePrivilegeSeparation es correcto


![http://artsweb.com.ar/terminal.png](http://artsweb.com.ar/terminal.png)

![http://artsweb.com.ar/browser.png](http://artsweb.com.ar/browser.png)