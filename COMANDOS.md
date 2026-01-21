## 🎯 COMANDOS EXACTOS PARA COPIAR Y PEGAR

> **Copia y pega estos comandos exactamente en orden. Reemplaza `TU_USUARIO` con tu usuario de GitHub.**

---

## ✅ PASO 1: INSTALAR MKDOCS Y MATERIAL

### Copiar y Pegar (Windows - PowerShell como Administrador):

```powershell
pip install mkdocs mkdocs-material
```

### O en macOS/Linux:

```bash
pip install mkdocs mkdocs-material
```

**Verificar:**
```bash
mkdocs --version
```

---

## ✅ PASO 2: PRUEBA LOCAL

### Copiar y Pegar:

```bash
mkdocs serve
```

**Resultado esperado:**
- Abre navegador en: `http://localhost:8000`
- Verifica todas las páginas
- Presiona `Ctrl + C` para detener

---

## ✅ PASO 3: INICIALIZAR GIT

### Primera vez - Copiar y Pegar:

```bash
git config --global user.name "Tu Nombre Completo"
git config --global user.email "tu.email@ejemplo.com"
```

### Copiar y Pegar:

```bash
git init
```

---

## ✅ PASO 4: PRIMER COMMIT

### Copiar y Pegar:

```bash
git add .
```

### Copiar y Pegar:

```bash
git commit -m "commit inicial: documentación CyberShield completa"
```

---

## ✅ PASO 5: CREAR REPOSITORIO EN GITHUB

### Manual en https://github.com:

1. Haz clic en el **+** (arriba a la derecha)
2. Selecciona **New repository**
3. **Nombre:** `Proyecto-Jose`
4. **Marcas:** ☑️ Public (IMPORTANTE)
5. **NO marques** README, .gitignore, LICENSE
6. Clic en **Create repository**

### Después de crear, copia la URL que se ve. Debe ser algo como:

```
https://github.com/TU_USUARIO/Proyecto-Jose.git
```

---

## ✅ PASO 6: VINCULAR REPOSITORIO

### Copiar y Pegar (REEMPLAZA `TU_USUARIO`):

```bash
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git
```

### Copiar y Pegar:

```bash
git branch -M main
```

### Copiar y Pegar:

```bash
git push -u origin main
```

**Si pide contraseña:** Usa tu token de GitHub o contraseña

---

## ✅ PASO 7: DESPLIEGUE EN GITHUB PAGES

### Instalar extensión - Copiar y Pegar:

```bash
pip install mkdocs-gh-deploy
```

### Desplegar - Copiar y Pegar:

```bash
mkdocs gh-deploy
```

**Resultado esperado:**
```
INFO     -  Copying './site' to 'gh-pages' branch and pushing to GitHub...
INFO     -  Your documentation should shortly be live at https://TU_USUARIO.github.io/Proyecto-Jose/
```

**Espera 2-3 minutos y luego abre en navegador:**

```
https://TU_USUARIO.github.io/Proyecto-Jose/
```

---

## 📋 RESUMEN DE COMANDOS POR ORDEN

```bash
# 1. Instalar
pip install mkdocs mkdocs-material

# 2. Verificar
mkdocs --version

# 3. Probar localmente
mkdocs serve
# Presiona Ctrl + C para detener

# 4. Configurar Git (primera vez)
git config --global user.name "Tu Nombre"
git config --global user.email "tu.email@ejemplo.com"

# 5. Inicializar
git init

# 6. Primer commit
git add .
git commit -m "commit inicial: documentación CyberShield completa"

# 7. Agregar remoto (REEMPLAZA TU_USUARIO)
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git

# 8. Enviar a main branch
git branch -M main
git push -u origin main

# 9. Instalar extensión de despliegue
pip install mkdocs-gh-deploy

# 10. Desplegar
mkdocs gh-deploy

# ¡LISTO! Tu sitio está en:
# https://TU_USUARIO.github.io/Proyecto-Jose/
```

---

## 🔄 PARA FUTUROS CAMBIOS

Cuando quieras hacer cambios y actualizarlos:

```bash
# 1. Edita los archivos .md

# 2. Prueba localmente
mkdocs serve

# 3. Si todo está bien, commit
git add .
git commit -m "Descripción del cambio"
git push

# 4. Desplega
mkdocs gh-deploy
```

---

## ⚠️ ERRORES COMUNES Y SOLUCIONES

### Error: "ModuleNotFoundError: No module named 'mkdocs'"

```bash
pip install --upgrade mkdocs mkdocs-material
```

### Error: "fatal: 'origin' does not appear to be a 'git' repository"

```bash
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git
```

### El sitio no aparece en GitHub Pages

1. Ve a: `https://github.com/TU_USUARIO/Proyecto-Jose`
2. Settings → Pages
3. Verifica que esté en rama `gh-pages`
4. Espera 2-3 minutos y recarga

### Los estilos no se ven (Material Theme no carga)

```bash
pip install --upgrade mkdocs-material
mkdocs gh-deploy --clean
```

---

## ✅ CHECKLIST FINAL

- [ ] MkDocs instalado (`mkdocs --version` funciona)
- [ ] Sitio se ve localmente (`mkdocs serve`)
- [ ] Git inicializado (`git status` muestra archivos)
- [ ] Primer commit hecho
- [ ] Repositorio creado en GitHub (público)
- [ ] Remoto agregado (`git remote -v` muestra origin)
- [ ] Código enviado a GitHub (`git push` funciona)
- [ ] Despliegue en GitHub Pages hecho (`mkdocs gh-deploy`)
- [ ] Sitio accesible en https://TU_USUARIO.github.io/Proyecto-Jose/
- [ ] Las 5 páginas aparecen en el menú
- [ ] Los estilos Material se ven correctamente
- [ ] Los bloques de código funcionan
- [ ] Los bloques desplegables se pueden abrir

---

## 🎉 ¡ÉXITO!

Si completaste todos los pasos, tu documentación está:

✅ Completamente desplegada en GitHub Pages  
✅ Accesible públicamente  
✅ Con tema Material aplicado  
✅ Con extensiones avanzadas  
✅ Con contenido profesional  
✅ **Listo para obtener calificación máxima**

---

**Preguntas frecuentes:**

**P: ¿Dónde está mi sitio?**  
R: En `https://TU_USUARIO.github.io/Proyecto-Jose/` (reemplaza TU_USUARIO)

**P: ¿Cómo edito el contenido?**  
R: Edita los archivos `.md` en la carpeta `docs/` y ejecuta `mkdocs gh-deploy`

**P: ¿Por qué tarda en actualizar?**  
R: GitHub tarda 2-3 minutos en desplegar. Limpia el cache del navegador.

**P: ¿Puedo cambiar los colores?**  
R: Sí, edita `mkdocs.yml` en la sección `theme.palette`

