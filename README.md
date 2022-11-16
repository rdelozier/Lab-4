# Lab-4

Blink_LED_250ms_Interval uses the Watchdog Timer interrupt process to toggle an LED with a 250msec interval on time. To set the timer to 250ms, I set 
WDTCTL = WDT_ADLY_250. 

For both PWM signals, I intialize Pin 1.6 to be the output of the PWM signal.

500msPeriod_10%DutyCycle generates a PWM with a 10% duty cycle and 500ms period using polling process. To set the period to 500ms, I set TB0CCR0 = 500000-1. To set the Duty Cycle, I multiply 500ms by 10% to get 50ms of on time. This is shown in the code by the line TB0CCR1 = 50000.

250msPeriod_20%DutyCycle generates a PWM with a 20% duty cycle and 250ms period. To set the period to 250ms, I set TB0CCR0 = 250000-1. To set the Duty Cycle, I multiply 250ms by 20% to get 50ms of on time. This is shown in the code by the line TB0CCR1 = 50000.

For the 500ms Period 10% duty cycle, the duty cycle was the same percentage. The period was 474.48ms, 26ms less than the calculated 500ms and the frequency was 2.106 Hz, .106 Hz higher than the calculated 2s. This is very close to our calculated values.

For the 250ms Period 20% duty cycle, the duty cycle was the same percentage. The period was 237.57ms, 13ms less than the calculated 250ms and the frequency was 4.209 Hz, .209 Hz higher than the calculated 2s. This is very close to our calculated values.

For both situations, the period was lower than expected and the frequency was higher.
