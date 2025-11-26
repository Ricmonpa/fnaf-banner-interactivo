# 🚀 FNAF2 BANNER - PRE-FLIGHT CHECKLIST

## ✅ VALIDACIONES OBLIGATORIAS ANTES DE LAUNCH

### 1. TEST LOCAL (Cloudflare Pages)
- [ ] Acceder a: `https://fnaf2-banner-hosted.pages.dev/`
- [ ] Verificar que todos los videos cargan correctamente
- [ ] Verificar transiciones entre estados (Poster → Intro → Menu → Player)
- [ ] Click en "VER MÁS" abre la URL de Universal en nueva pestaña
- [ ] Abrir DevTools Console y verificar log: `ClickTag capturado: https://www...`

### 2. TEST CON CLICKTAG SIMULADO (DV360 Mock)
- [ ] Acceder a: `https://fnaf2-banner-hosted.pages.dev/?clickTag=https://example.com/test`
- [ ] Abrir DevTools Console
- [ ] Verificar que el log muestra: `ClickTag capturado: https://example.com/test`
- [ ] Click en "VER MÁS" debe abrir `https://example.com/test` (NO la URL de Universal)
- [ ] ⚠️ **SI ABRE LA URL DE UNIVERSAL, EL CÓDIGO ESTÁ MAL**

### 3. TEST EN DV360 PREVIEW
- [ ] Subir el tag `DV360_TAG.html` como Custom Creative
- [ ] Activar "Preview" mode en DV360
- [ ] Verificar que el banner carga sin errores 404
- [ ] Click en "VER MÁS" debe redirigir a través del click tracker de DV360
- [ ] En Network Tab (DevTools), verificar que aparece una llamada a `ad.doubleclick.net/click` o similar

### 4. TEST CROSS-BROWSER (Sandbox Validation)

#### Chrome/Edge
- [ ] Banner carga correctamente
- [ ] Videos con autoplay funcionan
- [ ] "VER MÁS" abre popup sin bloqueadores
- [ ] Console sin errores críticos

#### Safari (Desktop)
- [ ] Banner carga correctamente
- [ ] Autoplay funciona (muted)
- [ ] "VER MÁS" abre popup

#### Mobile Safari (iOS)
- [ ] Layout responsive funciona
- [ ] Videos se reproducen inline (no fullscreen)
- [ ] Touch en "VER MÁS" funciona

#### Chrome Mobile (Android)
- [ ] Banner funciona correctamente
- [ ] Videos se reproducen
- [ ] Click en "VER MÁS" funciona

### 5. VALIDACIÓN DE PESO (Bandwidth Optimization)

```bash
# Ejecutar desde terminal en la carpeta del proyecto:
du -sh *
```

- [ ] Peso total del banner < 3MB (recomendado)
- [ ] Videos en formato MP4 H.264
- [ ] Imágenes JPG con compresión 80%+
- [ ] No hay assets duplicados

### 6. VALIDACIÓN DE TRACKING (DV360 Metrics)

Después de las primeras 100 impresiones en DV360:

- [ ] **Impressions** se están registrando
- [ ] **Clicks** se están registrando (cuando haces click en "VER MÁS")
- [ ] **CTR** es > 0% (si hay engagement)
- [ ] **Viewability** es > 50% (según estándar MRC)

⚠️ **SI CLICKS = 0** después de engagement real → El clickTag está fallando

---

## 🚨 TROUBLESHOOTING COMÚN

### Problema: "VER MÁS" no abre nada
**Causa:** Popup blocker o falta de `allow-popups` en sandbox  
**Solución:** Verificar que el tag en DV360 tiene todos los atributos sandbox

### Problema: Videos no se reproducen en mobile
**Causa:** Falta `playsinline` attribute  
**Status:** ✅ Ya implementado en tu HTML (líneas 556, 563, 611)

### Problema: ClickTag siempre abre URL de Universal, no la de DV360
**Causa:** JavaScript no está capturando el parámetro de la URL  
**Solución:** Verificar que usaste el código corregido con `getParameterByName()`

### Problema: DV360 rechaza el tag
**Causa posible 1:** Iframe sin atributos correctos → Usar `DV360_TAG.html`  
**Causa posible 2:** Publisher whitelist → Solicitar PMP/PG deal

---

## 📊 MÉTRICAS DE ÉXITO (KPIs)

| Métrica | Target | Actual |
|---------|--------|--------|
| Impressions | 100% | ___% |
| Click-through Rate | > 0.5% | ___% |
| Video Completion (Intro) | > 30% | ___% |
| Character Selection | > 10% | ___% |
| "VER MÁS" Clicks | > 5% | ___% |

---

## ✅ SIGN-OFF

- [ ] **Tech Lead:** Código revisado y aprobado
- [ ] **QA:** Todos los tests pasados
- [ ] **Ad Ops:** Tag subido a DV360 y testeado
- [ ] **Cliente (Universal):** Preview aprobado
- [ ] **Campaign Manager:** Listo para launch

**Launch Date:** _______________  
**Approved by:** _______________

