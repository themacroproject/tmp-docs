MacroPod One Examples
===================================

**Examples** 

There are two ways to program the MacroPod One- to insert characters and/or to send keystrokes (single or combined).

To send any characters, use the following in the if block of the loop() function.
.. code-block:: cpp

   DigiKeyboard.print("ABCDEFGH");

To send a keystroke or a combination of keys, use the following in the if block of the loop() function.
.. code-block:: cpp

   DigiKeyboard.sendKeyStroke(KEY_D, MOD_GUI_LEFT);

Here, 'KEY_D' is the character D and 'MOD_GUI_LEFT' is the windows key.

Check out the list of predefined keys that you can use in this `PDF <https://github.com/themacroproject/arduino_code/Arduino_Keyboard_Macros.pdf>_`

For more information, visit `The Macro Project website <https://themacroproject.github.io/>`


.. note::

   This project is under active development.

