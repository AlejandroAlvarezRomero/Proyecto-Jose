## 📋 GUÍA COMPLETA DE DESPLIEGUE - CyberShield Documentation

Esta es la guía exacta paso a paso para desplegar tu documentación MkDocs en GitHub Pages.

---

## FASE 1: PREPARACIÓN DEL ENTORNO LOCAL

### Paso 1.1: Instalar MkDocs y Tema Material

```powershell
# En Windows (PowerShell como Administrador)
pip install mkdocs mkdocs-material
```

O en macOS/Linux:
```bash
pip install mkdocs mkdocs-material
```

**Verificación:**
```bash
mkdocs --version
```

### Paso 1.2: Verificar la estructura del proyecto

Tu carpeta debe verse así:
```
Proyecto-Jose/
├── mkdocs.yml
├── docs/
│   ├── index.md
│   ├── introduccion.md
│   ├── instalacion.md
│   ├── uso.md
│   └── conclusiones.md
├── .gitignore (opcional)
└── README.md (opcional)
```

### Paso 1.3: Crear archivo .gitignore (Recomendado)

En la raíz del proyecto, crear archivo `.gitignore`:

```
site/
.DS_Store
*.pyc
__pycache__/
venv/
.venv/
*.egg-info/
dist/
build/
```

---

## FASE 2: PRUEBA LOCAL

### Paso 2.1: Servir la documentación localmente

```bash
mkdocs serve
```

**Salida esperada:**
```
INFO     -  Building documentation...
INFO     -  Cleaning site directory
INFO     -  Documentation built in X.XX seconds
INFO     -  Serving on http://127.0.0.1:8000/
```

### Paso 2.2: Visualizar en navegador

Abre tu navegador e ingresa: **http://localhost:8000**

Verifica que:
- ✅ Todas las 5 páginas aparecen en la navegación
- ✅ Los enlaces funcionan correctamente
- ✅ El tema Material se ve aplicado
- ✅ El código de colores (negro/cyan) es visible
- ✅ Los bloques desplegables funcionan

### Paso 2.3: Detener el servidor

Presiona: `Ctrl + C` en la terminal

---

## FASE 3: INICIALIZAR REPOSITORIO GIT

### Paso 3.1: Inicializar Git

```bash
git init
```

### Paso 3.2: Configurar usuario (Primera vez)

```bash
git config --global user.name "Tu Nombre Completo"
git config --global user.email "tu.email@ejemplo.com"
```

### Paso 3.3: Agregar todos los archivos

```bash
git add .
```

### Paso 3.4: Primer commit

```bash
git commit -m "commit inicial: documentación CyberShield completa"
```

**Salida esperada:**
```
[master (root-commit) abc1234] commit inicial: documentación CyberShield completa
 5 files changed, 500 insertions(+)
 ...
```

---

## FASE 4: CREAR REPOSITORIO EN GITHUB

### Paso 4.1: Crear cuenta en GitHub (si no tienes)

- Ve a https://github.com
- Haz clic en "Sign up"
- Completa el proceso de registro

### Paso 4.2: Crear nuevo repositorio

1. En GitHub, haz clic en el icono **+** (arriba a la derecha)
2. Selecciona **New repository**
3. Nombre: `Proyecto-Jose` (o el que prefieras)
4. **IMPORTANTE:** Marca como **Public** (para GitHub Pages)
5. NO inicialices con README, .gitignore ni LICENSE (ya los tenemos)
6. Haz clic en **Create repository**

### Paso 4.3: Copiar URL del repositorio

Después de crear, verás la URL. Ejemplo:
```
https://github.com/tuusuario/Proyecto-Jose.git
```

---

## FASE 5: VINCULAR REPOSITORIO LOCAL CON GITHUB

### Paso 5.1: Agregar remoto

En tu terminal, dentro de la carpeta del proyecto:

```bash
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git
```

**Reemplaza:**
- `TU_USUARIO` con tu nombre de usuario de GitHub
- Mantén el nombre del repositorio

### Paso 5.2: Verificar conexión

```bash
git remote -v
```

**Salida esperada:**
```
origin  https://github.com/TU_USUARIO/Proyecto-Jose.git (fetch)
origin  https://github.com/TU_USUARIO/Proyecto-Jose.git (push)
```

### Paso 5.3: Enviar código a GitHub

```bash
git branch -M main
git push -u origin main
```

Si pide autenticación, usa tu token de GitHub o contraseña.

---

## FASE 6: DESPLIEGUE EN GITHUB PAGES

### Paso 6.1: Instalar extensión para GitHub Pages

```bash
pip install mkdocs-gh-deploy
```

### Paso 6.2: Ejecutar despliegue

```bash
mkdocs gh-deploy
```

**Salida esperada:**
```
INFO     -  Cleaning site directory
INFO     -  Building documentation to directory: C:\...\site
INFO     -  Documentation built in X.XX seconds
INFO     -  Copying './site' to 'gh-pages' branch and pushing to GitHub...
INFO     -  Your documentation should shortly be live at https://TU_USUARIO.github.io/Proyecto-Jose/
```

### Paso 6.3: Verificar despliegue

Espera 2-3 minutos y luego abre en navegador:
```
https://TU_USUARIO.github.io/Proyecto-Jose/
```

---

## FASE 7: VERIFICACIÓN FINAL

### ✅ Checklist de Validación

- ✅ El sitio es accesible en GitHub Pages
- ✅ Se ven todas 5 páginas en la navegación
- ✅ El tema Material se ve correctamente
- ✅ Los colores (negro/cyan) están aplicados
- ✅ Los botones de navegación funcionan
- ✅ Los bloques de código están resaltados
- ✅ Los bloques desplegables (detalles) funcionan
- ✅ Las tablas se ven bien formateadas
- ✅ Los admonitions (advertencias, notas, etc.) se ven bien
- ✅ El buscador funciona (arriba a la derecha)
- ✅ Los enlaces internos funcionan

---

## REFERENCIAS DE COMANDOS IMPORTANTES

### Para Desarrollo Local

```bash
# Iniciar servidor local
mkdocs serve

# Compilar sitio estático
mkdocs build
```

### Para Git

```bash
# Ver estado
git status

# Ver commits
git log

# Hacer nuevo commit
git add .
git commit -m "descripción del cambio"
git push

# Ver cambios no enviados
git diff
```

### Para Despliegue

```bash
# Desplegar en GitHub Pages
mkdocs gh-deploy

# Desplegar limpiando site anterior
mkdocs gh-deploy --clean
```

---

## SOLUCIÓN DE PROBLEMAS

### Problema: "ModuleNotFoundError: No module named 'mkdocs'"

**Solución:**
```bash
pip install mkdocs mkdocs-material --upgrade
```

### Problema: "fatal: 'origin' does not appear to be a 'git' repository"

**Solución:**
```bash
git remote add origin https://github.com/TU_USUARIO/Proyecto-Jose.git
```

### Problema: "Permission denied (publickey)"

**Solución:** 
1. Genera clave SSH en GitHub
2. O usa HTTPS en lugar de SSH
3. Usa token de autenticación personal

### Problema: Sitio no aparece en GitHub Pages

**Verificación:**
1. Ve a tu repositorio en GitHub
2. Settings → Pages
3. Verifica que esté configurado en rama `gh-pages`
4. Espera 2-3 minutos
5. Recarga la página

### Problema: Los estilos no se ven (tema Material no carga)

**Solución:**
1. Verifica que `mkdocs-material` está instalado: `pip list | grep material`
2. Ejecuta: `pip install --upgrade mkdocs-material`
3. Limpia y redeploya: `mkdocs gh-deploy --clean`

---

## PRÓXIMOS PASOS DESPUÉS DEL DESPLIEGUE

### Para Hacer Más Cambios:

1. Edita los archivos `.md` en la carpeta `docs/`
2. Prueba localmente: `mkdocs serve`
3. Haz commit y push:
   ```bash
   git add .
   git commit -m "Descripción del cambio"
   git push
   ```
4. Desplega:
   ```bash
   mkdocs gh-deploy
   ```

### Para Personalizar Más:

1. Edita `mkdocs.yml` para cambiar colores, fuentes, etc.
2. Agrega más extensiones de Markdown
3. Crea subdirectorios en `docs/` para más organización
4. Añade carpeta `docs/assets/` para imágenes

---

## REFERENCIAS EXTERNAS

- [Documentación de MkDocs](https://www.mkdocs.org/)
- [Tema Material para MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)

---

**¡Felicidades! Tu documentación está lista para ser desplegada.** 🎉

