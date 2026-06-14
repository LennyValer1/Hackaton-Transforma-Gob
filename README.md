# 🗺️ OncoRuta Mujer Inteligente

> **Hackatón TransformaGob 2026 — Reto INEN**  
> Experiencia de diagnóstico oportuno, equitativo, inclusivo e intercultural

---

## 📋 Descripción del proyecto

**OncoRuta** es una extensión modular de la Plataforma del Paciente del INEN (`plataforma.inen.sld.pe`) que guía a mujeres de 30 a 65 años en situación de vulnerabilidad a través de su proceso de diagnóstico de cáncer de mama y cérvix, eliminando la fragmentación, las demoras y las barreras culturales que hoy les impiden llegar a un diagnóstico oportuno.

La solución **no reemplaza los sistemas existentes del INEN** — se integra como un nuevo módulo sobre la plataforma ya operativa, leyendo datos del SISINEN vía API REST.

---

## 🎯 El problema que resuelve

Las pacientes del INEN, especialmente las provenientes de provincia, enfrentan cuatro barreras invisibles:

| # | Barrera | Impacto |
|---|---------|---------|
| 1 | **Demoras en el proceso** | Semanas de espera sin saber qué paso sigue |
| 2 | **Fragmentación del proceso** | La paciente no sabe en qué etapa está ni cuándo ir |
| 3 | **Barreras culturales** | Indicaciones médicas solo en español, sin soporte quechua |
| 4 | **Sin red de apoyo digital** | Familiares cuidadores sin visibilidad del proceso |

> Solo el 30% de pacientes de provincia llega a su primera cita de diagnóstico sin haber faltado antes. *(INEN 2024)*

---

## 👩‍⚕️ Usuarias objetivo (Personas)

| Persona | Perfil | Necesidad principal |
|---------|--------|---------------------|
| **María** | 52 años, Ayacucho, quechua/español, nivel digital básico | Reducir viajes innecesarios a Lima, entender indicaciones |
| **Rosa** | 38 años, Lima, nivel digital intermedio | Gestionar citas desde el celular, recordatorios automáticos |
| **Juana** | 68 años, Huancavelica, nivel digital muy bajo | Interfaz simple, letras grandes, apoyo audiovisual |
| **Ana** | 45 años, Lima, familiar cuidadora, nivel alto | Seguimiento centralizado, acceso remoto al estado de la paciente |
| **Carmen** | 50 años, voluntaria sobreviviente | Canal para orientar a nuevas pacientes |

**Foco prioritario:** María + Ana — el caso más complejo y de mayor impacto.

---

## 💡 La solución: módulos de OncoRuta

### 01 · Mi Ruta Oncológica
Dashboard visual de progreso que muestra en qué paso del proceso diagnóstico se encuentra la paciente:

```
[Admisión ✓] → [Especialista ✓] → [Exámenes ⏳] → [Resultados ○] → [Diagnóstico ○]
```

Incluye: próxima cita con fecha, hora y lugar; lista de documentos a llevar; indicación de si debe ir presencialmente.

### 02 · Recordatorios SMS / WhatsApp
Alertas automáticas en **español y quechua**, enviadas 24h y el mismo día de cada cita. Incluye recordatorio de documentos 48h antes.

### 03 · Acceso para cuidadora
Código compartible (ej. `R-4829`) que permite a la familiar cuidadora ver la ruta de la paciente en modo solo lectura, sin necesitar su contraseña.

### 04 · Interfaz intercultural
Botón ES / QU que cambia el contenido clave a quechua en tiempo real. Diseño accesible: contraste alto, texto legible, lenguaje simple.

---

## 🖥️ Prototipo

El prototipo es un archivo HTML navegable que simula la extensión de la Plataforma del Paciente INEN con el módulo OncoRuta integrado.

**Cómo abrirlo:**
1. Descargar el archivo `onco_ruta_prototipo_inen.html`
2. Abrirlo en cualquier navegador (Chrome, Edge, Firefox)
3. No requiere instalación ni conexión a internet

**Funcionalidades demostrables:**
- Navegar entre todos los módulos del sidebar
- Cambiar idioma ES ↔ QU en tiempo real
- Activar/desactivar recordatorios con switches
- Copiar el código de acceso familiar
- Ver historial de citas y resultados simulados

---

## ⚙️ Viabilidad técnica

| Componente | Detalle |
|-----------|---------|
| **Plataforma base** | Extensión de `plataforma.inen.sld.pe` (ya operativa) |
| **Integración backend** | API REST al SISINEN — solo lectura, sin modificar datos |
| **Notificaciones** | Gateway SMS/WhatsApp vía proveedor nacional (modelo GovTech) |
| **Autenticación** | ID Perú ya integrado — sin nueva infraestructura |
| **Accesibilidad** | Cumple Lineamiento PCM 001-2025 para plataformas accesibles |

---

## 🌱 Apertura y ética digital

- **Reutilizable:** Arquitectura modular adaptable a otros institutos del MINSA
- **Privacidad:** Acceso familiar solo lectura. Datos clínicos no salen del SISINEN
- **Inclusión:** Soporte quechua, texto grande, contraste accesible, navegación simple
- **IA responsable:** Sin modelos opacos. Lógica de negocio trazable y auditable

---

## 🗓️ Hoja de ruta

```
Fase 1 (0–3 meses)    →  Fase 2 (3–6 meses)     →  Fase 3 (6–12 meses)
─────────────────────    ──────────────────────      ───────────────────────
MVP                       Expansión                   Escala nacional
• Dashboard Mi Ruta       • WhatsApp + quechua        • Replicación en MINSA
• Recordatorios SMS       • Módulo cuidadora          • Open source del módulo
• Piloto 100 pacientes    • Feedback pacientes        • Evaluación de impacto
• Validación INEN TI      • Escala 1,000 pacientes    • Modelo GovTech
```

> **Costo Fase 1:** Bajo — reutiliza infraestructura INEN existente. Aprox. 3 meses de 1 desarrollador fullstack.

---

## 📊 Impacto esperado

| Métrica | Estimado | Base |
|---------|----------|------|
| Reducción de citas perdidas | **40%** | Recordatorios automáticos |
| Pacientes de provincia que evitan viajes innecesarios | **60%** | Información de proceso en tiempo real |
| Más familias cuidadoras involucradas | **3x** | Acceso compartido sin contraseña |
| Beneficiarias directas (INEN/año) | **~18,000** | ~7,200 de provincia |

---

## 📁 Archivos del proyecto

```
📦 OncoRuta
 ┣ 📄 onco_ruta_prototipo_inen.html   ← Prototipo navegable (abrir en browser)
 ┣ 📊 OncoRuta_TransformaGob2026.pptx ← Presentación 10 diapositivas
 ┗ 📄 README.md                        ← Este archivo
```

---

## 👥 Equipo

**Equipo OncoRuta**  
Hackatón TransformaGob 2026 — Reto INEN  
Lima, Perú · Junio 2026

---

*"Un diagnóstico oportuno cambia el pronóstico. OncoRuta no reemplaza la medicina — guía a la mujer para llegar a tiempo."*
