# Lab-4

Blink_LED_250ms_Interval uses the Watchdog Timer interrupt process to toggle an LED with a 250msec interval on time. To set the timer to 250ms, I set 
WDTCTL = WDT_ADLY_250. 

500msPeriod_10%DutyCycle generates a PWM with a 10% duty cycle and 500ms period using polling process. To set the period to 500ms, I set TB0CCR0 = 500000-1. To set the Duty Cycle, I multiply 500ms by 10% to get 50ms of on time. This is shown in the code by the line TB0CCR1 = 50000.

250msPeriod_20%DutyCycle generates a PWM with a 20% duty cycle and 250ms period. To set the period to 250ms, I set TB0CCR0 = 250000-1. To set the Duty Cycle, I multiply 250ms by 20% to get 50ms of on time. This is shown in the code by the line TB0CCR1 = 50000.
