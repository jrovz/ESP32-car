# Control de Motores DC con Sensor Ultrasónico HC-SR04 y ESP32

Este proyecto demuestra cómo controlar dos motores DC usando un ESP32 y un sensor ultrasónico HC-SR04 para ajustar la velocidad de los motores en función de la distancia medida. El código está escrito en C y utiliza el entorno de desarrollo ESP-IDF.

## Requisitos de Hardware

- ESP32 (u otro dispositivo compatible con ESP-IDF)
- Sensor ultrasónico HC-SR04
- Dos motores DC
- Puente H L293D
- Cables de conexión

## Configuración de Pines

- Trigger del sensor ultrasónico: GPIO 5
- Echo del sensor ultrasónico: GPIO 18
- Pines de control de los motores DC (L293D):
  - M1O1: GPIO 12
  - M1O2: GPIO 13
  - M2O1: GPIO 34
  - M2O2: GPIO 35

## Funciones Principales

- `set_pwm_adelante()`: Configura los canales PWM para controlar la velocidad de los motores.
- `set_pwm_duty()`: Establece el ciclo de trabajo (duty cycle) para los motores basado en las distancias medidas.
- `init_motors()`: Inicializa los pines de control de los motores.
- `set_direction()`: Actualiza la dirección de los motores en función de la distancia medida.
- `ultrasonic_test()`: Mide la distancia con el sensor ultrasónico y actualiza el control de los motores.

## Uso

1. Conecta todos los componentes según las configuraciones de pines mencionadas.
2. Carga el código en tu ESP32 utilizando el entorno de desarrollo ESP-IDF.
3. El ESP32 medirá la distancia utilizando el sensor ultrasónico y ajustará la velocidad de los motores DC en función de la distancia.

Asegúrate de modificar las configuraciones de los pines y otros parámetros según tu propia configuración hardware.

## Contribuciones

¡Las contribuciones son bienvenidas! Si encuentras mejoras o correcciones para este proyecto, no dudes en enviar un pull request.
