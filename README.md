# Safe Eyes - Vibe

**Safe Eyes Vibe** es un fork personalizado de [Safe Eyes](https://github.com/slgobinath/safeeyes) diseñado para priorizar no solo la salud ocular, sino también la ergonomía cervical y postural.

Este fork surge de la necesidad de adaptar las pausas activas a una rutina que incluya ejercicios específicos para el cuello y la espalda, además de corregir problemas técnicos específicos de ejecución en dispositivos con configuraciones de audio avanzadas (PipeWire).

## 🌟 Características de este Fork

- **Frases Personalizadas en Español**: Se han sustituido los mensajes predeterminados por una serie de ejercicios guiados en español enfocados en estiramientos de cuello, hombros y corrección postural.
- **Soporte de Audio Mejorado (PipeWire)**: El plugin `audiblealert` ha sido modificado para permitir la redirección de los sonidos de alerta a dispositivos de audio específicos mediante el parámetro `audio_target` (usando `pw-play`).
- **Configuración Optimizada**: Ajustes predefinidos para una experiencia más fluida y menos intrusiva, pero efectiva para prevenir el RSI (Lesión por Esfuerzo Repetitivo).

## 🚀 Ejecución desde el Código Fuente

Para ejecutar esta versión personalizada en tu sistema, asegúrate de tener las dependencias necesarias instaladas:

```bash
# Clonar el repositorio
git clone https://github.com/caralacm/safeeyes-vibe.git
cd safeeyes-vibe

# Ejecutar la aplicación
python3 -m safeeyes
```

### Dependencias recomendadas

- `python3` (>= 3.10)
- `gir1.2-gtk-4.0`
- `pipewire` / `pw-play` (para el soporte de audio mejorado)
- `python3-gi`, `python3-babel`, `python3-croniter`

## 🛠️ Personalización de Audio

Si utilizas PipeWire y deseas que las alertas suenen por un dispositivo específico, puedes editar tu configuración en `~/.config/safeeyes/safeeyes.json` (dentro de la sección del plugin `audiblealert`):

```json
{
    "id": "audiblealert",
    "enabled": true,
    "settings": {
        "audio_target": "nombre_de_tu_dispositivo",
        "volume": 80
    }
}
```

## 📋 Lista de Ejercicios Incluidos

Algunos de los ejercicios que verás durante tus descansos cortos y largos:

- Inclinar la cabeza hacia los hombros.
- Retracciones de mentón.
- Giros de hombros y estiramientos de escápulas.
- Caminatas con postura erguida.
- Estiramientos en el marco de la puerta.

## ⚖️ Licencia

Este proyecto mantiene la licencia original **GNU General Public License v3**.

---

_Basado en el trabajo original de [slgobinath](https://github.com/slgobinath/safeeyes)._
