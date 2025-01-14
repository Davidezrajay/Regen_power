# Regen_power
Regenerative power code for electric car

## Controls and user interface
- Power switch (on/off)
- Bat Display (analog read out)
- Rate of Charge/Discharge display (analog readout)
- Brake pedal (analog voltage)
- Accelerator (analog voltage) (pulled from the TPS)
- Ignition Key (on/off) (could use the ECU voltage of 0/1)
- Led Flashing Green for charged/charing, Green for Fully charged
- Led Red for system fault (battery pack temp or 


## Input lines
- Key Power (0/1)
- Bat Level Sensor (voltage 0-
- Accelerator position
- Brake Position
- Battery Pack Temp Sensor

## System States
- Off switch position, or Battery Pack Sensor
- Charging
- Powering

## System Logic

 - Off = "Power Switch" position 'off' or 'Battery Pack Temp Sensor" exceeding "x"
 - Charging Bat = If power is not requested, if battery is less than x (voltage from Bat level sensor) & signal from accelerator is below x amount, Rate of charge is mapped to increase charge rate in conjunction with accelerator and brake sensor voltage. (accelerator below x = increase in rate of change, brake sensor increase voltage = increase rate of charge to map max rate at end of brake pedal play)
 - Powering =  engine ignition is off, battery level is above x. Amount of power is mapped to accelerator sensor voltage

## Parts

- Motor: [https://emrax.com/e-motors/emrax-228/](https://emrax.com/e-motors/emrax-228/)
- ESC: [https://drive.google.com/file/d/19PIGDJjHQr4P6eKvvkMb4wlcMqGtrt3e/view](https://drive.google.com/file/d/19PIGDJjHQr4P6eKvvkMb4wlcMqGtrt3e/view)
- Battery - (720V nominal recommended) Possible option: [https://www.freedomwon.co.za/wp-content/uploads/LiTE-HOME-HV-Range-Overview-Spec-Sheet-3.pdf](https://www.freedomwon.co.za/wp-content/uploads/LiTE-HOME-HV-Range-Overview-Spec-Sheet-3.pdf)
- Sensor Brake (5v)
- Sensor Acclerator (5v)
- Controller (arduino / Tinsey)
- Voltage Display
- Shunt
- Amp Meter
- Load Balancer (if not built in)
- 5 volt Power supply
- Power Switch (5 volt)
- High voltage System cutoff Relay
- Pack Voltage Sensor
- Voltmeter Display
- TPS (throttle Position Sensor)
- LED (green for fully charged, Flashing for charging)
- LED (red for failure)





