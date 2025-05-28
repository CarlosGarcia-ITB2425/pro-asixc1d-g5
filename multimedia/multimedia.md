
# 🎧 Guía para Transmitir Audio y Video con Icecast2, DarkIce y FFmpeg en Linux

## 🛠️ Instalación de herramientas necesarias

```bash
uname -r
```
- Muestra la versión actual del kernel de Linux.

```bash
sudo apt update
```
- Actualiza la lista de paquetes disponibles desde los repositorios.

```bash
sudo apt install -y [paquetes]
```
- Instala programas útiles como:
  - Icecast2 (servidor de streaming)
  - DarkIce (codificador de audio)
  - Herramientas de red y seguridad

## ⚙️ Configuración de Icecast2

```bash
sudo nano /etc/icecast2/icecast.xml
```
- Abre el archivo principal de configuración de Icecast2.

```bash
sudo nano /etc/default/icecast2
```
- Ajusta los parámetros de inicio del servicio Icecast2.

```bash
sudo systemctl restart icecast2
```
- Reinicia el servicio Icecast2.

```bash
sudo systemctl enable icecast2
```
- Hace que el servicio inicie automáticamente al arrancar el sistema.

```bash
sudo systemctl status icecast2
```
- Verifica el estado actual del servicio.

## 🔒 Configuración del firewall (UFW)

```bash
sudo ufw allow 8000/tcp
```
- Abre el puerto 8000 para streaming de Icecast2.

```bash
sudo ufw allow 22/tcp
```
- Abre el puerto 22 para conexiones SSH.

## 🎙️ Instalación y configuración de DarkIce

```bash
sudo apt install darkice
```
- Instala el programa DarkIce, que transmite audio en vivo a un servidor de streaming.

```bash
sudo nano /etc/darkice.cfg
```
- Abre el archivo de configuración de DarkIce para editar parámetros como:
  - Fuente de audio
  - Formato de transmisión
  - Servidor destino

```bash
sudo tee /etc/darkice.cfg > /dev/null
```
- Crea un archivo de configuración vacío para editarlo posteriormente.

```bash
darkice -c /etc/darkice.cfg
```
- Inicia la transmisión de audio con la configuración especificada.

## 🔁 Módulo Loopback de sonido

```bash
sudo modprobe snd-aloop
```
- Carga el módulo `snd-aloop`, un dispositivo de audio virtual que redirige el audio de salida como entrada.

```bash
aplay -l
```
- Lista los dispositivos de audio para verificar que `Loopback` esté activo.

```bash
echo snd-aloop | sudo tee -a /etc/modules
```
- Asegura que `snd-aloop` se cargue automáticamente al iniciar el sistema.

## 🔊 Herramientas ALSA

```bash
sudo apt install alsa-utils
```
- Instala utilidades como:
  - `alsamixer`: control de volumen.
  - `amixer`: control por comandos.
  - `aplay`: reproductor de audio.
  - `arecord`: grabadora de audio.

## 🎵 Reproducir y transmitir una canción en bucle con FFmpeg

```bash
ffmpeg -re -stream_loop -1 -i cancion.mp3 \
  -content_type audio/mpeg \
  -f mp3 \
  icecast://source:hackme@54.225.48.159:8000/live.mp3
```
- Reproduce `cancion.mp3` en bucle y la transmite como MP3 al servidor Icecast.

## 🎥 Transmitir video con FFmpeg

```bash
ffmpeg -re -i cancion.mp4 \
  -c:v libvpx -b:v 800k \
  -c:a libvorbis \
  -f webm \
  -content_type video/webm \
  icecast://source:hackme@3.81.82.145:8000/video.webm
```
- Transmite el archivo `cancion.mp4` en formato WebM al servidor Icecast.
