# 🚀 Generador de Landing Pages para Investigadores

**Plataforma web para crear landing pages profesionales alineados con requisitos SNII 2025 y VIEP BUAP 2026**

## 📋 Descripción

Este generador permite a investigadores mexicanos crear automáticamente un landing page profesional y personalizado que:

- ✅ Integra información académica completa
- ✅ Incluye multimedia (audios, imágenes)
- ✅ Se vincula con GitHub Pages automáticamente
- ✅ Evalúa métricas SNII/VIEP en tiempo real
- ✅ Genera repositorio GitHub personalizado
- ✅ Cumple con estándares de accesibilidad WCAG 2.1

## 🎯 Características Principales

### 1. **Formulario Paso a Paso**
- Información personal y académica
- Credenciales SNII (ORCID, CVU, Google Scholar)
- Producción académica (patentes, publicaciones, libros, tesis)
- Carga de multimedia

### 2. **Evaluación de Métricas SNII/VIEP**
- Matriz de evidencia académica interactiva
- Puntuación de cumplimiento en tiempo real
- Recomendaciones personalizadas
- Checklist de requisitos

### 3. **Integración GitHub**
- Creación automática de repositorio
- Vinculación segura con Personal Access Token (PAT)
- Publicación en GitHub Pages
- Acceso a métricas y landing page

### 4. **Generación Automática**
- Landing page personalizado
- Página de métricas SNII/VIEP
- Repositorio GitHub configurado
- URLs públicas listas para compartir

## 🔧 Requisitos Técnicos

### Para Usuarios
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexión a internet
- Cuenta GitHub con acceso a Personal Access Token

### Para Instalación Local
- Node.js 18+ (opcional, para servidor local)
- Git
- Acceso a GitHub

## 📦 Instalación

### Opción 1: Usar en GitHub Pages (Recomendado)

```bash
# 1. Clonar este repositorio
git clone https://github.com/tu-usuario/generador-landing-investigadores.git
cd generador-landing-investigadores

# 2. Abrir en navegador
# Simplemente abre index.html en tu navegador
# O usa un servidor local:
python -m http.server 8000
# Luego accede a http://localhost:8000
```

### Opción 2: Usar Directamente Online

Accede a: `https://tu-usuario.github.io/generador-landing-investigadores/`

## 🚀 Guía de Uso

### Paso 1: Información Personal
1. Completa tu nombre, institución y departamento
2. Agrega tu correo electrónico y teléfono
3. Escribe un resumen de tu investigación
4. Haz clic en "Guardar Información"

### Paso 2: Credenciales Académicas
1. Ingresa tu ORCID (obligatorio)
2. Agrega CVU SNII si lo tienes
3. Vincula perfiles en Google Scholar, ResearchGate, LinkedIn
4. Sube una foto profesional (URL)
5. Haz clic en "Guardar Credenciales"

### Paso 3: Producción Académica

#### Patentes
- Título de la patente
- Número de registro (ej: MX 2024 123456)
- Fecha de registro
- Descripción breve

#### Publicaciones
- Título del artículo
- DOI (obligatorio)
- Año de publicación
- Revista/Conferencia

#### Libros/Capítulos
- Título del libro o capítulo
- ISBN
- Año de publicación
- Editorial

#### Tesis Supervisadas
- Título de la tesis
- Nombre del estudiante
- Nivel (Licenciatura, Maestría, Doctorado)
- Año de conclusión

### Paso 4: Multimedia
1. Carga audios narrados (WAV, MP3) - máximo 10MB
2. Carga imágenes/portadas (PNG, JPG) - recomendado 1920x1080px
3. Verifica que los archivos aparezcan en la lista

### Paso 5: Configuración GitHub
1. Ingresa tu usuario de GitHub
2. Genera un Personal Access Token:
   - Ve a GitHub → Settings → Developer settings → Personal access tokens
   - Haz clic en "Generate new token"
   - Selecciona permisos: `repo`, `workflow`
   - Copia el token y pégalo en el formulario
3. Ingresa un nombre para tu repositorio (ej: landing-investigador-2024)
4. Haz clic en "Generar Mi Landing Page"

### Paso 6: Evaluación de Métricas
- Completa el checklist de requisitos SNII/VIEP
- Observa tu puntuación de cumplimiento en tiempo real
- Lee las recomendaciones personalizadas
- Ajusta tu información según sea necesario

## 📊 Matriz de Evaluación SNII/VIEP

El generador evalúa 7 dimensiones clave:

| Dimensión | Requisito | Puntuación |
|-----------|-----------|-----------|
| **Identidad Global** | ORCID, CVU SNII, Google Scholar | 1 punto |
| **Publicaciones** | Mínimo 3 con DOI | 1 punto |
| **Libros/Capítulos** | Mínimo 1 con ISBN | 1 punto |
| **Formación de RH** | Mínimo 2 tesis supervisadas | 1 punto |
| **Patentes/Innovación** | Mínimo 1 patente registrada | 1 punto |
| **Multimedia** | Landing page con contenido multimedia | 1 punto |
| **Presencia Digital** | Perfiles en ResearchGate y LinkedIn | 1 punto |

**Puntuación Total: 7 puntos**
- **70-100%**: ✅ Cumple requisitos SNII/VIEP
- **50-69%**: ⚠️ Cumplimiento parcial
- **0-49%**: 🔄 En progreso

## 🔐 Seguridad

### Protección de Datos
- ✅ Tu Personal Access Token se usa **SOLO localmente** en tu navegador
- ✅ Nunca se almacena en servidores
- ✅ No se envía información sensible a terceros
- ✅ Todos los datos se procesan en el cliente

### Recomendaciones
1. **Usa un PAT con permisos limitados** (solo `repo` y `workflow`)
2. **Revoca el PAT después de usar el generador** si no lo necesitas
3. **No compartas tu PAT** con nadie
4. **Usa navegadores actualizados** para máxima seguridad

## 📁 Estructura del Proyecto

```
generador-landing-investigadores/
├── index.html              # Aplicación principal (todo en uno)
├── README.md              # Este archivo
├── .gitignore            # Configuración de Git
└── LICENSE               # Licencia del proyecto
```

## 🎨 Personalización

### Cambiar Colores
Edita las variables CSS en `index.html`:

```css
:root {
    --primary: #1e40af;        /* Azul principal */
    --secondary: #d97706;      /* Naranja secundario */
    --success: #059669;        /* Verde de éxito */
    --danger: #dc2626;         /* Rojo de error */
}
```

### Agregar Campos Adicionales
1. Abre `index.html` en un editor de texto
2. Busca la sección de formularios
3. Agrega nuevos `<div class="form-group">` con `<input>` o `<textarea>`
4. Actualiza el objeto `investigadorData` en JavaScript

## 🔗 Integración con Otros Repositorios

Este generador se integra con:

- **[dr-candia-landing](https://github.com/filibertocandia/dr-candia-landing)** - Ejemplo de landing page
- **[divulgacion-cientifica-manus](https://github.com/filibertocandia/divulgacion-cientifica-manus)** - Guía de implementación
- **[Metricas-SNII](https://github.com/filibertocandia/Metricas-SNII)** - Matriz de evaluación

## 📚 Documentación Relacionada

- [Guía de Divulgación Científica](https://filibertocandia.github.io/divulgacion-cientifica-manus/)
- [Métricas SNII/VIEP](https://filibertocandia.github.io/Metricas-SNII/)
- [Landing Page Ejemplo](https://filibertocandia.github.io/dr-candia-landing/)

## 🐛 Solución de Problemas

### El formulario no guarda datos
- Verifica que JavaScript esté habilitado en tu navegador
- Intenta limpiar el caché del navegador
- Usa un navegador diferente

### No puedo conectar con GitHub
- Verifica que tu PAT sea válido
- Asegúrate de tener permisos `repo` y `workflow`
- Revisa que tu usuario de GitHub sea correcto

### El landing page no se publica
- Espera 2-5 minutos para que GitHub Pages procese
- Verifica que GitHub Pages esté habilitado en configuración del repositorio
- Revisa la rama `main` en GitHub

### Los archivos multimedia no se cargan
- Verifica el tamaño de los archivos (máximo 10MB)
- Asegúrate de que los formatos sean WAV, MP3 (audio) o PNG, JPG (imágenes)
- Intenta subir los archivos nuevamente

## 💡 Mejores Prácticas

### Para Investigadores
1. **Completa todos los campos** - Aumenta tu puntuación SNII/VIEP
2. **Usa URLs válidas** - Verifica que tus enlaces a perfiles funcionen
3. **Actualiza regularmente** - Regenera tu landing page cuando agregues nuevas publicaciones
4. **Comparte tu landing page** - Incluye el enlace en tu CV y perfiles académicos

### Para Administradores
1. **Mantén el repositorio actualizado** - Sincroniza cambios regularmente
2. **Monitorea problemas** - Revisa issues y pull requests
3. **Documenta cambios** - Actualiza el README con nuevas características

## 🤝 Contribuciones

¿Quieres mejorar este generador? ¡Bienvenido!

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo licencia MIT. Ver `LICENSE` para más detalles.

## 👨‍💼 Autor

**Dr. Filiberto Candia García**
- Institución: BUAP
- ORCID: [Tu ORCID]
- Email: [Tu email]

## 📞 Soporte

Para preguntas o sugerencias:
- Abre un issue en GitHub
- Contacta al autor directamente
- Revisa la documentación en el repositorio

## 🔄 Historial de Cambios

### v1.0 (2026-01-21)
- ✅ Lanzamiento inicial
- ✅ Formulario completo paso a paso
- ✅ Evaluación de métricas SNII/VIEP
- ✅ Integración GitHub
- ✅ Generación automática de landing page

## 🎯 Roadmap Futuro

- [ ] Integración con API de GitHub para automatizar creación de repositorio
- [ ] Generación de PDF con métricas
- [ ] Exportar datos a formato JSON
- [ ] Plantillas de landing page personalizables
- [ ] Soporte para múltiples idiomas
- [ ] Análisis de impacto académico
- [ ] Integración con ORCID API
- [ ] Dashboard de seguimiento

---

**Última actualización:** 21 de enero de 2026  
**Versión:** 1.0  
**Estado:** Activo y funcional

*Este generador es parte del Ecosistema de Divulgación Científica Multimedia para Investigadores Mexicanos.*
