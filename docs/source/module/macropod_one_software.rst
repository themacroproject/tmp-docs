MacroPod One Software
===================================


**How to program Digispark Attiny85 using Arduino IDE** 


#. Install the Digispark board definitions in Arduino IDE.


#. Open the Arduino IDE and go to File > Preferences.
In the Additional Boards Manager URLs field, add the following URL: `https://raw.githubusercontent.com/digistump/arduino-boards-index/master/package_digistump_index.json <https://raw.githubusercontent.com/digistump/arduino-boards-index/master/package_digistump_index.json>_`
Click "OK" to close the Preferences window.
Install the necessary USB drivers:


#. Download the appropriate driver for your operating system from the Digispark website: `https://digistump.com/wiki/digispark/tutorials/connecting <https://digistump.com/wiki/digispark/tutorials/connecting>_`
Follow the installation instructions for the driver.
Connect the Digispark to your computer:


#. Plug the Digispark into an available USB port on your computer using a micro USB cable.
Configure the Arduino IDE to use the Digispark board:


#. Go to Tools > Board and select "Digispark (Default - 16.5mhz)" from the list.
Write your code in the Arduino IDE:


#. Write your code in the Arduino IDE as you normally would.
Upload your code to the Digispark:


#. Click the Upload button in the Arduino IDE.
The IDE will compile your code and then upload it to the Digispark.


#. Test your code:
Once the code is uploaded, the Digispark will automatically run it.
Test your code to make sure it works as expected.


**The Code:**


This code is designed to control a button press that sends a keyboard shortcut to a computer. It uses the DigiKeyboard library to allow an Arduino board to act as a USB keyboard.

Include the DigiKeyboard library.


.. code-block:: cpp

   #include "DigiKeyboard.h";

Constant keyPin1 is defined as 1, which indicates that the button is connected to pin 1 on the board.


.. code-block:: cpp

   const int keyPin1 = 1;  

An integer variable keyState1 is declared and initialized to 0. This variable will store the state of the button.


.. code-block:: cpp

   int keyState1 = 0;  

In the setup() function, the keyPin1 is set as an input pin using the pinMode() function.


.. code-block:: cpp

   void setup() {
      pinMode(keyPin1, INPUT);
   }

In the loop() function, the DigiKeyboard.sendKeyStroke(0) function sends a null key to the computer to prevent missing the first character after a delay.


.. code-block:: cpp

   DigiKeyboard.sendKeyStroke(0);

The digitalRead() function reads the state of the button and stores it in the keyState1 variable.


.. code-block:: cpp

   keyState1 = digitalRead(keyPin1);

Then, an if statement checks if the button is pressed by comparing keyState1 to HIGH. If the button is pressed, the DigiKeyboard.sendKeyStroke() function is called to send a keyboard shortcut to the computer. In this case, it sends the Windows shortcut to show the desktop using the KEY_D and MOD_GUI_LEFT parameters.

Finally, the DigiKeyboard.delay() function is used to wait for 500 milliseconds before repeating the loop. This function is preferred over the delay() function used in regular Arduino programming because it keeps the computer informed that the keyboard is still alive and connected.


For more information, check the MacroPod One `Github <https://github.com/themacroproject/arduino_code>`


.. note::

   This project is under active development.

