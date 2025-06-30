# STM32F411 Nucleo: Dual-Interrupt LED Control

## Description
Controls onboard LED (PA5) using two interrupt sources:
- **PA0** (rising edge): Turns LED ON
- **PC13** (falling edge): Turns LED OFF

## Key Features
- **Dual-interrupt system**: Independent triggers for ON/OFF
- **Hardware**: 
  - STM32F411RE Nucleo
  - LED: PA5 (LD2)
  - Buttons: 
    - PA0 (External button, rising-edge)
    - PC13 (Onboard button B1, falling-edge)
- **Config**:
  - Clock: HSI (16MHz)
  - GPIO:
    - PA0: Input with rising-edge interrupt
    - PC13: Input with falling-edge interrupt
    - PA5: Push-pull output

## Usage
1. Connect external button to PA0 (with pull-up)
2. Flash to STM32F411RE Nucleo
3. Interactions:
   - Press external button (PA0) → LED ON
   - Press onboard button (PC13) → LED OFF

## Dependencies
- STM32Cube HAL
- Generated with STM32CubeIDE/ STM32CubeMX
