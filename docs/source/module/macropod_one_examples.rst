MacroPod One Examples
===================================

**Examples** 

There are two ways to program the MacroPod One- to insert characters and/or to send keystrokes (single or combined).

#. 1. To send any characters, use the following in the if block of the loop() function.


.. code-block:: cpp

   DigiKeyboard.print("ABCDEFGH");


Check out the code `HERE <https://github.com/themacroproject/macropod_one/blob/master/digispark_single_key_strings/digispark_single_key_strings.ino>`_

#. 2. To send a keystroke or a combination of keys, use the following in the if block of the loop() function.


.. code-block:: cpp

   DigiKeyboard.sendKeyStroke(KEY_D, MOD_GUI_LEFT);


Check out the code `HERE <https://github.com/themacroproject/macropod_one/blob/master/digispark_single_key_shortcuts/digispark_single_key_shortcuts.ino>`_

Here, 'KEY_D' is the character D and 'MOD_GUI_LEFT' is the windows key.

Check out the list of predefined keys that you can use in this `PDF <https://themacroproject.github.io/Arduino_Keyboard_Macros.pdf>`_

For more information, visit `The Macro Project website <https://themacroproject.github.io/>`_


.. note::

   This project is under active development.

