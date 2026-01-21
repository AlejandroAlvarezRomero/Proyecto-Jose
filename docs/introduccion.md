# 📖 Introducción a la Ciberseguridad

## ¿Qué es la Ciberseguridad?

La **ciberseguridad** es el conjunto de técnicas, procesos y herramientas diseñadas para **proteger sistemas informáticos, redes y datos** contra accesos no autorizados, modificaciones destructivas o robo.

En la era digital actual, es **más importante que nunca**.

---

## 🚨 La Realidad Actual

<div class="grid cards" markdown>

!!! danger "📊 **Estadísticas Alarmantes**"
    
    - ⚡ **Un ataque cada 11 segundos**
    - 💰 **Pérdidas globales: $6 billones anuales**
    - 📈 **Aumento: 30% año a año**
    - 🎯 **Objetivo: Cualquiera (desde individuos a gobiernos)**

!!! warning "🔓 **Tipos de Ataques Comunes**"
    
    - 🎣 **Phishing**: 90% de brechas comienzan así
    - 🔐 **Ransomware**: Retiene datos por dinero
    - 💻 **Malware**: Software malicioso
    - 🌐 **Ataques DDoS**: Derriban servidores
    - 🔑 **Robo de credenciales**: Acceso no autorizado

!!! success "💡 **La Buena Noticia**"
    
    - ✅ **Es prevenible**: Con conocimiento
    - ✅ **Es detectable**: Con herramientas adecuadas
    - ✅ **Es controlable**: Con disciplina
    - ✅ **Es lucrativa**: Carrera demandada
    - ✅ **Es accesible**: Para cualquiera

</div>

---

## 🏗️ Pilares Fundamentales: La Triada CIA

Cualquier sistema de seguridad se basa en **tres principios fundamentales**:

### 🔒 Confidencialidad (Confidentiality)

**Garantizar que solo personas autorizadas acceden a la información**

```
Datos Sensibles
    ↓
[Encriptación]
    ↓
Acceso Controlado
    ↓
Solo Autorizados ✅
```

**Ejemplos:**
- 🏥 Historiales médicos privados
- 💳 Números de tarjeta de crédito
- 📧 Correos electrónicos personales
- 🔐 Contraseñas y credenciales

---

### ✏️ Integridad (Integrity)

**Garantizar que los datos no se alteran sin autorización**

```
Datos Originales
    ↓
[Verificación]
    ↓
¿Sin cambios? ✅ / ¿Alterados? ❌
```

**Ejemplos:**
- 📋 Registros de transacciones bancarias
- 📊 Bases de datos críticas
- 📄 Documentos legales
- 🎮 Archivos de configuración

---

### 🌐 Disponibilidad (Availability)

**Garantizar que los sistemas están accesibles cuando se necesitan**

```
Servicio Activo
    ↓
[Monitoreo]
    ↓
¿Funcionando? ✅ / ¿Caído? ❌
```

**Ejemplos:**
- 🏦 Cajeros automáticos disponibles 24/7
- 🌐 Servidores web sin interrupciones
- 📞 Centros de atención al cliente
- 🚑 Sistemas de emergencia

---

## ⚠️ Tipos de Amenazas

### 1️⃣ **Malware** - Software Malicioso

| Tipo | Descripción | Impacto |
|------|-------------|---------|
| **Virus** | Se replica como un virus biológico | Daña archivos y sistema |
| **Gusano** | Se propaga automáticamente por red | Consume recursos y ancho de banda |
| **Troyano** | Se disfraza de programa legítimo | Abre puertas traseras |
| **Ransomware** | Cifra datos y pide dinero | Pérdida completa de datos |
| **Spyware** | Espía la actividad del usuario | Robo de información personal |

---

### 2️⃣ **Exploits** - Aprovechamiento de Vulnerabilidades

Una **vulnerabilidad** es una debilidad en un sistema que puede ser explotada.

**Ciclo de vida:**

```
1. Descubrimiento       → Se encuentra una debilidad
2. Explotación          → Se crea código para usarla
3. Propagación          → Se difunde el ataque
4. Mitigación           → Se publica un parche
5. Adopción del parche  → El usuario se actualiza
```

---

### 3️⃣ **Ingeniería Social** - La Ingeniería Humana

**La mayoría de los ataques comienzan con manipulación psicológica:**

!!! warning "Técnicas Comunes"
    
    - 🎣 **Phishing**: Correos falsos para robar datos
    - 📞 **Vishing**: Llamadas telefónicas fraudulentas
    - 🎭 **Pretexting**: Crear historias falsas para obtener acceso
    - 🔐 **Shoulder Surfing**: Mirar la pantalla de alguien
    - 🎁 **Tailgating**: Seguir a alguien autenticado

**La defensa:** Educación y conciencia.

---

### 4️⃣ **Ataques DDoS** - Denegación de Servicio

**Saturar un servidor con tráfico para que no pueda responder:**

```
Atacante
  ↓
Botnet (Millones de máquinas infectadas)
  ↓
BOMBARDEO de solicitudes → Servidor sobrecarguado → Servicio caído
```

**Impacto:**
- 💰 Pérdidas económicas inmediatas
- 😠 Pérdida de reputación
- 📉 Clientes afectados
- 🔴 Negocio detenido

---

## 🎯 Conceptos Clave

### Vulnerabilidad

!!! info "📌 Definición"
    
    Una **debilidad en un sistema** que puede ser explotada por un atacante para obtener acceso no autorizado o causar daño.
    
    **Ejemplos:**
    - Software sin actualizar
    - Contraseñas débiles
    - Configuración incorrecta
    - Falta de firewall

### Amenaza

!!! warning "📌 Definición"
    
    Un **agente (persona, proceso o evento)** con la capacidad e intención de explotar vulnerabilidades.
    
    **Ejemplos:**
    - Hacker malicioso
    - Ransomware
    - Empleado descontento
    - Competencia corporativa

### Riesgo

!!! danger "📌 Definición"
    
    La **probabilidad de que una amenaza explote una vulnerabilidad** y cause impacto.
    
    **Fórmula:**
    ```
    RIESGO = Vulnerabilidad × Amenaza × Impacto
    ```

---

## 🎓 Niveles de Experiencia en Ciberseguridad

### 🟢 Nivel 1: Principiante

<details markdown="1">
<summary><b>¿Qué sabes? (Click para expandir)</b></summary>

**Conocimientos:**
- ✅ Conceptos básicos de seguridad
- ✅ Identificar amenazas comunes
- ✅ Usar herramientas básicas de escaneo
- ✅ Entender la importancia de contraseñas fuertes
- ✅ Reconocer ataques phishing

**Herramientas:**
- Nmap básico
- Wireshark básico
- Navegadores web seguros
- Antivirus

**Tiempo:** 1-3 meses de estudio

</details>

---

### 🟡 Nivel 2: Intermedio

<details markdown="1">
<summary><b>¿Qué sabes? (Click para expandir)</b></summary>

**Conocimientos:**
- ✅ Auditorías de seguridad completas
- ✅ Configurar firewalls
- ✅ Implementar políticas de seguridad
- ✅ Análisis forense básico
- ✅ Scripting para automatización

**Herramientas:**
- Nmap avanzado
- Wireshark análisis profundo
- Metasploit
- Burp Suite
- Python/Bash

**Tiempo:** 6-12 meses de experiencia

</details>

---

### 🔴 Nivel 3: Avanzado

<details markdown="1">
<summary><b>¿Qué sabes? (Click para expandir)</b></summary>

**Conocimientos:**
- ✅ Pruebas de penetración complejas
- ✅ Análisis de malware
- ✅ Investigación forense
- ✅ Arquitectura de seguridad empresarial
- ✅ Desarrollo de exploits

**Herramientas:**
- Todas las anteriores +
- IDA Pro
- Ghidra
- Frida
- Custom tools

**Tiempo:** 2+ años de experiencia intensiva

</details>

---

## 🔗 Enlaces Útiles y Referencias

<div class="grid cards" markdown>

!!! info "🌐 **Organizaciones Importantes**"
    
    **OWASP - Open Web Application Security Project**
    
    [→ OWASP Top 10](https://owasp.org/www-project-top-ten/)
    
    Las 10 vulnerabilidades más críticas en aplicaciones web.

!!! note "📊 **Estándares Globales**"
    
    **NIST - National Institute of Standards and Technology**
    
    [→ NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
    
    Marco de referencia de seguridad estadounidense.

!!! warning "🔬 **Institutos de Investigación**"
    
    **SANS Institute**
    
    [→ Proyecto SANS](https://www.sans.org/)
    
    Instituto líder en investigación de seguridad.

</div>

---

## 📈 Tendencias Actuales en Ciberseguridad

```
2024: Inteligencia Artificial en ataques y defensa
2025: Computación cuántica (amenaza a encriptación actual)
2026: Zero Trust Architecture (confianza cero)
2027: Automatización completa de respuesta
```

---

## 🚀 Próximos Pasos

### 1️⃣ Entiende los Conceptos

✅ Ya lo hiciste (estás aquí)

### 2️⃣ Instala las Herramientas

[→ **Ir a Instalación**](instalacion.md)

Necesitarás:
- Nmap
- Wireshark
- Python
- Git

### 3️⃣ Practica con Ejercicios

[→ **Ir a Uso de Herramientas**](uso.md)

---

!!! success "💡 Recuerda"
    
    **La ciberseguridad se aprende haciendo, no solo leyendo.**
    
    Después de leer esta introducción, continúa con los siguientes pasos para transformar tu conocimiento en habilidades prácticas.