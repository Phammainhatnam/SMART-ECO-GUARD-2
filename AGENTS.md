# Project Rules

1. The ESP32 is responsible for real-time hardware control.
2. The PC is responsible for webcam processing and AI Vision.
3. AI decisions must be treated as suggestions.
4. ESP32 safety logic always has higher priority than AI commands.
5. Never allow unsafe motor commands.
6. Never change GPIO assignments without documenting the change.
7. Prefer non-blocking timing using `millis()` instead of long `delay()` calls.
8. Sensor failures must be handled safely.
9. Loss of PC/Wi-Fi communication must result in a safe state.
10. Hardware-specific assumptions must never be guessed.
11. Verify the actual ESP32 board, motor driver, sensors, voltage requirements, and GPIO assignments before writing hardware-control code.
12. Test hardware modules independently before integrating them.
13. Preserve existing working code unless a change is explicitly requested.
14. Clearly document important architecture and hardware decisions.
