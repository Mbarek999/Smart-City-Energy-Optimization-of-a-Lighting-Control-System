# Smart City Lighting Control System
## Energy-Optimized Public Lighting with IoT Integration

![System Overview](https://via.placeholder.com/1200x400/003366/FFFFFF?text=Smart+Lighting+System+Diagram)

## 📋 Project Overview
An autonomous lighting control system that reduces urban energy consumption through:

- Real-time ambient light measurement (1-100,000 lux range)
- Adaptive PWM dimming (0-100% with 0.5% resolution)
- Dual-mode operation (automatic/manual override)
- Cloud-connected energy monitoring (±2% accuracy)

## 🚀 Key Features

### 🖥️ Hardware Implementation
**STM32 Microcontroller Core**
| Function               | Implementation Details              |
|------------------------|-------------------------------------|
| Light Sensing          | 12-bit ADC @ 1kHz sampling rate     |
| Dimming Control        | Hardware PWM (16-bit timer)         |
| Energy Optimization    | Analog comparator wake-up           |
| Communication          | UART @ 115200 baud (8N1)            |

**Raspberry Pi Monitoring Hub**
- SQLite database logging (timestamped measurements)
- Real-time WebSocket dashboard (plotly.js visualization)
- REST API for remote configuration
- Automated report generation (CSV/PDF)

### 💾 Software Architecture
**STM32 Firmware (STM32CubeIDE)**
```c
// Core control loop (main.c)
while(1) {
    update_sensors();      // Interrupt-driven ADC
    calculate_dimming();   // Adaptive algorithm
    adjust_pwm_output();   // Hardware timer update
    handle_uart_comms();   // Protocol buffer messages
}
