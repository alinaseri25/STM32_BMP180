# STM32_BMP180

to use this lib you should be enable C99 Mode and Add --cpp to misc controls (in options for target --> C/C++ tab)

then you can add library to your project and use it

in this lib i'm used FreeRTOS and you can change it by remove #include "cmsis_os.h" from bmp180.hpp File and then
replace all osDelay function's with HAL_Delay and use it without FreeRTOS

you should be at first create an instance of BMP180 Class:
BMP180 bmp180(&hi2c);

then begin the sensor :
bmp180.Begin();

and then use all function .


caution true value of temp = temp / 10 and true value of altitude is altitude / 10
