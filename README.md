# STM32-control-of-SSM3582-OLED-Encoder-
Simple project for STM32 (i2c) initialization of SSM3582a digital(i2s) amplifier with encoder volume control (OLED screen)

<b>IDE</b>: STM32CubeIDE<br />
<b>MCU</b>: STM32H7B0VBT6 (aliexpress board)<br />
<b>AMP</b>: SSM3582a CHIP&DIP board RDC2-0059 (https://www.chipdip.ru/product/rdc2-0059)<br />
<b>UART</b>: CH341A Pro Programmer<br />
<b>Other</b>: Rotary Encoder (w/button), ssd1306 OLED (4wire SPI mode)<br />

1. Configure SSM3582 to operate wia I2C interface:<br />
1.1 Set I2C address<br />
![image](https://user-images.githubusercontent.com/71771695/205850593-a085442f-d172-4e6c-84b7-ec1da95ea317.png)

1.2 Define base parameters for amplifier initialization according available registers:<br />
![image](https://user-images.githubusercontent.com/71771695/205851777-0918aef8-af4e-466d-a5e1-2acdef029c97.png)

1.3 After configuring ADDR0/1 settings make sure you're pulled up sda/scl lines to VDD (with 10kOhm resistors).<br />

2 Generate initial project in IDE<br />
2.1 SSM3582 initializing requires only I2C (with standard settings).<br />
    If you want to use additional features (like encoder volume, OLED, etc.) you must add some MCU settings to your project.<br />

2.2 
