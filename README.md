import time
from machine import Pin

RED_LED = Pin(2, Pin.OUT)
YELLOW_LED = Pin(8, Pin.OUT)
GREEN_LED = Pin(13, Pin.OUT)

RED_BUTTON = Pin(28, Pin.IN , Pin.PULL_UP)
YELLOW_BUTTON = Pin(7 , Pin.IN , Pin.PULL_UP)
GREEN_BUTTON = Pin(5, Pin.IN , Pin.PULL_UP)


duration_1 = 10
duration_2 = 5
duration_3 = 20

while True:
    if RED_BUTTON.value() == 0:
        duration_1 = int(input("Enter the duration for RED_LED:"))
        time.sleep(0.3)

    elif YELLOW_BUTTON.value() == 0:
        duration_2 = int(input("Enter the duration for YELLOW_LED:"))
        time.sleep(0.3)

    elif  GREEN_BUTTON.value() == 0 :
        duration_3 = int(input("Enter the duration for GREEN_LED:"))
        time.sleep(0.3)



    RED_LED.value(1)
    time.sleep(duration_1)
    RED_LED.value(0)

    YELLOW_LED.value(1)
    time.sleep(duration_2)
    YELLOW_LED.value(0)

    GREEN_LED.value(1)
    time.sleep(duration_3)
    GREEN_LED.value(0)







