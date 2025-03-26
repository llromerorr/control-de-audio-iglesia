# Proyecto Reaper - Configuración para Música en Vivo

Plantilla preconfigurada para **REAPER** optimizada para música en vivo (worship/iglesias). Incluye routing avanzado, efectos y soporte para tarjetas de audio integradas.

---

## 📥 Descarga e Instalación

1. **Descargar**:
   - Obtén el archivo portable desde [Releases](https://github.com/llromerorr/control-de-audio-iglesia/releases).
   - Contenido del ZIP:
     - REAPER portable (sin instalación).
     - Plugins/VST preconfigurados en `Reaper\Plugins\FX\UserPlugins` (detectados automáticamente al abrir el proyecto*).
     - Carpeta `¡¡INSTALADORES!!` con herramientas esenciales.

2. **Extraer**:
   - Descomprime en `C:\ReaperPortable` o similar.

3. **Dependencias** (recomendado):
   - Instala desde `¡¡INSTALADORES!!`:
     - **ASIO4ALL**: Para baja latencia.
     - **SWS Extension**: Funcionalidades extendidas.
     - **Optimizer**: Ajustes de sistema para audio en tiempo real.

> *Nota: Aunque REAPER no recomienda colocar plugins en `UserPlugins`, esta configuración garantiza que se detecten automáticamente para usuarios sin experiencia.

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

| Canal       | Descripción                                                                 |
|-------------|-----------------------------------------------------------------------------|
| **Voz**     | Procesamiento avanzado (de-esser, compresor multibanda).                   |
| **Guitarra**| Incluye amp simulación (Ignite Amps) y delay sincronizado.                 |
| **Reverb**  | Efecto compartido (Valhalla Supermassive).                                 |
| **Bajo**    | Virtual (Ample Bass P Lite II) con splits MIDI (C1-E3 para bajo+piano).    |
| **Pads**    | Capas de órgano (Surge XT) y coros (LABS Soft Piano).                      |

---

## ⚠️ Recomendaciones Clave
1. **Primer uso**:
   - Verifica que los plugins estén cargados (menú `FX` en cada canal).
   - Si falta alguno, REAPER sugerirá reemplazarlo automáticamente.

2. **Seguridad**:
   - Usa el archivo `Proyecto_Backup.RPP` como respaldo.

3. **Portabilidad**:
   - Funciona desde USB (actualiza las rutas de plugins si cambias de computadora).

---

## 🔧 Solución de Problemas

| Problema               | Solución                                                                 |
|------------------------|--------------------------------------------------------------------------|
| **Plugins no detectados** | Revisa `Opciones > Preferencias > Plugins > VST` y añade `Reaper\Plugins\FX\UserPlugins` manualmente. |
| **Ruido/feedback**      | Mantén el volumen de entrada en Windows ≤50% y ajusta ganancia en REAPER. |
| **Latencia alta**       | Usa ASIO4ALL con buffer ≤256 muestras. Cierra navegadores/antivirus.     |

---

## 📌 Notas Finales
- **Créditos**: Incluye plugins gratuitos (Surge XT, Keyzone Classic).
- **Personalización**: Modifica los presets de EQ en `Voz` y `Guitarra` según tu micrófono/instrumento.
- **Soporte**: Reporta issues en [GitHub](https://github.com/llromerorr/control-de-audio-iglesia).