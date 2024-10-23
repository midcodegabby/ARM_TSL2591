This project is a from-scratch implementation of a TLS2591 light sensor driver. 
My main goal for this project was to learn about the I2C communication protocol by
implementing it from scratch between an STM32 Cortex-M4 mcu and a TSL2591 light sensor.

Things learned:
- I2C communication protocol: implementation, use, and electrical characteristics
- Configuring clocks and gpio for I2C communication
- Enabling and using the FPU in ARM Cortex-M4 microcontrollers
- Debugging I2C via Logic Analyzer

Status (10/21/2024):
- In-Progress
- Operational
- Accuracy has been increased in Low gain mode by multiplying LUX readings over 650 by a factor
  of 1.6 and LUX readings under 300 by a factor of 0.8. Accuraccy is now around 90-95% of the values
  from the Photone iPhone app (LUX meter app). This calibration was also done using the Photone app. 

Next steps:
- Switch from ~5s busy loop polling to interrupt polling

Possible future implementations:
- Function to reset I2C bus from a deadlocked state

Current, more accurate test video: 
https://www.youtube.com/watch?v=m42UTxCefyY

Old, less accurate test video:
https://www.youtube.com/shorts/LOIbflBZAfY
