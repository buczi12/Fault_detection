/**
This project is developed as a part of Master Thesis in field of Electrical Engineering at the 
AGH University of Technology,
Faculty of Electrical Engineering, Automatics, Computer Science and Biomedical Engineering,
Department of Electrical and Power Engineering
	
The project aim is to implement digital impendance relay algorithm on Discovery-F4 evaluation board.
Algorithm performance under different conditions (sampling frequency, current transformers excitation,
estimation algorithms) is simultaneously tested in MATLAB/Simulink software.

version history:

2017-07-20 -> ADC/DMA transfer working correctly (circular buffers)
2017-07-24 -> simple averaging FIR implemented, checked without signal generator and sems to work correctly


next aim:
- test FIR filter with signal generator, refactor code and performance

Author: Bart³omiej Buczek
mail: buczek.bartlo@gmail.com

Cracow, 2017
 */
