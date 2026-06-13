# Netphone Track 🌐📡

Herramienta ligera basada en Node.js para geolocalización en entornos controlados.
**Uso exclusivo para laboratorios y pruebas autorizadas.**

## 🚀 Instalación y Ejecución

### 📱 1. Termux (Android)

```bash
pkg update && pkg upgrade -y
pkg install git nodejs cloudflared -y
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
```

**Ejecutar (Sesión 1):**
```bash
node nettrack.js -p 8080 -t serveo -wl http://example.com
```

**Exponer a internet (Sesión 2):**
```bash
cloudflared tunnel --url http://localhost:8080
```

### 🐧 2. Linux (Ubuntu/Debian/Kali)

```bash
sudo apt update && sudo apt install git nodejs npm -y
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
node nettrack.js -p 8080 -t serveo -wl http://example.com
```

### 🪟 3. Windows (PowerShell)

```powershell
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
npm install
node nettrack.js -p 8080 -t serveo -wl http://example.com
```

### 🐋 4. Docker

```bash
git clone https://github.com/craxsrt/netphone_track.git
cd netphone_track
docker build -t netphone-track .
docker run -it netphone-track
```

## 📋 Parámetros

| Parámetro | Descripción | Ejemplo |
|-----------|-------------|---------|
| `-p` | Puerto | `-p 8080` |
| `-t` | Tunneling (`serveo` o `ngrok`) | `-t serveo` |
| `-wl` | Redirección | `-wl https://google.com` |

## ⚠️ Aviso

Uso exclusivo para laboratorios y pruebas autorizadas. No promueve actividades ilícitas.

## 📎 Enlaces

- GitHub: [craxsrt/netphone_track](https://github.com/craxsrt/netphone_track)
- Autor: [@craxsrt](https://github.com/craxsrt)
