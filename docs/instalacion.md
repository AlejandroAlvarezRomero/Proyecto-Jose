# ⚙️ Guía de Instalación y Configuración

## Requisitos del Sistema

### Mínimos Recomendados

- **Procesador:** Intel Core i5 / AMD Ryzen 5 o superior
- **RAM:** 8 GB mínimo (16 GB recomendado)
- **Almacenamiento:** 20 GB libre en SSD
- **Conexión:** Internet estable (no menos de 10 Mbps)
- **Sistema Operativo:** Windows 10+, macOS 10.15+, o Ubuntu 18.04+

## Instalación Paso a Paso

### 1. Instalación de Herramientas Base

Primero, asegúrate de tener instalado Git y Python:

```bash
# En Windows (usando PowerShell como administrador)
choco install git python3 -y

# En macOS (usando Homebrew)
brew install git python3

# En Linux (Debian/Ubuntu)
sudo apt-get update
sudo apt-get install git python3 python3-pip -y
```

### 2. Creación del Entorno Virtual

Es una buena práctica usar entornos virtuales para aislar dependencias:

```bash
# Crear directorio del proyecto
mkdir cybershield-workspace
cd cybershield-workspace

# Crear entorno virtual
python3 -m venv venv

# Activar entorno virtual
# En Windows:
venv\Scripts\activate
# En macOS/Linux:
source venv/bin/activate
```

### 3. Instalación de Herramientas de Seguridad

!!! note "Nota Importante"
    Estas herramientas deben usarse únicamente con propósitos educativos y éticos. Cualquier uso sin autorización es ilegal.

#### Nmap (Network Mapper)

```bash
# En Windows
choco install nmap -y

# En macOS
brew install nmap

# En Linux
sudo apt-get install nmap -y
```

#### Wireshark (Analizador de Tráfico)

```bash
# En Windows
choco install wireshark -y

# En macOS
brew install --cask wireshark

# En Linux
sudo apt-get install wireshark -y
```

#### Metasploit Framework

```bash
# En macOS
brew install metasploit

# En Linux (Debian/Ubuntu)
wget https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wss.erb
```

### 4. Instalación de Dependencias Python

Algunas herramientas útiles para seguridad en Python:

```bash
# Activar tu entorno virtual primero
pip install --upgrade pip
pip install scapy paramiko requests cryptography
```

## Verificación de la Instalación

<details markdown="1">
<summary><b>Scripts de Verificación (Click para expandir)</b></summary>

```bash
# Verificar Git
git --version

# Verificar Python
python3 --version

# Verificar Nmap
nmap --version

# Verificar paquetes Python
pip list | grep -E "scapy|paramiko|requests"
```

</details>

## Tabla de Versiones Recomendadas

| Herramienta | Versión Mínima | Versión Recomendada | Licencia |
|---|---|---|---|
| Python | 3.7 | 3.10+ | PSF |
| Nmap | 7.70 | 7.93+ | Libre |
| Wireshark | 3.0 | 4.0+ | GPL |
| Git | 2.20 | 2.40+ | GPL-2.0 |

## Configuración Inicial de Git

Configura tu identidad en Git para futuros commits:

```bash
git config --global user.name "Tu Nombre Completo"
git config --global user.email "tu.email@ejemplo.com"
git config --global core.editor "nano"
```

## Solución de Problemas Comunes

!!! warning "Problema: 'python3: command not found'"
    **Solución:** Agrega Python al PATH del sistema. En Windows, reinstala Python asegurándote de marcar "Add Python to PATH".

!!! warning "Problema: Error de permisos en Linux"
    **Solución:** Usa `sudo` o añade tu usuario al grupo sudo: `sudo usermod -aG sudo $USER`

!!! warning "Problema: Conflicto de puertos"
    **Solución:** Verifica qué proceso ocupa el puerto: `netstat -ano | findstr :8080` (Windows) o `lsof -i :8080` (Unix).

## Siguientes Pasos

Una vez completada la instalación:

1. ✅ Verifica que todas las herramientas funcionan correctamente
2. ✅ Crea tu primer entorno de prueba aislado
3. ✅ Familiarízate con la línea de comandos

[➡️ Ir a Uso de Herramientas](uso.md){ .md-button .md-button--primary }