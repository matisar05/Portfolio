# Portfolio Profesional - Guía de Deployment

## 🚀 Opciones de Deployment

### Opción 1: GitHub Pages (Recomendada - Gratis)

1. **Crear repositorio en GitHub**:
   ```bash
   cd /home/ffaka/Escritorio/Portfolio
   git init
   git add .
   git commit -m "Initial commit: Portfolio profesional"
   ```

2. **Crear repositorio en GitHub.com**:
   - Ve a https://github.com/new
   - Nombre: `Portfolio` o `portfolio-web`
   - NO inicialices con README

3. **Subir código**:
   ```bash
   git remote add origin https://github.com/matisar05/Portfolio.git
   git branch -M main
   git push -u origin main
   ```

4. **Activar GitHub Pages**:
   - Ve a Settings → Pages
   - Source: Deploy from a branch
   - Branch: main → / (root)
   - Save

5. **Tu portfolio estará en**: `https://matisar05.github.io/Portfolio/`

---

### Opción 2: Netlify (Muy fácil - Gratis)

1. **Método Drag & Drop**:
   - Ve a https://app.netlify.com/drop
   - Arrastra la carpeta `Portfolio`
   - ¡Listo! URL generada automáticamente

2. **Personalizar dominio** (opcional):
   - Site settings → Change site name
   - Cambia a: `matias-sarasola` 
   - URL será: `https://matias-sarasola.netlify.app`

---

### Opción 3: Vercel (Profesional - Gratis)

1. **Instalar Vercel CLI** (opcional):
   ```bash
   npm install -g vercel
   cd /home/ffaka/Escritorio/Portfolio
   vercel
   ```

2. **O usar la web**:
   - Ve a https://vercel.com/new
   - Importa tu repositorio de GitHub
   - Deploy automático

---

## 📧 Cómo Compartir tu Portfolio

Una vez desplegado, puedes:

1. **Agregar el link en LinkedIn**:
   - Perfil → Información de contacto → Sitio web
   - Agregar: `https://tu-portfolio-url.com`

2. **Agregar en GitHub**:
   - Perfil → Edit profile
   - Website: Agregar URL

3. **Compartir en CV**:
   - Agregar link en sección de "Información de contacto"

4. **Email signature**:
   - Agregar link en firma de email

---

## 🔧 Mantenimiento

### Actualizar Proyectos

En `index.html`, busca la sección `<!-- Projects Section -->` y agrega:

```html
<div class="project-card">
    <div class="project-header">
        <div class="project-folder">
            <!-- SVG icon -->
        </div>
        <div class="project-links">
            <a href="GITHUB_URL" target="_blank">
                <!-- SVG icon -->
            </a>
        </div>
    </div>
    <h3 class="project-title">Nombre del Proyecto</h3>
    <p class="project-description">
        Descripción del proyecto...
    </p>
    <div class="project-tech">
        <span class="tech-tag">Tech1</span>
        <span class="tech-tag">Tech2</span>
    </div>
</div>
```

### Actualizar Información de Contacto

En `index.html`, busca `<!-- Contact Section -->` y modifica según necesites.

---

## ✅ Checklist Pre-Deploy

- [ ] Verificar todos los links funcionan
- [ ] Revisar ortografía
- [ ] Probar en móvil
- [ ] Verificar imágenes de certificaciones cargan
- [ ] Comprobar que email y WhatsApp funcionan
- [ ] Revisar que proyectos estén públicos en GitHub

---

## 🆘 Troubleshooting

**Problema**: Las imágenes de certificaciones no cargan
- **Solución**: Las URLs de Credly están correctas, verificar conexión a internet

**Problema**: Animaciones no funcionan
- **Solución**: Verificar que `script.js` se carga correctamente

**Problema**: Diseño se ve mal en móvil
- **Solución**: Los breakpoints están configurados, verificar viewport meta tag

---

## 📱 Testing en Diferentes Dispositivos

Para probar localmente en tu teléfono:

1. Asegúrate que tu PC y teléfono estén en la misma red WiFi
2. Encuentra tu IP local: `ip addr show`
3. En tu teléfono, abre: `http://TU_IP:8000`

---

¡Tu portfolio está listo para impresionar! 🎉
