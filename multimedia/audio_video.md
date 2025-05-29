
# 🛠️ Guía para Transmitir Audio/Video con Darkice e Icecast

---

## 1️⃣ Actualizar el sistema  
![sudo apt update](sudoaptupdate.png)


```bash
sudo apt update
```

---

## 2️⃣ Instalar Alsa-utils
![Alsa-utils](installalsa-utils.png)

```bash
sudo apt install alsa-utils
```

---

## 3️⃣ Instalar Darkice  
![Alsa-utils](installdarkice.png)

```bash
sudo apt install darkice
```

---

## 4️⃣ Configurar permisos (si es necesario)  
`04_configurar_permisos.png`  
🔐 Asegúrarse de que los permisos para la tarjeta de sonido o archivos del sistema estén correctamente configurados.

---

## 5️⃣ Configurar Darkice  
`05_configurar_darkice.png`  
📝 Editar el archivo de configuración:

```bash
sudo nano /etc/darkice.cfg
```

🔧 Asegúrate de configurar correctamente:  
- Fuente de audio  
- Servidor Icecast  
- Códec y bitrate

---

## 6️⃣ Configurar Icecast  
`06_configurar_icecast.png`  
📝 Edita:

```bash
sudo nano /etc/icecast2/icecast.xml
```

⚙️ Configura:  
- Puerto de escucha  
- Mountpoint  
- Credenciales de acceso

---

## 7️⃣ Probar entrada de audio con GStreamer  
`07_probar_audio_gstreamer.png`

```bash
gst-launch-1.0 ...
```

🎧 Asegúrate de que el audio esté siendo capturado correctamente.

---

## 8️⃣ Pruebas de transmisión  
`08_prueba_transmision_1.png`  
`09_prueba_transmision_2.png`

🔍 Verifica que el flujo se transmite correctamente al servidor.

---

## 9️⃣ Reproducir archivos de prueba  
`10_reproducir_mp3.png`  
`11_reproducir_mp4_1.png`  
`12_reproducir_mp4_2.png`

🎼 Prueba con archivos `.mp3` y `.mp4` para asegurarte de que la salida es funcional.

---

## 🔟 Configurar video  
`13_configurar_video.png`  
📹 Elige la fuente de video adecuada (dispositivo, cámara, etc.).

---

## 1️⃣1️⃣ Ejecutar Darkice  
`14_darkice_ejecucion.png`

```bash
sudo darkice
```

🚀 Inicia la transmisión.

---

## 1️⃣2️⃣ Transmisión continua  
`15_transmision_bucle.png`

🔁 Puedes automatizar la retransmisión o configurarla en modo bucle.

---

## 1️⃣3️⃣ Ver en el navegador  
`16_interfaz_web_icecast.png`  

🌐 Abre en tu navegador:

```arduino
http://localhost:8000
```

👁️ Desde aquí puedes monitorear tu transmisión en vivo.
