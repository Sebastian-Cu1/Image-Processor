# Image-Processor
This is a image processor based on FGPA writng in verilog with DE1_SOC board.

functions:
  This processor can adjust the color density of each RGB channel with 5 levels.
  Including a black and white filter by averging the RGB channel.
  Including a horizontal flip, a rotation by 180 degrees.
  Including a blur effect by using convolution with 3*3 averaging kernal.

  The inputs on the board takes SW[2:0] as RGB enable, and using KEY[1:0] to change the level from 0-4 (2 by default), KEY[2] is reset. 
For example, set SW[2] to 1 will enable red channel adjustment, then by pushing KEY[0] will increase the red intensity of the entire picture.
SW[3] will apply black and white filter, SW[4] will enable blur effect, SW[6] and SW[5] are for flip and rotation.

  User can change the image the want to use by initalizing the ROM "OriginalMona" with a .mif file that contains a 160*120 resolution, 4 bits 
channel depth picture data( by defualt it contains a "Mona Lisa").

This project contains a VGA adaptor, which is from:
  [1]S. Brown, “VGA Adaptor,” Utoronto.ca, Oct. 29, 2024. https://q.utoronto.ca/courses/363319/pages/vga-adapter (accessed Nov. 9, 2024).
