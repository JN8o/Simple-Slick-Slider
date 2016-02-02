# Simple-Slick-Slider
Motorised timelapss slider with display output and bluetooth control.

##The hardware side.
The first iteration will include:
- Arduino Uno
- Nema 17 stepper
- Easy driver
- 1602 LCD with I2C 
- Battery pack (currently using mains for testing purposes)

In the future I would like to miniturize the electronics and hopefully end up using:
- Arduino Nano
- Nema 11 stepper
- Easy driver
- 1602 LCD with I2C
- Bluetooth module
- NFC
- LiPo/LiFe power pack

Electronics-wise im set, however i am relatively new to coding, so my C is quite bad. 

The IO's for the project will be:
- **Up**        = 0
- **Down**      = 1
- **Select**    = 2
- **Start**     = 3
- **Stop**      = 4
- **LS1+2**     = 5 (Limit switches)
- LCD       = SDA
- LCD       = SCL
- Stepper   = 9
- Stepper   = 10

##Software Side.
The basic menu system:
Direction
  -Left
  -Right

Distance
  -0mm      (increases by 250mm; each section is this length)

Speed
  -omm/min  (increases in increments of 5mm/min with a max of 50 times the distance)

Delay
  -0sec     (increases by increments of 1 with a max of 30)
  
To navigate through the menu, i'd like to use just the up and down keys, once selected one the menu headings you must then
press select to enter the submenu. Once in the submenu, you would use the up and down keys to increase the number, and press 
select to return to the menu.

When start is executed it is important to check that values greater than 0 have been entered, if not it will return to the 
menu. If successful an ETA countdown timer will show the remaining time.

Once completed, the slider will stop, if the stop button is pressed again then it will reset the values and take you back to
the menu. 



