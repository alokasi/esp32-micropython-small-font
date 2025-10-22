The first run at this ran out of memory on the esp32 that I have therefore I had to design a method to compress the font. 

The oled.py file creates the display instance.  

The sm_font.py contains the font map encoded into a compressed format and a function to write the text to the frame buffer.

The oprint(print_string,x,y,char_spacing,color) function does the framebuffer writing.  'print_string' is what you want to show on the screen.  'x' and 'y' are top left coordinates of where you want to start writing (when wrapping occurs, it will go to the same x on the next line).  'char_spacing' is the pixels between characters.  'color' is the color of the text.  On my monochrome display, 0 is off and 1 is on.

To display the text, you still need to call the show() function on your oled object.
