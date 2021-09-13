

# Known market/project requirements at PC gate
Significantly reduce cost in SoC driver development, by defining an approach to enable driver reuse according to an accepted framework;<br>
Make consistent the upper layer software across different SoC. This requires standard HAL APIs to isolate hardware and software resources in such a manner that makes it easy to migrate software across platforms.

| Category | Req # | Requirement |
| --- | --- | --- |
| Technical Reqmtns	| T-1	| HAL MUST support API for core features |
|     | T-2	| HAL MUST support API for on-chip peripheral features | 
|     | T-3	| HAL MUST support both RTOS and bare-metal scenarios |
|     | T-4	| HAL MUST be able to support bare metal libc |
|     | T-5	| HAL MUST be able to be extended to support all CORE-V cores for the purpose of RTOS (not Linux) support|
|     | T-6	| HAL MUST support a description of the chip using a standardized syntax|
|     | T-7	| HAL SHOULD define a configuration file that can indicate to the IDE low level chip parameters such as memory space and allow it to display/read/write the registers of peripherals|
|     | T-8	| HAL MAY be able to be extended to support the CORE-V X Coprocessor Interface (CV-X-IF)|
|     | T-9 | HAL MAY be able to be extended to support the CV-VEC coprocessor|
| Industry Adoption Rqmtns|	IA-1	| HAL SHOULD be adopted/implemented for other RISC-V devices|
| Specification Rqmtns| S-1	| HAL Specification License for CORE-V MUST be open-source or freely licensed |
|    | S-2 | Proprietary extensions to the HAL Specification and Implementation, such as for custom ISA extensions or proprietary chip, MUST be supportable/allowable under open-source license|
|    | S-3	| HAL Specification, user documentation, and system implementation documentation for CORE-V HAL MUST be available in English |
|    | S-4	| HAL Specification MUST be published and managed by an industry open source or standards body, such as OpenHW, RISC-V International, or FOSSi|
| Implementation Rqmtns |	IM-1 | A complete open source reference implementation of the HAL for CORE-V MUST be a project deliverable |
|    | IM-2 |	FreeRTOS SHOULD be supported in the open source reference implementation of HAL for CORE-V |
|    | IM-3	|Newlib SHOULD be supported in the open source reference implementation of HAL for CORE-V |
|    | IM-3	| The HAL reference implementation for CORE-V SHOULD be published by the body publishing the Specification (previous page)|  
---

Table showing how existing solutions map against requirements at Project Concept gate

|  Items | 	CMSIS |	CSI |  NMSIS | Sifive Freedom Metal <br> (a library) <br> Freedom E SDK | STM32F4 HAL <br> STM32Cube <br> (a SDK?)  | CommonIO <br> (It is something different)  |
| --- | --- | --- | --- | --- | --- | --- |
| Core | Support (ARM) |	Support	| Support	|  Support  |  Support (ARM)  |     |
| Driver | Device x13 |	Device  x 23 | 	- |  Support  |  Support   |    |
| RTOS| FreeRTOS |	FreeRTOS, Rhino	| -   |   FreeRTOS  | FreeRTOS     |	    |
| NN	| Support	| Support |	Support  |  N  | Support   |	    |
| DSP	| Support	| Support	| Support	|   N  |  Support  |      |
| Coding Rule | MISRA | MISRA, TUeV61508 |	MISRA |  -  | -   |	    |
| Validation | Support |	Support |	 Support |  -  |  -  |	    |
| License |	Apache 2.0 |	Apache 2.0 |	Apache 2.0 |  Apache 2.0 and MIT  | Apache License 2.0, MIT <br> BSD-3-Clause, ST SLA0044 <br> Independent JPEG Group License  |	    |
| Software pack |	Support	| Support |	Support	|  Support  | Support   |    |
| Numbered Requirements	<br> (Y/N/Maybe/-)|     |    |    |    |    |		   |	
| T-1 |  Y, for ARM  | Y   |  Y   |   Y |  Y, for ARM  |		   |		
| T-2 |  Y  |  Y  |  Y  |  Y  |  Y   |	 |		
| T-3 |  Maybe  |  Y  |  N  |  Y  | Y  |	    |		
| T-4 | -  |  Y  | -  |  - |  -  |		   |		
| T-5 |  N  |  Y  |  N  |  N  |  N  |			|	
| T-6  | Y  |  N  | N   |  Y  | Y   |	   |		
| T-7 |  Y  |  N  | N | Y  | Y  |			|
| T-8 | N   | Maybe   |  N |  N  |   N |			|	
| T-9 |  N  |  Maybe?  |  N  |  N  |  N  |				|
| IA-1 | N  |  Y  |  Maybe  |  Maybe  | N   |			|	
| S-1 |  -  |  Y  |  Y  |  N  |  -  |	   |			
| S-2? |  Maybe  |  Maybe  |  Maybe  |  Maybe  |  Maybe  |	    |		
| S-3 |  -  |  Y  |  -  |  -  |   - |		   |	
| S-4 |  N  |  Y?  |  N  | -  |  N  |      |			
| IM-1 | N  |  Y  |  N  |  N  |  N  |		   |		
| IM-2 | N  |  Y  |  N  |  N  |   N |	    |			
| IM-3 | N  |  Y?  |  N  |  N  |  N  |	     |			
| IM-4 | N  |  Y?  |  N  |  N  |   N |		    |	<br>


**Resources** 
CMSIS: <br> 
--- https://developer.arm.com/tools-and-software/embedded/cmsis <br>  
--- https://github.com/ARM-software/CMSIS_5 <br>  
--- https://www.keil.com/pack/doc/CMSIS/General/html/index.html <br>  
CSI: <br>  
--- https://occ.t-head.cn/document?temp=t-head-chip-standard-interface-csi&slug=csi  <br>  
NMSIS:  <br>  
--- https://github.com/Nuclei-Software/NMSIS https://doc.nucleisys.com/nmsis/  <br>  
Sifive: <br>  
--- https://github.com/sifive/freedom-metal  <br>  
--- https://sifive.github.io/freedom-metal-docs/   <br>  
--- https://sifive.github.io/freedom-e-sdk-docs/index.html  <br>  
--- https://github.com/sifive/freedom-e-sdk  <br>  
STM32Cube:  <br>  
--- https://github.com/STMicroelectronics/stm32f4xx_hal_driver <br>  
--- https://github.com/STMicroelectronics/STM32CubeF4  <br>  
--- https://www.st.com/en/ecosystems/stm32cube.html  <br>  
Apache CommonIO: <br>  
--- https://commons.apache.org/proper/commons-io/  <br>  
--- https://www.tutorialspoint.com/commons_io/commons_io_overview.htm  <br>  
  





