Requisito

- La contraseña del nuevo certificado debe ser el mismo que del keystore (changeit)

Generar full.pem con el siguiente orden:

1. Private key
2. Certificate
3. Certificate chain

Generar public.pem con el siguiente orden:

1. Certificate
2. Certificate chain

Para confirmar contraseña y orden del keystore

```
cd /home/user-ec2/IBM/IBMControlCenter64/Install/jre/bin
./keytool -list -v -keystore /home/user-ec2/IBM/IBMControlCenter64/certificados-privados/keystore.jks
```

Subir el certificado full.pem en keystore del Control Center

<img width="921" height="452" alt="image" src="https://github.com/user-attachments/assets/e1bd6aac-105e-40d3-b43f-2389e919093f" />


Cargar certificado public.pem en el connect:direct (trusted store)
Nota: No importa la etiqueta del certificado en el trusted



Reiniciar Control Center
```
cd /home/user-ec2/IBM/IBMControlCenter64/Install/bin
./StopEngine.sh -np
./RunEngine.sh
```



# Actualizar certificado en Web Service

Validar password keystore (en este caso en blanco)
```
cd /home/user-ec2/xxxx/jre/bin
./keytool -list -v -keystore /home/user-ec2/IBM/IBMControlCenter64/certificados-privados/keystore.jks
```

Generar certificados para el WebService

Generar full.pem con el siguiente orden:

1. Private key
2. Certificate
3. Certificate chain

Generar public.pem con el siguiente orden:

1. Certificate
2. Certificate chain

Cargar la public.pem en el secure+ del nodo connect:direct

Eliminar el certificado anterior
<img width="1529" height="328" alt="image" src="https://github.com/user-attachments/assets/540c1638-a439-4d4b-8caf-494c00f2fa74" />

Cargar el full.pem en el admin del WebService con el mismo label y eliminar el certificado CA (Lima)



