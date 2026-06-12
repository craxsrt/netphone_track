# Netphone Track 🌐📡

Herramienta ligera basada en Node.js diseñada para el seguimiento y gestión de conexiones de red en entornos controlados.

## 🚀 Guía de Instalación Global

### 📱 1. Termux (Android)
```bash
pkg update && pkg upgrade -y
pkg install git nodejs -y
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
node nettrack.js
```

### 🐧 2. Linux (Ubuntu/Debian/Kali)
```bash
sudo apt update && sudo apt install git nodejs npm -y
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
node nettrack.js
```

### 🪟 3. Windows (PowerShell)
```powershell
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
node nettrack.js
```

### 🐋 4. Docker
```bash
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
docker build -t netphone-track .
docker run -it netphone-track
```

---

## 🌐 Exposición Web (Cloudflared Tunnel)

Para levantar la interfaz o el servicio y exponerlo a internet usando `cloudflared`, sigue estos pasos utilizando las **sesiones múltiples** de Termux:

### ⏱️ Paso 1: Sesión 1 (Iniciar la Herramienta)
Inicia el script normalmente en tu primera pantalla:
```bash
cd netphone_track
node nettrack.js
```
*(Nota el puerto en el que corre la herramienta, por ejemplo: `3000` o `8080`)*.

### 📲 Paso 2: Sesión 2 (Levantar el Túnel)
1. Desliza el dedo desde el borde izquierdo de la pantalla de Termux hacia el centro y toca en **"New Session"** para abrir la **Sesión 2**.
2. Instala y ejecuta `cloudflared` apuntando al puerto de tu herramienta:

```bash
# Instalar cloudflared en Termux
pkg install cloudflared -y

# Levantar el túnel público (reemplaza 3000 por tu puerto real)
cloudflared tunnel --url http://localhost:3000
```
3. Copia el enlace seguro `https://...trycloudflare.com` que te generará la terminal para acceder a tu herramienta desde cualquier parte del mundo.

---
⚠️ *Aviso: Uso exclusivo para entornos de laboratorio y pruebas autorizadas.*
