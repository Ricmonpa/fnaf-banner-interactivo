# Five Nights at Freddy's 2 - Banner Interactivo

Banner interactivo promocional para Five Nights at Freddy's 2 con flujo de estados y selección de personajes.

## 🚀 Deploy en Vercel

### Opción 1: Deploy desde GitHub (Recomendado)

1. **Crear repositorio en GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Versión estable - Lista para aprobación"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/fnaf-banner-interactivo.git
   git push -u origin main
   ```

2. **Conectar con Vercel:**
   - Ve a [vercel.com](https://vercel.com)
   - Inicia sesión con GitHub
   - Click en "Add New Project"
   - Importa el repositorio `fnaf-banner-interactivo`
   - Vercel detectará automáticamente la configuración
   - Click en "Deploy"

3. **Tu demo estará disponible en:**
   `https://tu-proyecto.vercel.app/demo.html`

### Opción 2: Deploy directo con Vercel CLI

```bash
# Instalar Vercel CLI (si no lo tienes)
npm i -g vercel

# En el directorio del proyecto
vercel

# Seguir las instrucciones
# - Login con tu cuenta
# - Aceptar configuración por defecto
# - Deploy
```

## 📁 Estructura del Proyecto

- `demo.html` - Versión demo con layout completo (banner + contenido simulado)
- `index.html` - Versión standalone del banner
- `CHECKPOINT.md` - Documentación de la versión estable

## 🔗 Links Importantes

- **Demo:** [Tu link de Vercel]/demo.html
- **Standalone:** [Tu link de Vercel]/index.html

## 📝 Notas

- Los videos deben estar en las rutas correctas (`Videos/`, `Animated Posters/`)
- El proyecto usa rutas relativas, asegúrate de mantener la estructura de carpetas
- Vercel soporta archivos estáticos HTML sin necesidad de build

## 🐛 Troubleshooting

Si los videos no cargan:
- Verifica que las rutas sean correctas
- Asegúrate de que los archivos estén en el repositorio
- Revisa la consola del navegador para errores

