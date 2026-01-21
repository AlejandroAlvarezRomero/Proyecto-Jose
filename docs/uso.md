# 🔧 Uso de Herramientas y Ejercicios Prácticos

## Introducción a las Herramientas

Esta sección proporciona guías prácticas para utilizar las herramientas de ciberseguridad instaladas. Todos los ejercicios deben realizarse en entornos de prueba autorizados.

## 1. Nmap - Escaneo de Redes

### ¿Qué es Nmap?

Nmap (Network Mapper) es una herramienta de código abierto utilizada para descubrimiento de redes y auditoría de seguridad.

### Comandos Básicos

```bash
# Escaneo simple de un host
nmap 192.168.1.1

# Escaneo de un rango de direcciones
nmap 192.168.1.0/24

# Escaneo de puertos específicos
nmap -p 22,80,443 192.168.1.1

# Escaneo agresivo con detección de versiones
nmap -A 192.168.1.1

# Escaneo silencioso (stealth scan)
nmap -sS 192.168.1.1
```

!!! tip "Consejo de Uso"
    Siempre utiliza Nmap únicamente en redes y sistemas sobre los que tengas permiso explícito.

## 2. Wireshark - Análisis de Tráfico

### Uso Básico

<details markdown="1">
<summary><b>Guía de Captura (Click para expandir)</b></summary>

1. Abre Wireshark
2. Selecciona la interfaz de red (ej: Ethernet, Wi-Fi)
3. Haz clic en el botón azul para iniciar captura
4. Realiza acciones en la red (navegar, descargar, etc.)
5. Detén la captura y analiza los paquetes

</details>

### Filtros Comunes

| Filtro | Descripción |
|---|---|
| `tcp` | Mostrar solo tráfico TCP |
| `udp` | Mostrar solo tráfico UDP |
| `http` | Mostrar solo HTTP |
| `dns` | Mostrar solo consultas DNS |
| `ip.addr == 192.168.1.1` | Filtrar por dirección IP |

## 3. Python para Seguridad

### Script: Verificador de Puerto

```python
import socket
import sys

def verificar_puerto(host, puerto):
    """
    Verifica si un puerto está abierto en un host.
    
    Args:
        host (str): Dirección IP o dominio
        puerto (int): Número de puerto a verificar
    
    Returns:
        bool: True si el puerto está abierto, False en caso contrario
    """
    try:
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        sock.settimeout(2)
        resultado = sock.connect_ex((host, puerto))
        sock.close()
        return resultado == 0
    except socket.error as e:
        print(f"Error: {e}")
        return False

# Ejemplo de uso
if __name__ == "__main__":
    host = "localhost"
    puerto = 80
    
    if verificar_puerto(host, puerto):
        print(f"✓ Puerto {puerto} está ABIERTO en {host}")
    else:
        print(f"✗ Puerto {puerto} está CERRADO en {host}")
```

### Script: Hash de Archivos

```python
import hashlib
import os

def calcular_hash(archivo, algoritmo='sha256'):
    """
    Calcula el hash de un archivo.
    
    Args:
        archivo (str): Ruta del archivo
        algoritmo (str): Algoritmo a usar (md5, sha1, sha256)
    
    Returns:
        str: Hash en formato hexadecimal
    """
    hash_obj = hashlib.new(algoritmo)
    
    with open(archivo, 'rb') as f:
        for bloque in iter(lambda: f.read(4096), b''):
            hash_obj.update(bloque)
    
    return hash_obj.hexdigest()

# Uso
archivo = "documento.pdf"
print(f"SHA-256: {calcular_hash(archivo)}")
```

## 4. Ejercicios Prácticos

### Ejercicio 1: Mapeo de Red Local

!!! example "Objetivo"
    Descubrir todos los dispositivos conectados en tu red local.

**Pasos:**

1. Identifica tu dirección IP: `ipconfig` (Windows) o `ifconfig` (Unix)
2. Ejecuta: `nmap -sn 192.168.1.0/24` (ajusta el rango según tu red)
3. Analiza los resultados

### Ejercicio 2: Captura y Análisis de Paquetes

!!! example "Objetivo"
    Capturar y analizar tráfico DNS en tu máquina local.

**Pasos:**

1. Abre Wireshark
2. Inicia captura en tu interfaz de red
3. Abre un navegador y navega a un sitio web
4. En Wireshark, filtra: `dns`
5. Observa las consultas DNS realizadas

### Ejercicio 3: Verificación de Integridad

!!! example "Objetivo"
    Crear y verificar hashes de archivos descargados.

**Pasos:**

```bash
# Descargar un archivo
wget https://ejemplo.com/archivo.zip

# Calcular hash
sha256sum archivo.zip

# Comparar con hash oficial proporcionado
# Los hashes deben coincidir exactamente
```

## Mejores Prácticas de Seguridad

- ✅ Siempre trabaja en entornos aislados
- ✅ Obtén permisos explícitos antes de auditar
- ✅ Mantén actualizadas todas las herramientas
- ✅ Usa VPN en redes públicas
- ✅ Documenta todos tus hallazgos
- ❌ Nunca ataque sistemas sin autorización
- ❌ No compartas credenciales de acceso

## Recursos Adicionales

**Documentación Oficial:**
- [Manual de Nmap](https://nmap.org/man/)
- [Wiki de Wireshark](https://wiki.wireshark.org/)
- [Documentación de Scapy](https://scapy.readthedocs.io/)

**Plataformas de Aprendizaje:**
- TryHackMe - Retos prácticos de hacking ético
- HackTheBox - Máquinas virtuales para practicar
- DVWA - Aplicación web vulnerable para aprender

[➡️ Ir a Conclusiones](conclusiones.md){ .md-button .md-button--primary }