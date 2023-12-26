# F405 VTOP Ardupilot Parameter Setup

**1st released:** 2023/12/22  
[Parameters Plane Stable V4.4.3](https://ardupilot.org/plane/docs/parameters-Plane-stable-V4.4.3.html)

### Battery Monitoring
- **BATT_VOLT_PIN 14** - Analog input pin for battery voltage measurement. Specific pin depends on your flight controller hardware.
- **BATT_VOLT_MULT 21** - Calibration multiplier for the battery voltage monitoring system, converting the raw voltage value from the analog input pin to the actual battery voltage.
- **BATT_CURR_PIN 15** - Analog input pin for battery current measurement.
- **BATT_AMP_PERVLT 66.7** - Calibration constant for the battery current monitoring system.

### RSSI Configuration
- **RSSI_TYPE 2** - Defines the type or format of the RSSI signal. 2 means the controller uses voltage as the RSSI signal.
- **RSSI_ANA_PIN 8** - Analog input pin on the controller board for reading analog RSSI signal.

### Board Alternate Configuration
- **BRD_ALT_CONFIG 1** - The flight controller will use a predefined first set of alternate hardware configurations.
- **SERIAL6_PROTOCOL 23** - Defines the communication protocol for the sixth serial port (Serial 6). 23 means this port is configured to support MSP (MultiWii Serial Protocol).
- **SERIAL6_OPTIONS 0** - Additional options and behaviors for the sixth serial port (Serial 6).
- **SERIAL6_BAUD 115** - Baud rate for the sixth serial port (Serial 6). 115 indicates a communication baud rate of 115200 bits/sec.

### Compass and Airspeed Sensor
- **COMPASS_AUTODEC 1** - Controls whether the compass's magnetic declination is set automatically.
- **ARSPD_TYPE 0** - Sets the type of airspeed sensor. 0 means airspeed sensor function is disabled.

### Remote Control Mapping
- **RCMAP_PITCH 2** - Maps pitch control to channel 2 of the remote control.
- **RCMAP_ROLL 1** - Maps roll control to channel 1 of the remote control.

### Flight Mode Configuration
- **FLTMODE_CH 6** - Channel 6 of the remote control is used to switch flight modes.
- **FLTMODE1 19** - Q-LOITER (PWM 910-1230)
- **FLTMODE2 11** - RTL (PWM 1231-1360)
- **Other Flight Modes...**

### Rangefinder Types
- **RNGFND_LANDING 0** - Controls whether a rangefinder is used during landing.
- **RNGFND1_TPYE 0** - Defines the type of the first rangefinder.
- **RNGFND2_TPYE 0** - Defines the type of the second rangefinder.
- **RNGFND3_TPYE 0** - Defines the type of the third rangefinder.
- **RNGFND4_TPYE 0** - Defines the type of the forth rangefinder.
- **RNGFND5_TPYE 0** - Defines the type of the fifth rangefinder.
- **RNGFND6_TPYE 0** - Defines the type of the sixth rangefinder.
- **RNGFND7_TPYE 0** - Defines the type of the seventh rangefinder.
- **RNGFND8_TPYE 0** - Defines the type of the wighteh rangefinder.
- **RNGFND9_TPYE 0** - Defines the type of the ninth rangefinder.
- **RNGFNDA_TPYE 0** - Defines the type of the tenth rangefinder.

### Logging Configuration
- **LOG_BACKEND_TYPE 0** - Sets the type of log backend. 0 usually indicates all logging functions are disabled.
- **LOG_BITMASK 0** - Controls the detail level of flight logging.

### Terrain Following and Arming Checks
- **TERRAIN_ENABLE 0** - Controls the enabling of terrain following functionality.
- **ARMING_CHECK 751998** - Determines which checks are required before arming the aircraft.

### QuadPlane Configuration
- **Q_ENABLE 1** - Enables or disables the QuadPlane functionality.
- **Q_FRAME_CLASS 7** - Defines the frame class of the quadplane.
- **More QuadPlane Parameters...**

### Video Transmitter Control
- **VTX_ENABLE 1** - Enables or disables control of the Video Transmitter (VTX).

### Servo Output Configuration
- **1 Motor2** 1000 1000 2000
- **2 Motor1** 1000 1000 2000
- **More Servo Outputs...**

### Flight Modes
- **Flight Mode 1** QLOITER
- **Flight Mode 2** RTL
- **More Flight Modes...**
