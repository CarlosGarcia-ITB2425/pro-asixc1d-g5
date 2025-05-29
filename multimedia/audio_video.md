
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



```bash
sudo nano /etc/darkice.cfg
```


---

## 5️⃣ Configurar Icecast  
![Icecast conf](conficecast.png)


```bash
sudo nano /etc/icecast2/icecast.xml
```

---

## 6️⃣ Probar entrada de audio con GStreamer  
![GStreamer](gstlaunch.png)

```bash
gst-launch-1.0 ...
```



---

## 7️⃣ Pruebas de transmisión  
![Prova1](Proves.png)

![Prova2](Proves2.png)



---

## 8️⃣ Ejecutar Darkice  
![darkice](darkice.png)

```bash
sudo darkice
```

## 9️⃣ Reproducir archivos de prueba  
![mp3 ](streamloop.png)

![mp3](reproducciomp3.png)

![mp4](reproducirmp4.png)

![mp4](Reproducciomp4.png)

---


