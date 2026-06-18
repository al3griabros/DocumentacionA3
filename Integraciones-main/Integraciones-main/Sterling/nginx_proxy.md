# Configurar nginx proxy para C:D WebService por puerto 443

> [!NOTE]
> **Aplica para laboratorio TechZone donde solo esta expuesto el puerto 443**

Instalar nginx
```
sudo dnf install nginx nginx-mod-stream vim -y
```

Editar nginx.conf y borrar todo con **"dd"**
```
sudo vim /etc/nginx/nginx.conf
```

Reemplazar por completo con lo siguiente (guardar con **:wq**)
```
user nginx;
worker_processes auto;
error_log /var/log/nginx/error.log;
pid /run/nginx.pid;

# Carga de módulos dinámicos (necesario para el bloque stream)
include /usr/share/nginx/modules/*.conf;

events {
    worker_connections 1024;
}

# SOLUCIÓN: Passthrough puro de SSL (Capa 4)
# Nginx no te pedirá certificados aquí; delegará todo al puerto 9443
stream {
    server {
        listen     443;
        proxy_pass 127.0.0.1:9443;
    }
}

http {
    log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
                      '$status $body_bytes_sent "$http_referer" '
                      '"$http_user_agent" "$http_x_forwarded_for"';

    access_log  /var/log/nginx/access.log  main;

    sendfile            on;
    tcp_nopush          on;
    tcp_nodelay         on;
    keepalive_timeout   65;
    types_hash_max_size 4096;

    include             /etc/nginx/mime.types;
    default_type        application/octet-stream;

    include /etc/nginx/conf.d/*.conf;
}
```

Validar y reiniciar nginx
```
sudo nginx -t
sudo systemctl restart nginx
```

Ingresar sin el puerto 9443, registrar en el archivo hosts previamente. Por ejemplo:

https://itzvsi3-f5dtdopj/cdws-ui/index.html

<img width="1723" height="537" alt="image" src="https://github.com/user-attachments/assets/c6f4e400-f68b-4266-a2a0-f43cd57f8893" />

