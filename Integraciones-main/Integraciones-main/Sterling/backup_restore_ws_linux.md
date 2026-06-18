# Backup/restore connect:direct

Sacar backup de los siguiente archivos en el servidor inicial

```
/IBM/CDWS6408/mftws/BOOT-INF/classes/ssl-server.jks
/IBM/CDWS6408/mftws/BOOT-INF/classes/trustedkeystore.jks
/IBM/CDWS6408/JSONFileSystem/AdminNodeDetails.json
/IBM/CDWS6408/JSONFileSystem/AdminPasswordEntity.json
```

Realizar la instalación de C:D y luego reemplazar los archivos, mantener el nombre del C:D.

```
Ruta del C:D: /IBM/CD6405
Ruta del instalador: /IBM/Instaladores/cdunix
```

Anotar la ruta de los siguientes archivos a reeemplazar
```
/IBM/CD6405/ndm/cfg/CDTAVO/initparm.cfg
/IBM/CD6405/ndm/cfg/CDTAVO/netmap.cfg
/IBM/CD6405/ndm/cfg/CDTAVO/userfile.cfg
```
<img width="660" height="404" alt="image" src="https://github.com/user-attachments/assets/ad384ecd-4c76-44a3-a9af-4a709a095e40" />

> [!IMPORTANT]
> ***Modificar y/o validar las rutas, ips y usuarios en los archivos de configuración***


Luego iniciar y validar el C:D

```
/IBM/CD6405/ndm/bin/cdpmgr -i /IBM/CD6405/ndm/cfg/CDTAVO/initparm.cfg
NDMAPICFG=/IBM/CD6405/ndm/cfg/cliapi/ndmapi.cfg
export NDMAPICFG
/IBM/CD6405/ndm/bin/./direct
select statistics;
quit;
```

<img width="750" height="746" alt="image" src="https://github.com/user-attachments/assets/4a1a30b8-c21f-4cd0-90e7-2560ce02b154" />

