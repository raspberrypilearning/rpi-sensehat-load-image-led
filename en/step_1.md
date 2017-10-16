You may wish to display an image loaded from a file on your Sense HAT's LED matrix. This is convenient if you want to have lots of stock images, for example international flags.

- Use any graphics editing tool (on Windows, OS X or Linux) to create the files. As long as they are saved on the Raspberry Pi's SD card as `JPEG` or `PNG`, and are 8×8 pixels in size, they can be loaded directly to the LED matrix with a single command.

- Here is an example image you can use to test. Right-click [here](images/example.png) and save the image into a folder on your Raspberry Pi. The image is very small because it is only eight pixels square.

    ![Example image](images/example.png)

- Open the file browser and locate the folder on your Raspberry Pi where you saved the image. The path to this folder will be displayed in the bar at the top of the screen. For example, your path might be `/home/pi/example.png`. Make a note of this path.

- Load the image onto the Sense Hat LED matrix by using the `load_image` function, which needs the path to the file you want to load.

    Here is the code:

    ```python
    from sense_hat import SenseHat

    sense = SenseHat()

    sense.load_image("/home/pi/example.png")
    ```
