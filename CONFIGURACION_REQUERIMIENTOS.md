# 📋 GUÍA DE CONFIGURACIÓN Y REQUERIMIENTOS

## 1. REQUERIMIENTOS TÉCNICOS

### Para Usuarios Finales (Investigadores)

#### Hardware Mínimo
- **Procesador**: Intel Core i5 o equivalente
- **RAM**: 4 GB mínimo (8 GB recomendado)
- **Almacenamiento**: 500 MB disponibles
- **Conexión**: Internet de banda ancha (5 Mbps mínimo)

#### Software Requerido
- **Navegador**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **JavaScript**: Habilitado (obligatorio)
- **Cookies**: Habilitadas (para almacenamiento local)
- **Sistema Operativo**: Windows 7+, macOS 10.12+, Linux (cualquier distribución moderna)

### Para Administradores/Desarrolladores

#### Herramientas Recomendadas
- **Git**: v2.30+
- **Node.js**: v18+ (opcional, para servidor local)
- **npm o yarn**: Última versión
- **Editor de código**: VS Code, Sublime Text, o similar
- **Terminal**: Bash, PowerShell, o Zsh

#### Dependencias
- **HTML5**: Soporte nativo en navegadores modernos
- **CSS3**: Soporte nativo en navegadores modernos
- **JavaScript ES6+**: Soporte nativo en navegadores modernos
- **LocalStorage API**: Soporte nativo en navegadores modernos

## 2. CONFIGURACIÓN INICIAL

### Paso 1: Preparar Cuenta GitHub

#### Crear Personal Access Token (PAT)

1. **Acceder a GitHub**
   - Ve a https://github.com/settings/tokens
   - O: GitHub → Settings → Developer settings → Personal access tokens

2. **Generar nuevo token**
   - Haz clic en "Generate new token"
   - Dale un nombre descriptivo: "Generador Landing Pages"

3. **Seleccionar permisos (scopes)**
   ```
   ✓ repo (acceso completo a repositorios privados y públicos)
   ✓ workflow (permisos para GitHub Actions)
   ✓ user:email (acceso a email)
   ```

4. **Copiar y guardar el token**
   - ⚠️ **IMPORTANTE**: Copia el token inmediatamente
   - No podrás verlo de nuevo
   - Guárdalo en un lugar seguro (gestor de contraseñas)

#### Ejemplo de Token
```
ghp_16C7e42F292c6912E7710c838347Ae178B4a
```

### Paso 2: Preparar Información Personal

#### Información Obligatoria
- [ ] Nombre completo
- [ ] Institución (BUAP, UNAM, etc.)
- [ ] Correo electrónico institucional
- [ ] ORCID (formato: 0000-0000-0000-0000)
- [ ] Resumen de investigación (50-200 palabras)

#### Información Recomendada
- [ ] Departamento/Facultad
- [ ] Teléfono
- [ ] CVU SNII
- [ ] Google Scholar (URL)
- [ ] ResearchGate (URL)
- [ ] LinkedIn (URL)
- [ ] Foto profesional (URL)

### Paso 3: Preparar Producción Académica

#### Patentes (Mínimo 1 recomendado)
Para cada patente necesitas:
- Título
- Número de registro (ej: MX 2024 123456)
- Fecha de registro
- Descripción breve

**Dónde encontrar información:**
- IMPI (Instituto Mexicano de la Propiedad Industrial): https://www.gob.mx/impi
- Búsqueda de patentes: https://www.impi.gob.mx/

#### Publicaciones (Mínimo 3 recomendadas)
Para cada publicación necesitas:
- Título del artículo
- DOI (Digital Object Identifier)
- Año de publicación
- Revista o conferencia

**Dónde encontrar información:**
- Google Scholar: https://scholar.google.com/
- CrossRef: https://www.crossref.org/
- PubMed: https://pubmed.ncbi.nlm.nih.gov/ (si aplica)

#### Libros/Capítulos (Mínimo 1 recomendado)
Para cada libro necesitas:
- Título
- ISBN
- Año de publicación
- Editorial

**Dónde encontrar información:**
- ISBN Search: https://www.isbn-search.org/
- Google Books: https://books.google.com/
- Editorial del libro

#### Tesis Supervisadas (Mínimo 2 recomendadas)
Para cada tesis necesitas:
- Título
- Nombre del estudiante
- Nivel (Licenciatura, Maestría, Doctorado)
- Año de conclusión

**Dónde encontrar información:**
- Registros de tu institución
- Sistema de bibliotecas
- Archivo de tesis

### Paso 4: Preparar Multimedia

#### Audios Narrados
**Especificaciones técnicas:**
- Formato: WAV o MP3
- Frecuencia de muestreo: 44.1 kHz
- Canales: Estéreo o Mono
- Duración: 30-60 segundos por patente
- Tamaño máximo: 10 MB por archivo
- Bitrate: 128-320 kbps

**Herramientas para crear audios:**
- Audacity (gratuito): https://www.audacityteam.org/
- Adobe Audition
- GarageBand (macOS)
- Vocaroo (online): https://vocaroo.com/

**Guía de narración:**
1. Escribe un guion de 30-60 segundos
2. Graba en ambiente silencioso
3. Usa micrófono de buena calidad
4. Normaliza el volumen
5. Exporta como WAV o MP3

#### Imágenes/Portadas
**Especificaciones técnicas:**
- Formato: PNG o JPG
- Resolución: 1920 x 1080 píxeles (Full HD)
- Tamaño máximo: 5 MB por imagen
- Compresión: Optimizada para web
- Profundidad de color: RGB o RGBA

**Herramientas para crear imágenes:**
- Canva (online): https://www.canva.com/
- Figma (online): https://www.figma.com/
- Adobe Photoshop
- GIMP (gratuito): https://www.gimp.org/
- Pixlr (online): https://pixlr.com/

**Dimensiones recomendadas:**
- Portada principal: 1920 x 1080 px
- Portadas de patentes: 1920 x 1080 px
- Miniaturas: 400 x 225 px

## 3. CONFIGURACIÓN DEL GENERADOR

### Instalación Local (Opcional)

#### Opción A: Servidor Python
```bash
# Navega a la carpeta del generador
cd /ruta/a/generador-landing-investigadores

# Inicia servidor Python 3
python -m http.server 8000

# Accede a http://localhost:8000
```

#### Opción B: Servidor Node.js
```bash
# Instala http-server globalmente
npm install -g http-server

# Navega a la carpeta
cd /ruta/a/generador-landing-investigadores

# Inicia servidor
http-server

# Accede a http://localhost:8080
```

#### Opción C: Live Server (VS Code)
1. Instala extensión "Live Server" en VS Code
2. Haz clic derecho en index.html
3. Selecciona "Open with Live Server"

### Configuración de Navegador

#### Habilitar JavaScript
- **Chrome/Edge**: Siempre habilitado
- **Firefox**: Siempre habilitado
- **Safari**: Preferences → Security → Habilitar JavaScript
- **Internet Explorer**: Tools → Internet Options → Security → Custom Level

#### Habilitar Cookies/LocalStorage
- **Chrome/Edge**: Siempre habilitado
- **Firefox**: Siempre habilitado
- **Safari**: Preferences → Privacy → Permitir cookies
- **Internet Explorer**: Tools → Internet Options → Privacy

#### Limpiar Caché (si hay problemas)
- **Chrome**: Ctrl+Shift+Delete (o Cmd+Shift+Delete en Mac)
- **Firefox**: Ctrl+Shift+Delete (o Cmd+Shift+Delete en Mac)
- **Safari**: Develop → Empty Caches
- **Edge**: Ctrl+Shift+Delete (o Cmd+Shift+Delete en Mac)

## 4. SEGURIDAD Y PRIVACIDAD

### Protección de Datos Personales

#### Datos que se almacenan LOCALMENTE
- ✅ Información personal
- ✅ Credenciales académicas
- ✅ Producción académica
- ✅ Referencias a multimedia

**Ubicación**: LocalStorage del navegador
**Acceso**: Solo tú desde tu navegador
**Duración**: Hasta que limpies el caché

#### Datos que se envían a GitHub
- ✅ Información personal (para el landing page)
- ✅ Producción académica (para el landing page)
- ✅ Multimedia (si la subes a GitHub)

**Ubicación**: Repositorio GitHub público
**Acceso**: Público (visible para todos)
**Duración**: Mientras mantengas el repositorio

#### Datos que NUNCA se almacenan
- ❌ Personal Access Token (PAT)
- ❌ Contraseñas
- ❌ Información de tarjeta de crédito
- ❌ Datos biométricos

### Recomendaciones de Seguridad

1. **Usa PAT con permisos limitados**
   - Solo selecciona `repo` y `workflow`
   - Evita seleccionar `admin:repo_hook` u otros permisos amplios

2. **Revoca el PAT después de usar**
   - Ve a GitHub → Settings → Developer settings → Personal access tokens
   - Haz clic en "Delete" junto al token que usaste

3. **No compartas tu PAT**
   - Nunca lo publiques en redes sociales
   - No lo incluyas en emails
   - No lo compartas con colegas

4. **Usa navegador seguro**
   - Mantén tu navegador actualizado
   - Usa HTTPS (siempre)
   - Desactiva extensiones sospechosas

5. **Protege tu cuenta GitHub**
   - Usa autenticación de dos factores (2FA)
   - Contraseña fuerte y única
   - Revisa actividad de sesiones

## 5. SOLUCIÓN DE PROBLEMAS

### Problema: "No se guardan mis datos"
**Solución:**
1. Verifica que JavaScript esté habilitado
2. Limpia el caché del navegador
3. Intenta en modo incógnito
4. Usa un navegador diferente

### Problema: "No puedo conectar con GitHub"
**Solución:**
1. Verifica tu conexión a internet
2. Comprueba que el PAT sea válido
3. Verifica que el usuario de GitHub sea correcto
4. Asegúrate de tener permisos `repo` en el PAT

### Problema: "El landing page no se publica"
**Solución:**
1. Espera 2-5 minutos (GitHub Pages procesa)
2. Verifica que GitHub Pages esté habilitado
3. Revisa la rama `main` en GitHub
4. Limpia el caché del navegador

### Problema: "Los archivos multimedia no se cargan"
**Solución:**
1. Verifica el tamaño (máximo 10 MB)
2. Comprueba el formato (WAV, MP3 para audio; PNG, JPG para imágenes)
3. Intenta subir nuevamente
4. Usa URLs directas en lugar de rutas relativas

### Problema: "Olvidé mi PAT"
**Solución:**
1. Genera uno nuevo en GitHub
2. Elimina el antiguo
3. Usa el nuevo en el generador

## 6. MANTENIMIENTO Y ACTUALIZACIONES

### Actualizar Información

**Cada 3 meses:**
- Revisa y actualiza tu información personal
- Agrega nuevas publicaciones
- Actualiza tus patentes

**Cada 6 meses:**
- Regenera tu landing page
- Revisa tu puntuación SNII/VIEP
- Actualiza multimedia

**Anualmente:**
- Revisa tu presencia digital
- Actualiza perfiles académicos
- Genera reporte de métricas

### Backup de Datos

```bash
# Clonar tu repositorio de landing page
git clone https://github.com/tu-usuario/tu-landing-page.git backup-landing

# Hacer backup local
cp -r tu-landing-page/ backup-landing-$(date +%Y-%m-%d)
```

### Monitoreo de Cambios

```bash
# Ver historial de cambios
git log --oneline

# Ver cambios recientes
git diff HEAD~1

# Ver estado actual
git status
```

## 7. CONTACTO Y SOPORTE

### Reportar Problemas
- Abre un issue en GitHub
- Incluye: navegador, versión, pasos para reproducir
- Adjunta capturas de pantalla si es posible

### Solicitar Características
- Crea un issue con etiqueta "enhancement"
- Describe la característica deseada
- Explica por qué sería útil

### Contactar al Autor
- **Email**: [tu-email@institucion.edu.mx]
- **GitHub**: @filibertocandia
- **ORCID**: [tu-ORCID]

## 8. REFERENCIAS Y RECURSOS

### Documentación Oficial
- [GitHub Pages](https://pages.github.com/)
- [GitHub API](https://docs.github.com/en/rest)
- [ORCID](https://orcid.org/)
- [IMPI - Patentes](https://www.gob.mx/impi)

### Herramientas Útiles
- [ORCID Search](https://orcid.org/orcid-search/search)
- [DOI Lookup](https://www.crossref.org/)
- [ISBN Search](https://www.isbn-search.org/)
- [GitHub Token Generator](https://github.com/settings/tokens)

### Comunidades
- [Stack Overflow](https://stackoverflow.com/)
- [GitHub Community](https://github.community/)
- [Reddit r/github](https://www.reddit.com/r/github/)

---

**Última actualización:** 21 de enero de 2026  
**Versión:** 1.0  
**Autor:** Dr. Filiberto Candia García

*Para más información, consulta el README.md principal.*
