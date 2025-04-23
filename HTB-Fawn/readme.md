# 🐾 HTB - Fawn

**IP:** 10.129.245.88
**Dificultad:** Muy fácil  
**Categoría:** Starting Point  
**Autor:** [miguelt86](https://www.hackthebox.com/profile/2126021)

---

## 🎯 Objetivo

Conectarse al servicio FTP expuesto en la máquina y capturar la bandera accediendo como usuario anónimo.

---

## 🔍 Escaneo Nmap

```bash
sudo nmap -sS -Pn -p- -T4 10.129.245.88

---

## 🔐 Acceso vía FTP 

ftp 10.129.160.179
Usuario: anonymous
Contraseña: anon123

---

## 🗂️ Listado y descarga de archivos:

ls
get flag.txt

---

## 🏁 Flag

flag.txt

---

## 🧰 Herramientas utilizadas

nmap
ftp
openvpn

## ✍️ Autor
GitHub: @Migueltejada86
HTB Profile: miguelt86
