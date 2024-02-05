#!/bin/bash

#lee la variable 
read -p "Ingrese usuario de github" Lu1s16
Url = "https://api.github.com/users/$Lu1s16"

Respuesta=$(curl -s $Url)

github_user=$(echo $Respuesta | jq -r '.login')
id = $(echo $Respuesta | jq -r '.idt')
created_at=$(echo $Respuesta | jq -r '.created_at')

echo "Hola $github_user. User ID: $id. Cuenta fue creada el $created_at."

date = $(date + "%Y%m%d")

directorio = "/tmp/$date"
mkdir -p $directorio

archivo = "$directorio/saludos.log"
echo "Hola $github_user. User ID: $id. Cuenta fue creada el $created_at." > $archivo
echo "Mensaje guardado en: $archivo"
