/**
  @page ADC3_DMA ADC3 conversion using DMA for Data transfer

  @verbatim
  ******************** (C) COPYRIGHT 2011 STMicroelectronics *******************
  * @file    ADC3_DMA/readme.txt 
  * @author  MCD Application Team
  * @version V1.0.1
  * @date    15-May-2012
  * @brief   Description of the ADC3 DMA example.
  ******************************************************************************
  * @attention
  *
  * <h2><center>&copy; COPYRIGHT 2012 STMicroelectronics</center></h2>
  *
  * Licensed under MCD-ST Liberty SW License Agreement V2, (the "License");
  * You may not use this file except in compliance with the License.
  * You may obtain a copy of the License at:
  *
  *        http://www.st.com/software_license_agreement_liberty_v2
  *
  * Unless required by applicable law or agreed to in writing, software 
  * distributed under the License is distributed on an "AS IS" BASIS, 
  * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  * See the License for the specific language governing permissions and
  * limitations under the License.
  *
  ******************************************************************************
   @endverbatim

@par Example Description 

This example describes how to use the ADC3 and DMA to transfer continuously 
converted data from ADC3 to memory.
The ADC3 is configured to convert continuously channel7.
Each time an end of conversion occurs the DMA transfers, in circular mode, the
converted data from ADC3 DR register to the ADC3ConvertedValue variable.

In this example, the system clock is 144MHz, APB2 = 72MHz and ADC clock = APB2/2. 
Since ADC3 clock is 36 MHz and sampling time is set to 3 cycles, the conversion 
time to 12bit data is 12 cycles so the total conversion time is (12+3)/36= 0.41us(2.4Msps).

@par Directory contents 

  - ADC3_DMA/system_stm32f4xx.c   STM32F4xx system clock configuration file
  - ADC3_DMA/stm32f4xx_conf.h     Library Configuration file
  - ADC3_DMA/stm32f4xx_it.c       Interrupt handlers
  - ADC3_DMA/stm32f4xx_it.h       Interrupt handlers header file
  - ADC3_DMA/main.c               Main program

@par Hardware and Software environment 

  - This example runs on STM32F4xx Devices Revision A.
  
  - This example has been tested with STM32F4-Discovery (MB997) RevA and can be
    easily tailored to any other development board.
    
  - STM32F4-Discovery 
    - Connect the external signal(ranges from 0 to 3.3V) to the ADC3 pin (PC.02) to be converted.

@par How to use it ? 

In order to make the program work, you must do the following :

 + EWARM
    - Open the ADC3_DMA.eww workspace 
    - Rebuild all files: Project->Rebuild all
    - Load project image: Project->Debug
    - Run program: Debug->Go(F5)

 + MDK-ARM
    - Open the ADC3_DMA.uvproj project
    - Rebuild all files: Project->Rebuild all target files
    - Load project image: Debug->Start/Stop Debug Session
    - Run program: Debug->Run (F5)    

 + TASKING
    - Open TASKING toolchain.
    - Click on File->Import, select General->'Existing Projects into Workspace' 
      and then click "Next". 
    - Browse to  TASKING workspace directory and select the project "ADC3_DMA"   
    - Rebuild all project files: Select the project in the "Project explorer" 
      window then click on Project->build project menu.
    - Run program: Select the project in the "Project explorer" window then click 
      Run->Debug (F11)

 + TrueSTUDIO
    - Open the TrueSTUDIO toolchain.
    - Click on File->Switch Workspace->Other and browse to TrueSTUDIO workspace 
      directory.
    - Click on File->Import, select General->'Existing Projects into Workspace' 
      and then click "Next". 
    - Browse to the TrueSTUDIO workspace directory and select the project  "ADC3_DMA" 
    - Rebuild all project files: Select the project in the "Project explorer" 
      window then click on Project->build project menu.
    - Run program: Select the project in the "Project explorer" window then click 
      Run->Debug (F11)

 * <h3><center>&copy; COPYRIGHT 2011 STMicroelectronics</center></h3>
 */
