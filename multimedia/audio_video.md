
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
![Darkice](installdarkice.png)

```bash
sudo apt install darkice
```

---

## 4️⃣ Configurar Darkice  
![Darkice conf](confdarkice.png)

📝 Editar el archivo de configuración:

```bash
sudo nano /etc/darkice.cfg
```

🔧 Asegúrate de configurar correctamente:  
- Fuente de audio  
- Servidor Icecast  
- Códec y bitrate

---

## 5️⃣ Configurar Icecast  
![Icecast conf](conficecast.png)

📝 Edita:

```bash
sudo nano /etc/icecast2/icecast.xml
```

⚙️ Configura:  
- Puerto de escucha  
- Mountpoint  
- Credenciales de acceso

---

## 6️⃣ Probar entrada de audio con GStreamer  
![GStreamer](gstlaunch.png)

```bash
gst-launch-1.0 ...
```

🎧 Asegúrate de que el audio esté siendo capturado correctamente.

---

## 7️⃣ Pruebas de transmisión  
![Prova1](Proves.png)

![Prova2](Proves2.png)

🔍 Verifica que el flujo se transmite correctamente al servidor.

---

## 8️⃣ Ejecutar Darkice  
![darkice](darkice.png)

```bash
sudo darkice
```

## 9️⃣ Reproducir archivos de prueba  
![mp3](reproducciomp3.png)

![mp4](reproducirmp4.png)

![mp4](Reproducciomp4.png)

---


