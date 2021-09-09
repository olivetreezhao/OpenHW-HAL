
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

<br>
<br>
<br>
Table showing how existing solutions map against requirements at Project Concept gate

|  Items | 	[CMSIS](https://developer.arm.com/tools-and-software/embedded/cmsis) |	CSI | [CommonIO](https://commons.apache.org/proper/commons-io/) |  [NMSIS](https://doc.nucleisys.com/nmsis/) | [Sifive Freedon Metal](https://github.com/sifive/freedom-metal) | 
| --- | --- | --- | --- | --- | --- |
| Web Link |  https://developer.arm.com/tools-and-software/embedded/cmsis   |     |  https://commons.apache.org/proper/commons-io/   |  https://github.com/Nuclei-Software/NMSIS ; https://doc.nucleisys.com/nmsis/   | https://github.com/sifive/freedom-metal ; https://sifive.github.io/freedom-e-sdk-docs/index.html |
| Core | Support |	Support	| Support	| Support |
| Driver | Device x13 |	Device  x 23 | 	-  |  -   |     |
| RTOS| FreeRTOS |	FreeRTOS, Rhino	| -    |   -  |     |	
| NN	| Support	| Support |	-  | Support   |    |	
| DSP	| Support	| Support	| -	|  Support  |    |   
| Coding Rule | MISRA | MISRA, TUeV61508 |	 |  MISRA  |    |	
| Validation | Support |	Support |	 - |  Support  |    |	
| License |	Apache 2.0 |	Apache 2.0 |	- | Apache 2.0   |    |	
| Software pack |	Support	| Support |	-	|   Support |    |
| Numbered Requirements	(Y/N/Maybe)|     |    |    |    |    |			
| T1 |    |    |    |    |    |				
| T2 |    |    |    |    |    |			
| T3 |    |    |    |    |    |			
| T4 |    |    |    |    |    |				
| T5 |    |    |    |    |    |				
| T6 |    |    |    |    |    |			
| T7 |    |    |    |    |    |				
| T8 |    |    |    |    |    |				
| T9 |    |    |    |    |    |				
| IA1 |   |    |    |    |    |				
| S1 |    |    |    |    |    |				
| S2 |    |    |    |    |    |			
| S3 |    |    |    |    |    |			
| S4 |    |    |    |    |    |				
| IM1 |   |    |    |    |    |				
| IM2 |   |    |    |    |    |				
| IM3 |   |    |    |    |    |				
| IM4 |   |    |    |    |    |			






