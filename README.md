# VHDLV_video_blend_module
Design a video blend module

![Alt text](https://cloud.githubusercontent.com/assets/13169624/8503715/b31cda50-21bb-11e5-94e9-3e3351b9a0c4.png?raw=true "Design a video blend module")

Image A and image B are stored in memory (block ram). Each image is made of 8 bit wide (monochrome) pixels. First pixel is denoted as a black dot as shown above. 
- Image A dimension: 320 x 240 pixels 
- Image B dimension: 256 x 144 pixels 

The aim of the video blend module is to read all pixels of image A and image B from the memory, then composite image B on top of image A as shown on the diagram. Then write image C into the memory as shown. Image A is located in memory address 0x00012000, and image C is located in memory address 0x0005D000. The final result of image C should be written into memory address 0x000A8000. Each memory address is capable of storing a single pixel. You can assume the system is running at 100MHz clock rate. You will receive a start pulse (SOF), to update Image C.

**Design requirement:** 
- [ ] Create a block diagram with details
- [ ] Calculate amount of memory required to store image A, B and C 
- [ ] Determine pipe line delay through the system 
- [ ] Produce VHDL code of the design 
- [ ] Write a small test bench to test the module 
- [ ] Synthesise VHDL module for Xilinx KintexK70T FPGA**(Optional)**
- [ ] Analyse timing results**(Optional)**

# Solution
Text here

**Step 1: Set-up Image A and Image B in Rom**
- [ ] Create coe file for Image A and Image B
- [ ] Transfer both Images in ROM

**Step 2: Transfer A and Image B into Ram into required location**
- [ ] Read data from of Image A Transfer into Ram on location 0x00012000
- [ ] Read data from of Image B Transfer into Ram on location 0x0005D000

**Step 3: Render Image C**
- [ ] Transfer Image A data on Ram on location 0x000A8000 Starting from (0,0) end at (319,239)
- [ ] Transfer Image B data on Ram on location 0x000A8000 Starting from (X,X) end at (319, 239)
