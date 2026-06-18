# Instalación de WebService

Descargar instalador desde el Fix Central - IBM_CDWebServices_V_6.4.0.8_Redhat_x64

cd /IBM/Instaladores
tar -zxvf IBM_CDWebServices_V_6.4.0.8_Redhat_x64.tar.gz

Ejecutar:
./MFTWebServicesInstall.sh

Ruta del WS: /IBM/CDWS6408

<img width="810" height="562" alt="image" src="https://github.com/user-attachments/assets/438e2c2e-d58d-41a6-8ba6-dd1847e858d8" />

<img width="806" height="213" alt="image" src="https://github.com/user-attachments/assets/64bb68c6-8856-465a-b9b7-522d49c53561" />

<img width="801" height="459" alt="image" src="https://github.com/user-attachments/assets/3e96c3b2-1c84-4d0f-9aa1-3b0a39f8e921" />

<img width="801" height="122" alt="image" src="https://github.com/user-attachments/assets/4b6aa9e7-9ddf-44b8-964f-29812ba047e1" />

Colocar password keystore/truststore: Mainsoft.123

<img width="808" height="740" alt="image" src="https://github.com/user-attachments/assets/a046038e-a825-4f0b-a6c9-ef11bed7d989" />

<img width="800" height="378" alt="image" src="https://github.com/user-attachments/assets/32df6f3f-af23-4f77-b1af-9a5d5a113241" />


Certificado: labcertmainsoft

<img width="803" height="141" alt="image" src="https://github.com/user-attachments/assets/670c57bb-1b6d-4f52-a8e8-01fc8fc4387b" />

Presionar "Enter" hasta llegar a la siguiente parte:

<img width="800" height="438" alt="image" src="https://github.com/user-attachments/assets/8e7be1a3-5593-4835-a420-aef0c072c233" />

Indicar ruta donde se guardara el certificado publico del WebService, /IBM/CDWS6408

<img width="798" height="240" alt="image" src="https://github.com/user-attachments/assets/4b69406a-4c60-497b-822d-e4090e82d76a" />

<img width="803" height="242" alt="image" src="https://github.com/user-attachments/assets/863dccec-b1b4-40ba-abd0-148f0fe49db1" />

Dejar en blanco

<img width="810" height="240" alt="image" src="https://github.com/user-attachments/assets/43ac8519-13f6-4d8b-b9e8-5c29134910fa" />

<img width="803" height="277" alt="image" src="https://github.com/user-attachments/assets/e09087a9-16a5-45fe-aee9-66fcbdae4279" />

Ingresar a la web

```
ConnectDirectWebservices User Interface is available at  :
https://itzvsi0-elj6a9rj:9443/cdws-ui/index.html
ConnectDirectWebservices API reference is available at  :
https://itzvsi0-elj6a9rj:9443/cdws-doc/signOn.html
```

**CDWS Admin Login**
Usuario: admin

Password: admin (defecto)

Nuevo Password: Mainsoft123!

Agregar nodo a administrar CDTAVO

**C:D User Login**

Ingresar al nodo

User: U85FJEK o itzuser

Password: Mainsoft.123

# Reinicio de servicio

```
/IBM/CDWS6408/bin/stopWebservice.sh
/IBM/CDWS6408/bin/startWebservice.sh
```

<img width="688" height="102" alt="image" src="https://github.com/user-attachments/assets/e381ef7d-71d6-495d-8561-90d4c69277e4" />

# Validación

```
sudo dnf install net-tools -y
netstat -ntpl
```

<img width="1012" height="226" alt="image" src="https://github.com/user-attachments/assets/dbe60f2c-0cb1-4f07-82b8-3a99981b420d" />

