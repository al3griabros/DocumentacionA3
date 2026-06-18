# Instalar Connect:Direct en Linux

Descargar instalador dede Fix central (https://www.ibm.com/support/fixcentral)

<img width="550" height="334" alt="image" src="https://github.com/user-attachments/assets/00fb5e04-b3f4-4e23-a030-2d61f2760cf7" />

<img width="535" height="544" alt="image" src="https://github.com/user-attachments/assets/955585a3-eb75-49d8-9e2e-26589fc61e82" />

<img width="1059" height="570" alt="image" src="https://github.com/user-attachments/assets/fee0abc6-1e55-4fe6-8f82-61c1446f921d" />

<img width="795" height="433" alt="image" src="https://github.com/user-attachments/assets/cec82603-b75e-4452-bbcb-4743e4b40810" />

Contar con usuario de servicio por privilegios sudo
```
sudo useradd cduser
sudo passwd cduser //Password: Mainsoft.123
sudo usermod -aG wheel cduser
su - cduser
sudo whoami
```

Desde el usuario cduser, crear carpeta para subir los instaladores y carpeta donde se instalará el Connect:Direct

```
mkdir -p ./IBM/Instaladores
mkdir -p ./IBM/CD6405
```

Subir el instalador en ./IBM/Instaladores

<img width="1131" height="64" alt="image" src="https://github.com/user-attachments/assets/41df31b5-5a57-40b9-8749-924477271de5" />

Descomprimir instalador
```
tar -xvf 6.4.0.5-IBMSterlingConnectDirectforUNIX-Linux-x86-iFix019.tar
```

<img width="1133" height="200" alt="image" src="https://github.com/user-attachments/assets/173bf003-adc7-40e2-b630-8959c577c2e0" />

Anotar la ruta del instalador
```
/home/cduser/IBM/Instaladores/cdunix
```

Anotar ruta donde se instalara el Connect:Direct
```
/home/cduser/IBM/CD6405
```

Instalar C:D
```
cd /home/cduser/IBM/Instaladores/
./cdinstall
```

<img width="678" height="69" alt="image" src="https://github.com/user-attachments/assets/760c7635-c9e8-41bb-b20b-7e55cd0dc014" />

<img width="476" height="223" alt="image" src="https://github.com/user-attachments/assets/ee495aad-5fac-4234-b858-faa28dcf1913" />

<img width="673" height="53" alt="image" src="https://github.com/user-attachments/assets/6f550a87-1d9d-4eb6-b248-980f1026a82c" />

<img width="581" height="41" alt="image" src="https://github.com/user-attachments/assets/cd809d52-5ab2-4f13-baff-46e8e0879b52" />

Esperar a que termine, luego de unos segundos se mostrará:

<img width="519" height="178" alt="image" src="https://github.com/user-attachments/assets/83266ca1-3fa9-4a03-94c9-6359d5690780" />

Definir nombre del C:D

<img width="587" height="116" alt="image" src="https://github.com/user-attachments/assets/611c9ea9-7a29-4722-b170-9de762c2b585" />

En caso no se tenga Control Center Director, no es necesario instalar el agente del CCD

<img width="598" height="65" alt="image" src="https://github.com/user-attachments/assets/9e57efb8-c516-4f3e-a2f7-731d00f2785c" />

Configurar los puertos para la transferencia (1364) y el cliente (1363)

<img width="771" height="786" alt="image" src="https://github.com/user-attachments/assets/1fe4b37e-5b3f-4f43-aa64-c25faff28db8" />

Anotar las rutas del paso anterior:
```
/home/cduser/IBM/CD6405/ndm/cfg/CDLINUX/initparm.cfg
/home/cduser/IBM/CD6405/ndm/cfg/CDLINUX/netmap.cfg
/home/cduser/IBM/CD6405/ndm/cfg/CDLINUX/userfile.cfg.
```
Agregar usuario remoto, por ejemplo cduser de otro CDWINDOWS. Agregar usuario local, ej. cduser

<img width="400" height="263" alt="image" src="https://github.com/user-attachments/assets/f1109fb1-7ddc-4dc5-95b1-6095bc68ed0b" />

Luego enter y enter

Configurar privilegos root (root/Mainsoft.123)

<img width="531" height="177" alt="image" src="https://github.com/user-attachments/assets/e62a989d-811d-46e4-827a-36b09f5970e7" />

<img width="461" height="91" alt="image" src="https://github.com/user-attachments/assets/6c711f53-9d9a-4d3d-8a4e-e8ecdc5cac27" />

<img width="831" height="81" alt="image" src="https://github.com/user-attachments/assets/6d4dca15-43e5-4de9-9326-a2da77e15c29" />

<img width="550" height="246" alt="image" src="https://github.com/user-attachments/assets/fb0eb7f7-c7d0-4cfa-993c-4236332e59c4" />

<img width="939" height="259" alt="image" src="https://github.com/user-attachments/assets/a63a9b75-da7d-4096-9a43-3d79070e599a" />

Regresar al menú principal

<img width="506" height="176" alt="image" src="https://github.com/user-attachments/assets/dc14dd8e-860e-420e-9248-d445a1a15af3" />

<img width="520" height="76" alt="image" src="https://github.com/user-attachments/assets/dd25a2e3-3c94-4eda-bae2-314454793935" />

Instalar File Agent (implica también el Secure+)

<img width="473" height="217" alt="image" src="https://github.com/user-attachments/assets/2d85177e-8f56-472a-b9f0-b099d16988c5" />

<img width="431" height="84" alt="image" src="https://github.com/user-attachments/assets/d199fb02-7227-4ef6-afe1-6cb0125152f6" />

<img width="413" height="48" alt="image" src="https://github.com/user-attachments/assets/a86c4f51-26ae-4142-94cf-3b3cd5018172" />

<img width="632" height="59" alt="image" src="https://github.com/user-attachments/assets/aedc7d7f-593c-4d6d-9264-fc0f7f07356e" />

Password keystore: Mainsoft.123

<img width="343" height="98" alt="image" src="https://github.com/user-attachments/assets/460952fe-3078-4268-b9c5-1e6b439b766b" />

<img width="945" height="349" alt="image" src="https://github.com/user-attachments/assets/8d101f06-f63c-4e7d-81bc-f4d0512f76c8" />

Iniciar Connect:Direct
```
/home/cduser/IBM/CD6405/ndm/bin/cdpmgr -i /home/cduser/IBM/CD6405/ndm/cfg/CDLINUX/initparm.cfg
```
<img width="1206" height="61" alt="image" src="https://github.com/user-attachments/assets/a30d84b9-d697-4afc-b498-e626a64be199" />


Validar que este corriendo
```
netstat -na | grep 1364
ps -fea | grep CD6405
```
<img width="1479" height="123" alt="image" src="https://github.com/user-attachments/assets/9c185454-d637-4b3a-a82a-279bbea2e5e5" />


```
NDMAPICFG=/home/cduser/IBM/CD6405/ndm/cfg/cliapi/ndmapi.cfg
export NDMAPICFG
/home/cduser/IBM/CD6405/ndm/bin/./direct
select statistics;
quit;
```

Agregar los datos de los otros C:D
/IBM/CD6405/ndm/cfg/CDTAVO/netmap.cfg
/IBM/CD6405/ndm/cfg/CDTAVO/userfile.cfg


crear archivo envio.cd (chmod 755)
###############################################
ENVIO PROCESS
SNODE=CDWILBERT
CLASS=1
PRTY=1
HOLD=No
CRC=ON

COPIA COPY
FROM (
FILE="/IBM/ARCHIVO.EXT"
PNODE
SYSOPTS="DATATYPE(BINARY)"
)
TO (
FILE="/IBM/ARCHIVOFINAL.EXT"
SNODE
disp=rpl
SYSOPTS="DATATYPE(BINARY)"
)

BORRADO IF (COPIA EQ 0) THEN

RUN TASK PNODE
SYSOPTS="rm /IBM/ARCHIVO.EXT"
EIF
PEND;

###############################################

submit file=/IBM/envio.cd;

select statistics detail=yes pnumber=2;

Desinstalar

sudo /IBM/CD6405/ndm/bin/uninstall

Para deshabilitar el secure+

NDMAPICFG=/IBM/CD6405/ndm/cfg/cliapi/ndmapi.cfg
export NDMAPICFG
/IBM/CD6405/ndm/bin/./spcli.sh
display all;
update Localnode Protocol=Disable; 
update Client Protocol=Disable;

