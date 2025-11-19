# 🚀 Instrucciones de Deploy - FNAF Banner Interactivo

## ✅ Estado Actual

- ✅ Repositorio Git inicializado
- ✅ Commit inicial creado
- ✅ Archivos listos para deploy
- ✅ Configuración de Vercel preparada

---

## 📋 Pasos para Deploy

### Paso 1: Crear Repositorio en GitHub

1. Ve a [github.com](https://github.com) e inicia sesión
2. Click en el botón **"+"** (arriba derecha) → **"New repository"**
3. Configuración:
   - **Repository name:** `fnaf-banner-interactivo` (o el nombre que prefieras)
   - **Description:** "Banner interactivo FNAF 2 - Demo para aprobación"
   - **Visibility:** Private (recomendado) o Public
   - **NO marques** "Initialize with README" (ya tenemos uno)
   - Click en **"Create repository"**

### Paso 2: Conectar Repositorio Local con GitHub

Ejecuta estos comandos en tu terminal (ya estás en el directorio correcto):

```bash
# Reemplaza TU_USUARIO con tu usuario de GitHub
git remote add origin https://github.com/TU_USUARIO/fnaf-banner-interactivo.git

# Subir el código
git push -u origin main
```

**Nota:** Si GitHub te pide autenticación, puedes usar:
- Personal Access Token (recomendado)
- O GitHub CLI: `gh auth login`

### Paso 3: Deploy en Vercel

#### Opción A: Desde la Web (Más Fácil)

1. Ve a [vercel.com](https://vercel.com)
2. Inicia sesión con tu cuenta de GitHub
3. Click en **"Add New Project"**
4. Selecciona el repositorio `fnaf-banner-interactivo`
5. Vercel detectará automáticamente:
   - Framework Preset: Other
   - Build Command: (dejar vacío)
   - Output Directory: (dejar vacío)
6. Click en **"Deploy"**
7. Espera 1-2 minutos mientras se despliega

#### Opción B: Desde CLI

```bash
# Instalar Vercel CLI (si no lo tienes)
npm i -g vercel

# En el directorio del proyecto
vercel

# Seguir las instrucciones:
# - Login con tu cuenta
# - Link to existing project? No
# - Project name: fnaf-banner-interactivo
# - Directory: ./
# - Deploy
```

### Paso 4: Obtener el Link del Demo

Una vez desplegado, Vercel te dará una URL como:
```
https://fnaf-banner-interactivo.vercel.app
```

**Tu demo estará disponible en:**
```
https://fnaf-banner-interactivo.vercel.app/demo.html
```

**Versión standalone:**
```
https://fnaf-banner-interactivo.vercel.app/index.html
```

---

## 🔄 Actualizaciones Futuras

Cada vez que hagas cambios y quieras actualizar el deploy:

```bash
# Hacer cambios en los archivos
git add .
git commit -m "Descripción de los cambios"
git push origin main
```

Vercel detectará automáticamente el push y hará un nuevo deploy.

---

## 🐛 Troubleshooting

### Los videos no cargan
- Verifica que los archivos de video estén en el repositorio
- Revisa las rutas en `demo.html` (deben ser relativas)
- Abre la consola del navegador para ver errores

### Error al hacer push a GitHub
- Verifica que tengas permisos en el repositorio
- Usa un Personal Access Token si es necesario
- Revisa que el remote esté correcto: `git remote -v`

### Vercel no detecta los archivos
- Asegúrate de que `demo.html` esté en la raíz
- Verifica que `vercel.json` esté presente
- Revisa los logs de deploy en el dashboard de Vercel

---

## 📝 Notas Importantes

1. **Tamaño de archivos:** Los videos pueden ser grandes. GitHub tiene límites:
   - Archivos > 50MB requieren Git LFS
   - Si los videos son muy grandes, considera comprimirlos

2. **Dominio personalizado:** Puedes agregar un dominio personalizado en Vercel:
   - Settings → Domains → Add Domain

3. **Variables de entorno:** Si necesitas configuraciones especiales, agrégalas en:
   - Vercel Dashboard → Project Settings → Environment Variables

---

## ✅ Checklist Pre-Deploy

- [x] Repositorio Git inicializado
- [x] Commit inicial creado
- [ ] Repositorio creado en GitHub
- [ ] Código subido a GitHub
- [ ] Proyecto conectado en Vercel
- [ ] Deploy exitoso
- [ ] Demo accesible en la URL de Vercel
- [ ] Videos cargando correctamente
- [ ] Probar en mobile y desktop

---

**¿Necesitas ayuda?** Revisa los logs en Vercel Dashboard o la consola del navegador.

