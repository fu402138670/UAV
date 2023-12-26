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
> Address 0x76 設備在I²C（Inter-Integrated Circuit）總線上的位址  
- **ARSPD_TYPE 0** - Sets the type of airspeed sensor. 0 means airspeed sensor function is disabled.  
> ARSPD_TYPE 1 ARSPD_TYPE 參數定義了空速計的型別或模型。 1: MS4525  
> ARSPD_TYPE 2 ARSPD_TYPE 參數定義了空速計的型別或模型。 2: analog  
> ARSPD_TYPE 9 ARSPD_TYPE 參數定義了空速計的型別或模型。 9: DLVR-L10D  
> ARSPD_BUS 1 參數定義了空速計連接到的I²C匯流排編號。 設定為1意味著空速計連接到I²C總線1。  
> ARSPD_PIN 10 定義了飛控板上用於接收空速計訊號的類比輸入引腳。 設定為10表示空速計的訊號將從飛控板上的接腳編號10讀取。  

### Remote Control Mapping
- **RCMAP_PITCH 2** - Maps pitch control to channel 2 of the remote control.
- **RCMAP_ROLL 1** - Maps roll control to channel 1 of the remote control.

### Flight Mode Configuration
- **FLTMODE_CH 6** - Channel 6 of the remote control is used to switch flight modes.
- **FLTMODE1 19** - Q-LOITER (PWM 910-1230)
- **FLTMODE2 11** - RTL (PWM 1231-1360)
- **FLTMODE3 5** - FBWA (PWM 1361-1490)
- **FLTMODE4 5** - FBWA (PWM 1491-1620)
- **FLTMODE5 0** - Manual (PWM 1621-1749)
- **FLTMODE6 11** - RTL (PWM 1750-2049)
- **OSD1_FLTMODE_EN 1** - Enable filight information to OSD.
- **OSD1_FLTMODE_X 2** - Set horizon (X) location of flight information.
- **OSD1_FLTMODE_Y 8** - Set vertical (Y) location of flight information.

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
- **Q_ENABLE 1** - 用於啟用或停用QuadPlane功能，這是針對那些同時具備固定翼和多旋翼飛行能力的飛行器的設定。 1意味著啟用了QuadPlane功能。
- **Q_FRAME_CLASS 7** - 參數定義了四旋翼飛機的框架類別。 7表示Tri Plane佈局。
- **Q_ENABLE 1** - 數用於啟用或停用QuadPlane功能，這是針對那些同時具備固定翼和多旋翼飛行能力的飛行器的設定。 1意味著啟用了QuadPlane功能。
- **Q_FRAME_CLASS 7** - 參數定義了四旋翼飛機的框架類別。 7表示Tri Plane佈局。
- **Q_FRAME_TYPE 0** - 參數定義了旋翼的具體類型。 0表示"+"佈局。 馬達和螺旋槳被安排成一個“+”形狀。
- **Q_TILT_ENABLE 1** - 參數用於啟用或停用QuadPlane（一種具有垂直起降能力的固定翼飛機）的傾轉旋翼（Tiltrotor）功能。 1意味著啟用了傾轉旋翼功能。 #重囉後才會出現Q_TILT選項
- **Q_TILT_TYPE 2** - 參數用於定義QuadPlane（具有垂直起降能力的固定翼飛機）的傾轉旋翼（tilt-rotor）機構的類型。 2通常表示Vectored Yaw傾轉旋翼控制偏航。
- **Q_TILT_MASK 3** - 參數用來定義哪些馬達應該被視為傾轉旋翼（tiltrotor）.3等於00000011表示第1和第2馬達是傾轉旋翼。
- **Q_ASSIST_SPEED -1** - 參數用於在空速降至某個特定值以下時自動啟用旋翼提供額外的升力和穩定性。 -1意味著禁用了輔助模式。
- **Q_M_PWM_TYPE 6** - 參數用於設定多旋翼馬達控制器（ESC）的PWM協議類型。 6表示使用DShot600通訊協議。
- **Q_OPTIONS 688129** - 參數用於設定一系列的選項。 (setup per bitmask for details)
- **Q_TRANS_FAIL 10** - 參數用於設定在嘗試從垂直起降（VTOL）模式過渡到固定翼模式的時間閾值,超出閾值啓動失敗處理。 10: 10秒.
- **Q_RTL_MODE 1** - 參數用於設定執行RTL模式時的行為。 1：先以固定翼模式飛回，然後切換到VTOL模式進行垂直降落。
- **Q_RTL_ALT 50** - 參數用於設定執行RTL模式時的飛行高度。 50:50米.
- **Q_TILT_RATE_DN 20** - 20表示從懸停到向前飛行時馬達角度變化的最大速度，最多20度/秒。
- **Q_TILE_RATE_UP 80** - 80表示從向前飛行到懸停時馬達角度變化的最大速度，最多80度/秒。
- **Q_TRANSITION_MS 5000** - 參數用於設定從垂直起降（VTOL）模式到固定翼模式的過渡時間長度。 5000意味將花費5000毫秒完成過渡。
- **Q_WVANE_HGT_MIN 15** - 參數用於風向標（weathervane）功能。 此功能可讓飛機自動調整其朝向以減少風的影響，提高穩定性。 15：高度超過15米激活。
- **Q_TILT_YAW_ANGLE 12** - VTOL模式下的螺旋槳垂直位置  
> Q_TILT_YAW_ANGLE 0  

### Video Transmitter Control
- **VTX_ENABLE 1** - Enables or disables control of the Video Transmitter (VTX).

### Servo Output Configuration
- **1** Motor2 1000 1000 2000
- **2** Motor1 1000 1000 2000
- **3** Motor4 1000 1000 2000  
> Motor4 1100 1500 1900  
> Changed Motor3 to Motor4  
- **4** Motor3 Disabled 1100 1500 1900 /Painless360 suggest: 1100 1000 2000  
- **5** Aileron Reverse 1100 1500 1900  
> Aileron 1100 1500 1900  
- **6** Aileron Reverse 1100 1500 1900  
> Aileron 1100 1500 1900  
- **7** Elevator 1100 1500 1900  
- **8** TiltMotorFrontLeft 850 1437 2025  
> TiltMotorLeft 1100 1500 1900  
- **9** TiltMotorFrontRight Reverse 875 1462 2050  
> TiltMotorRight 1100 1500 1900  
- **10** Disabled 1100 1500 1900
- **11** Motor7/TailTiltServo 1100 1500 1900

### Flight Modes
- **Flight Mode 1** QLOITER
- **Flight Mode 2** RTL
- **Flight Mode 3** FBWA
- **Flight Mode 4** FBWA
- **Flight Mode 5** Manual
- **Flight Mode 6** RTL

### ESC Calibration
- **SERVO_BLH_AUTO 1** Enable BLHeli_S ESC calibration tool pass Ardupilot  
> SERVO_BLH_AUTO 0  
