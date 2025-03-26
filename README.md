# Proyecto Reaper - Configuración para Música en Vivo

Plantilla preconfigurada para **REAPER** optimizada para música en vivo (worship/iglesias). Incluye routing avanzado, efectos y soporte para tarjetas de audio integradas.

![screenshot1](https://github.com/llromerorr/control-de-audio-iglesia/blob/87e4ada81bd2e3ff7bbf13c63bfc9442ac19cf7d/screenshots/screenshot1.PNG)
![screenshot1](https://github.com/llromerorr/control-de-audio-iglesia/blob/87e4ada81bd2e3ff7bbf13c63bfc9442ac19cf7d/screenshots/screenshot2.PNG)

---

## 📥 Descarga e Instalación

1. **Descargar el archivo portable**:
   - Ve a la sección [Releases](https://github.com/llromerorr/control-de-audio-iglesia/releases) del repositorio.
   - Descarga el archivo `reaper.zip` que incluye:
     - REAPER en versión portable (no requiere instalación).
     - Plugins/VST esenciales preconfigurados.
     - Carpeta `¡¡INSTALADORES!!` con herramientas adicionales.

2. **Extraer el archivo**:
   - Descomprime `reaper.zip` en una carpeta de tu elección.

3. **Instalar dependencias** (opcional pero recomendado):
   - Abre la carpeta `¡¡INSTALADORES!!` y ejecuta:
     - `ASIO4ALL_2_16.exe`: Para baja latencia de audio (esencial si usas la tarjeta de audio integrada).
     - `vcredist\*.exe`: Redistribuibles de Visual C++ (requeridos por algunos plugins).
     - `sws-2.14.0.3-Windows-x64.exe`: Extiende funcionalidades de REAPER.
     - `Optimizer-16.7.exe`: Optimiza el sistema para audio en tiempo real.

---

## 🎛️ Configuración Inicial

### 🔌 Configuración de audio en Windows
1. **Antes de abrir REAPER**:
   - Ve a `Configuración de sonido de Windows > Entrada`.
   - **Coloca el volumen en 0%** y luego sube gradualmente hasta que las voces/guitarra tengan un nivel claro (sin distorsión).
   - *Razón*: El proyecto usa alta ganancia para minimizar ruido de tarjetas de audio integradas.

### 🎚️ Abrir el proyecto
1. Ejecuta `reaper.exe` y abre `Proyecto.RPP`.
2. **Routing predefinido**:
   - **Canal LEFT (1)**: Entrada de voz (EQ + compresión dedicada).
   - **Canal RIGHT (2)**: Entrada de guitarra (efectos limpios/distorsión).
   - *No es necesario reconfigurar las entradas físicas*.

---

## 🎹 Estructura del Proyecto

### Canales principales
| Canal         | Descripción                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **LEFT**      | Entrada de voces (ecualización y compresión dedicada).                     |
| **RIGHT**     | Entrada de guitarra (limpia o con distorsión).                             |
| **Reverb**    | Efecto de reverberación compartida para todos los instrumentos.            |
| **Voz**       | Procesamiento avanzado para voces (EQ, compresor, limitador).              |
| **Bass**      | Bajo virtual (Ample Bass P Lite II) con ajustes predefinidos.              |
| **Piano**     | Piano acústico (Keyzone Classic) con reverb y splits MIDI.                 |
| **Organo**    | Sonido de órgano moderno (Surge XT) controlado por modulación MIDI.        |

### Configuración MIDI
- **Canal 1**: Piano con release largo + reverb (ideal para baladas).
- **Canal 2**: Piano + pad coral (para rellenar armonías).
- **Canal 3**: Bajo (C1-E3) + piano con release corto (para ritmos rápidos).
- **Canal 4**: Bajo + sintetizador tipo órgano (control de volumen vía modulación MIDI).
- **Canal 5**: Mezcla de bajo, piano corto y órgano (para capas complejas).

---

## 🔧 Solución de Problemas

| Problema               | Solución                                                                 |
|------------------------|--------------------------------------------------------------------------|
| **Plugins no detectados** | Revisa `Opciones > Preferencias > Plugins > VST` y añade `Reaper\Plugins\FX\UserPlugins` manualmente. |
| **Ruido/feedback**      | Mantén el volumen de entrada en Windows ≤10% recomendablemente 1% y ajusta ganancia en REAPER SOLO SI EN CASO DE SER NECESARIO. |
| **Latencia alta**       | Usa ASIO4ALL con buffer ≤256 muestras. Cierra navegadores/antivirus.     |

---

## 📌 Notas Finales
- **Créditos**: Incluye plugins gratuitos (Surge XT, Keyzone Classic).
- **Personalización**: Modifica los presets de EQ en `Voz` y `Guitarra` según tu micrófono/instrumento.
- **Soporte**: Reporta issues en [GitHub](https://github.com/llromerorr/control-de-audio-iglesia).