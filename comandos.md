1. Crear un script

sudo nano /usr/local/bin/actividad3.sh

2. Codigo del script

#!/bin/bash

while true
do
    echo "Hola, la fecha actual es: $(date)"
    sleep 1
done

3. Dar permisos al script

sudo chmod +x /usr/local/bin/actividad3.sh

4. Crear un archivo systemd

sudo nano /etc/systemd/system/actividad_servicio.service

5. Crear el servicio

[Unit]
Description=Servicio de saludo

[Service]
ExecStart=/usr/local/bin/actividad3.sh
Restart=always
User=luis

6. Actualizar los servicios

sudo systemctl daemon-reload  

7. Iniciar el servicio

sudo systemctl start actividad_servicio.service

8. Validar que el servicio se esta ejecutando

sudo systemctl status actividad_servicio.service