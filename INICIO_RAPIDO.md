# 🚀 INICIO RÁPIDO - DESPLIEGUE EN 15 MINUTOS

> **Lee esto PRIMERO. Tienes todo lo necesario para desplegar tu sitio en 15 minutos.**

---

## ⏱️ CRONOGRAMA

```
⏱️ Paso 1: Instalar           (2 min)
⏱️ Paso 2: Probar local       (1 min)
⏱️ Paso 3: Git setup          (2 min)
⏱️ Paso 4: GitHub setup       (3 min)
⏱️ Paso 5: Desplegar          (1 min)
⏱️ Paso 6: Esperar            (3 min) ← Automático
⏱️ Paso 7: Verificar          (1 min)
─────────────────────────────
⏱️ TOTAL:                     15 minutos
```

---

## 📋 LO QUE NECESITAS

- ✅ Este proyecto (ya descargado)
- ✅ Terminal/PowerShell (Windows) o Terminal (Mac/Linux)
- ✅ Cuenta en GitHub (gratuita)
- ✅ 15 minutos de tu tiempo
- ✅ Una taza de café ☕

---

## 🎬 COPIA Y PEGA ESTOS COMANDOS

### 1️⃣ INSTALAR MKDOCS Y MATERIAL

Copiar y pegar en tu terminal:

```bash
pip install mkdocs mkdocs-material
```

✅ Espera a que termine (1-2 minutos)

---

### 2️⃣ PROBAR LOCALMENTE

Copiar y pega:

```bash
mkdocs serve
```

**Resultado:** Verás algo como:
```
INFO     -  Serving on http://127.0.0.1:8000/
```

✅ Abre navegador en: **http://localhost:8000**  
✅ Verifica que se ve bien  
✅ Presiona **Ctrl + C** para detener

---

### 3️⃣ CONFIGURAR GIT (Primera vez)

Copiar y pega:

```bash
git config --global user.name "Tu Nombre Aquí"
git config --global user.email "tu.email@ejemplo.com"
```

Luego:

```bash
git init
git add .
git commit -m "commit inicial: CyberShield completo"
```

✅ Verás un mensaje como:
```
[master (root-commit) abc1234] commit inicial...
```

---

### 4️⃣ CREAR REPOSITORIO EN GITHUB

**MANUAL - No es comando, es en el navegador:**

1. Ve a https://github.com
2. Haz login (o crea cuenta si no tienes)
3. Click en el **+** (arriba a la derecha)
4. Selecciona **New repository**
5. **Nombre:** `Proyecto-Jose`
6. **Selecciona:** ☑️ Public (IMPORTANTE)
7. **NO marques:** README, .gitignore, LICENSE
8. Click en **Create repository**

✅ Después de crear, copia la URL que sale. Será algo como:
```
https://github.com/TU_USUARIO/Proyecto-Jose.git
```

---

### 5️⃣ ENVIAR CÓDIGO A GITHUB

Copiar y pega (REEMPLAZA `TU_USUARIO`):

```bash
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git
```

Luego:

```bash
git branch -M main
git push -u origin main
```

✅ Te pedirá contraseña o token. Usa tu token de GitHub.

---

### 6️⃣ DESPLEGAR EN GITHUB PAGES

Copiar y pega:

```bash
pip install mkdocs-gh-deploy
```

Luego:

```bash
mkdocs gh-deploy
```

✅ Verás:
```
INFO     -  Your documentation should shortly be live at 
INFO     -  https://TU_USUARIO.github.io/Proyecto-Jose/
```

---

### 7️⃣ ESPERAR Y VERIFICAR

⏱️ **Espera 2-3 minutos** (GitHub necesita tiempo para desplegar)

Luego abre en navegador:
```
https://TU_USUARIO.github.io/Proyecto-Jose/
```

**Reemplaza `TU_USUARIO` con tu usuario de GitHub**

✅ ¡LISTO! Tu sitio está publicado

---

## ✅ VERIFICACIÓN FINAL

En tu sitio, verifica que:

- [ ] Se ve el título "CyberShield"
- [ ] Aparecen las 5 páginas en el menú
- [ ] El color es negro/cyan
- [ ] El tema Material está aplicado
- [ ] Los bloques de código tienen botón de copiar
- [ ] El buscador funciona (arriba a la derecha)

Si todo está ✅, **¡FELICIDADES!** Tu proyecto está desplegado.

---

## ❌ ALGO SALIÓ MAL?

### Error: "ModuleNotFoundError: No module named 'mkdocs'"

```bash
pip install --upgrade mkdocs mkdocs-material
```

### Error: "fatal: 'origin' does not appear to be a 'git' repository"

Verifica que ejecutaste:
```bash
git init
```

### El sitio no aparece en GitHub Pages

1. Ve a tu repositorio en GitHub
2. Abre Settings → Pages
3. Verifica que esté en rama `gh-pages`
4. Espera 5 minutos y recarga

### Los estilos no se ven bien

```bash
pip install --upgrade mkdocs-material
mkdocs gh-deploy --clean
```

---

## 📞 REFERENCIAS RÁPIDAS

**Archivo con todos los comandos:**
→ [COMANDOS.md](COMANDOS.md)

**Guía detallada paso a paso:**
→ [GUIA_DESPLIEGUE.md](GUIA_DESPLIEGUE.md)

**Documentación completa:**
→ [DOCUMENTO_ENTREGA.md](DOCUMENTO_ENTREGA.md)

**Verificar que todo está:**
→ [VERIFICACION.md](VERIFICACION.md)

**Índice de toda la documentación:**
→ [INDEX.md](INDEX.md)

---

## 🎯 TUS ENLACES FINALES

Una vez desplegado, tendrás:

**Repositorio GitHub:**
```
https://github.com/TU_USUARIO/Proyecto-Jose
```

**Sitio Publicado:**
```
https://TU_USUARIO.github.io/Proyecto-Jose/
```

**Estos son los 2 enlaces que debes entregar.**

---

## 🎓 PARA TU ENTREGA

Necesitas entregar:

1. ✅ Enlace al repositorio: `https://github.com/TU_USUARIO/Proyecto-Jose`
2. ✅ Enlace al sitio publicado: `https://TU_USUARIO.github.io/Proyecto-Jose/`
3. ✅ Documento de explicación: [DOCUMENTO_ENTREGA.md](DOCUMENTO_ENTREGA.md)

---

## 💡 PRO TIPS

**Tip 1:** Si quieres hacer cambios después:
```bash
# Edita un archivo .md
# Luego:
git add .
git commit -m "descripción del cambio"
git push
mkdocs gh-deploy
```

**Tip 2:** Prueba siempre localmente primero:
```bash
mkdocs serve
# Verifica en http://localhost:8000
# Presiona Ctrl + C cuando termines
```

**Tip 3:** Si algo no funciona, consulta la guía detallada:
→ [GUIA_DESPLIEGUE.md](GUIA_DESPLIEGUE.md)

---

## 🎉 LISTO

Ya tienes:

✅ Código 100% completo  
✅ Configuración profesional  
✅ 5 páginas de contenido  
✅ Extensiones avanzadas  
✅ Documentación exhaustiva  
✅ Comandos listos para ejecutar

**¡Solo falta hacer clic y copiar/pegar!**

---

## 📊 CHECKLIST ANTES DE EMPEZAR

- [ ] Estoy en la carpeta correcta (Proyecto-Jose)
- [ ] Tengo Terminal/PowerShell abierta
- [ ] Tengo cuenta en GitHub (o voy a crear una)
- [ ] Tengo café/bebida para pasar el tiempo ☕
- [ ] Tengo estos 15 minutos libres

✅ Si marcaste todo, **¡COMENZAMOS!**

---

## 🚀 PRIMER COMANDO

Copia y pega esto AHORA en tu terminal:

```bash
pip install mkdocs mkdocs-material
```

**Cuando termine**, sigue con el Paso 2.

---

**Tiempo estimado:** 15 minutos  
**Dificultad:** Muy Fácil (solo copiar/pegar)  
**Resultado:** Tu sitio publicado en Internet  

**¡VAS! 🚀**

