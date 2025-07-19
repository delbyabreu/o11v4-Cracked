# o11v4 - Cracked

Probado en **Ubuntu 20-23**

## Prerrequisitos

### 1. Crear el directorio requerido
Ejecute el siguiente comando para crear el directorio necesario:
```sh
mkdir -p /home/o11
cd /home/o11
```
### 2. Instalar Nodejs/NPM

Ejecute el siguiente comando para instalar el software necesario si desea utilizar nodejs:
```sh
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
npm install -g pm2
npm install express
```
## Configuración e inicio del proxy del servidor de licencias

Abra el archivo del servidor y agregue la dirección IP de su servidor a la variable ipAddress, luego guarde

Ejecute los siguientes comandos para configurar e iniciar el servidor de licencias:
```sh
## if using nodejs
pm2 start server.js --name licserver --silent

## if using python
pm2 start server.py --name licserver --interpreter python3

then

pm2 startup
pm2 save

nohup ./run.sh > /dev/null 2>&1 &
```
