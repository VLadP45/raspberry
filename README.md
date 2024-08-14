# raspberryimport RPi.GPIO as GPIO
import time

# Set up GPIO mode
GPIO.setmode(GPIO.BCM)

# Set up GPIO pin 17 as an output
GPIO.setup(17, GPIO.OUT)

try:
    while True:
        # Turn the LED on
        GPIO.output(17, GPIO.HIGH)
        time.sleep(1)  # Wait for 1 second
        
        # Turn the LED off
        GPIO.output(17, GPIO.LOW)
        time.sleep(1)  # Wait for 1 second

except KeyboardInterrupt:
    # Clean up GPIO settings before exiting
    GPIO.cleanup()
