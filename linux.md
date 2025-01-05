# LINUX

## FILES

```bash
# list files and directories
ls
ls -la #incluir directorios ocultos

# change current directory
cd ../ #subir nivel
cd ./ #mismo nivel

# create new directory
mkdir 

# move or rename files or chage file or directory
mv /home/angeles/test /home/angeles/test_new

# remove files or directories
rm /home/angeles/test

# change file or directories permissions
rm /home/angeles/test

# copy files or directories
cp

# search for files or directories
find 

# search for  pattern in files
ls ./ | grep vboxguest

# display the content of files
cat 

# edit files using text editor
nano

```

## PERMISIONS AND USERS

```bash
# change file or directories permissions
chmod

sudo chown bigdata /discogrande
sudo chgrg bigdata /discogrande 

sudo chown -R user:grupo /ruta # Hacer los 2 comandos anteriores en 1

# crear usuario
sudo adduser nombre_usuario
sudo usermod -aG grupo nombre_usuario # añade el user a un grupo
sudo usermod -aG sudo nombre_usuario # añadir al usuario al grupo sudo

# verificar usuarios
cat /etc/passwd

```

## DOWNLOAD FILES

```bash
# download file
wget https://dlcdn.apache.org/hadoop/common/hadoop-3.4.1/hadoop-3.4.1.tar.gz 

# manipulate tarball archive files
sudo tar -xzvf hadoop-3.4.1.tar.gz -C /home/hadoop/hadoop 
```

## PROCESSES AND SERVICES

```bash
# display process information
ps 

# ver si hay algún servicio corriendo en ese puerto
sudo lsof -i :27017

# terminate process by sending a signal
sudo kill -9 1234  # Sustituye 1234 por el PID del proceso 

# display process and resource usage
top 

# estimate file space usage
du 

```

## REDES

```bash
# nos dice las interfaces
ip a

# ver puerta de enlace
ip r

# comprobar conexion
ping -c 4 10.0.2.1

# configuración red
sudo nano /etc/netplan/00-installer-config.yaml
sudo netplan try
```

## DISK AND SPACE

```bash
# espacio en discos montados
df -h

# memoria del sistema
free -h
```

## MAQUINA

```bash
# nombre de la máquina
/etc/hostname

# asociaciones locales ip - maquinas
nano /etc/hosts

# apagar máquina

# reiniciar máquina
sudo reboot

# fichero variables de entorno ámbito global
/etc/environment

# montar
sudo mount /dev/sdb1 /home/hadoop/discogrande

```
