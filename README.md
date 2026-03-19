# 📓 Cuaderno Único Docente 2026

> PWA educativa completa para la gestión diaria del trabajo docente

[![PWA](https://img.shields.io/badge/PWA-Enabled-blue)](https://web.dev/progressive-web-apps/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Mobile](https://img.shields.io/badge/Mobile-First-orange)](https://www.mobile-first.com/)

## 🎯 Descripción

**Cuaderno Único Docente 2026** es una Progressive Web App diseñada específicamente para docentes de educación básica en Panamá (Pre-K a 6° grado). Permite gestionar de forma integral todas las actividades académicas y administrativas desde cualquier dispositivo, sin necesidad de conexión a internet.

## ✨ Características Principales

### 📊 Dashboard Central
- KPIs en tiempo real (estudiantes, asistencia, eventos, balance)
- Gráfico de tendencias de asistencia (últimos 30 días)
- Próximos eventos y acciones rápidas
- Balance económico de actividades

### 👥 Gestión de Estudiantes
- Registro completo por grado (Pre-K a 6°)
- Importación masiva desde CSV
- **Bitácora individual** con 6 tipos de entradas:
  - 📋 General
  - ⚠️ Disciplina
  - 🏥 Salud/Enfermedad
  - 📚 Académico
  - 📞 Contacto con Padres
  - 🎯 Logros/Positivos

### 📋 Registro de Asistencia
- Toma rápida por grado y fecha
- Estados: Presente (P), Ausente (A), Tardanza (T)
- Historial completo con filtros
- Estadísticas por período

### 📅 Calendario de Eventos
- Visualización mensual interactiva
- Múltiples eventos por fecha
- Tipos: Académico, Festivo, Reunión, Evaluación, Especial
- Edición y eliminación

### 🔍 Búsqueda Global
- Búsqueda instantánea en 9 secciones
- Navegación directa con botón "Ir"
- Resultados en tiempo real

### 📄 Exportación Selectiva
- **PDF**: 12 secciones con formato profesional
- **Excel/CSV**: Estudiantes, asistencia, actividades
- **JSON**: Backup completo del cuaderno

### ⚙️ Sistema Modular
- **Funcionalidades Core** (siempre activas):
  - Inicio, Estudiantes, Asistencia, Backup
- **Funcionalidades Opcionales** (activar/desactivar):
  - Dashboard, Calendario, Reuniones, Comisiones, Visitas, etc.
- **Funcionalidades Personalizadas**:
  - Crea tus propias secciones con ícono y color
  - Sistema de registros independiente
  - Ejemplos: Biblioteca 📚, Proyectos Especiales 🎭, Arte 🎨

### 📝 Otras Funcionalidades
- **Reuniones**: Registro de temas, participantes y acuerdos
- **Comisiones**: Gestión de comisiones de trabajo
- **Visitas de Estudio**: Control de salidas pedagógicas
- **Permisos**: Registro de permisos docentes
- **Circulares**: Archivo de circulares recibidas
- **Actividades Económicas**: Control de ingresos y egresos
- **Inventario**: Gestión de materiales y recursos
- **Asuntos Varios**: Notas y pendientes
- **Horario**: Programación semanal

## 🚀 Instalación

### Opción 1: Usar Directamente (Recomendado)
1. Descarga el archivo `cuaderno-NAVEGACION-ARREGLADA.zip`
2. Descomprime en una carpeta
3. Abre `index.html` en tu navegador
4. ¡Listo para usar!

### Opción 2: Servidor Local
```bash
# Usando Python
python -m http.server 8000

# Usando Node.js
npx http-server -p 8000

# Luego abre: http://localhost:8000
```

### Opción 3: Instalar como PWA
1. Abre la app en Chrome/Edge
2. Click en el ícono de instalación en la barra de direcciones
3. Acepta instalar
4. Ahora tienes acceso desde el escritorio/inicio

## 📱 Compatibilidad

- ✅ Chrome/Edge (Desktop + Móvil)
- ✅ Firefox
- ✅ Safari (iOS + macOS)
- ✅ Android WebView
- ✅ Funciona 100% offline

## 🛠️ Stack Técnico

- **Frontend**: Vanilla JavaScript (inline)
- **Estilos**: CSS3 personalizado con gradientes
- **Persistencia**: localStorage API
- **Gráficos**: Chart.js 4.4.0 (CDN)
- **PWA**: Service Worker + Manifest
- **Sin dependencias**: 0 npm packages, 0 frameworks

## 📂 Estructura del Proyecto
```
cuaderno/
├── index.html          # Aplicación principal (todo-en-uno)
├── css/
│   └── styles.css      # Estilos completos (~1400 líneas)
├── icon-512x512.png    # Ícono kawaii de la app
├── manifest.json       # Configuración PWA
└── sw.js              # Service Worker (v7)
```

## 🎨 Características de Diseño

- **Mobile-first**: Diseñado primero para dispositivos móviles
- **Responsive**: Breakpoint en 768px
- **Kawaii**: Portada con ícono amigable y colores vibrantes
- **Accesible**: Touch-friendly, botones grandes
- **Temas**: Gradientes morados y colores distintivos por sección

## 💾 Gestión de Datos

### localStorage Key
```javascript
cuadernoDocenteDB = {
  datosDocente: {...},           // Información del docente
  estudiantes: {...},            // Por grado
  asistencia: {...},             // Por grado_fecha
  eventos: {...},                // Por fecha
  bitacoraEstudiantes: {...},    // Por ID estudiante
  configuracionFuncionalidades: {...},
  reuniones: [],
  comisiones: [],
  visitas: [],
  permisos: [],
  circulares: [],
  actividades: [],
  inventario: [],
  asuntos: [],
  horario: []
}
```

### Backup y Restauración
- Exportación completa a JSON
- Importación con validación
- Compatible entre dispositivos

## 🔒 Privacidad

- ✅ **100% Local**: Todos los datos se almacenan en tu dispositivo
- ✅ **Sin servidor**: No hay conexión a servidores externos
- ✅ **Sin tracking**: No hay analytics ni seguimiento
- ✅ **Sin internet**: Funciona completamente offline
- ✅ **Tú controlas**: Exporta, borra o migra tus datos cuando quieras

## 📖 Uso Rápido

### Primer Uso
1. **Portada**: Edita tus datos (Docente, Centro Educativo, Grado)
2. **Estudiantes**: Agrega estudiantes manualmente o importa CSV
3. **Asistencia**: Selecciona grado y fecha, marca asistencia
4. **Dashboard**: Ve estadísticas en tiempo real

### Uso Diario
1. Abre la app
2. **Dashboard** → Ver resumen del día
3. **Asistencia** → Tomar asistencia
4. **Bitácora** → Registrar eventos de estudiantes
5. **Calendario** → Agregar eventos próximos

### Personalización
1. **Funcionalidades** → ⚙️ Configurar
2. Activa/desactiva lo que necesites
3. Crea funcionalidades personalizadas
4. Guarda cambios

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add: AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Áreas de Mejora
- [ ] Sincronización en la nube (opcional)
- [ ] Modo oscuro
- [ ] Más tipos de gráficos
- [ ] Notificaciones push
- [ ] Exportación de bitácoras individuales a PDF
- [ ] Plantillas de funcionalidades personalizadas
- [ ] Importación de horarios desde Excel

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver `LICENSE` para más detalles.

## 👨‍🏫 Desarrollado Por

**José R. White**  
Docente - Panamá  
Grados: Pre-K a 6°

---

## 📊 Versiones

- **v1.0** (Fase 1): Base + Historial + Edición
- **v2.0** (Fase 2): Búsqueda global + Exportación PDF/Excel
- **v3.0** (Fase 3): Dashboard Central con KPIs y gráficos
- **v4.0** (Fase 4): Bitácora individual de estudiantes
- **v5.0** (Fase 5): Sistema modular de funcionalidades ← **ACTUAL**

---

## 🙏 Agradecimientos

- A todos los docentes que dedican su tiempo y pasión a la educación
- A la comunidad de desarrollo web por las herramientas open source
- Chart.js por los gráficos hermosos y fáciles de usar

---

## 📞 Soporte

Para reportar bugs, solicitar features o hacer preguntas:
- Abre un [Issue](https://github.com/tuusuario/cuaderno-docente/issues)
- O contacta directamente al desarrollador

---

**⭐ Si este proyecto te es útil, considera darle una estrella en GitHub**

---

_Hecho con ❤️ para la comunidad educativa de Panamá 🇵🇦_