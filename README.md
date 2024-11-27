# Image-Processor
This is a image processor based on FGPA using verilog with DE1_SOC board.

functions:
  This processor can adjust the color density of each RGB channel with 5 levels.
  Including a black and white filter by averging the RGB channel.
  Including a horizontal flip, a rotation by 180 degrees.
  Including a blur effect by using convolution with 3*3 averaging kernal.

  The inputs on the board takes SW[2:0] as RGB enable, and using KEY[1:0] to change the level from 0-4 (2 by default), KEY[2] is reset. 
For example, set SW[2] to 1 will enable red channel adjustment, then by pushing KEY[0] will increase the red intensity of the entire picture.

