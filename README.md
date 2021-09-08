# OpenHW-HAL
markdown docs
Known market/project requirements at PC gate
Significantly reduce cost in SoC driver development, by defining an approach to enable driver reuse according to an accepted framework;
Make consistent the upper layer software across different SoC. This requires standard HAL APIs to isolate hardware and software resources in such a manner that makes it easy to migrate software across platforms.
Category	Req #	Requirement
Technical Reqmtns	T-1	HAL MUST support API for core features
T-2	HAL MUST support API for on-chip peripheral features
T-3	HAL MUST support both RTOS and bare-metal scenarios
T-4	HAL MUST be able to support bare metal libc
T-5	HAL MUST be able to be extended to support all CORE-V cores for the purpose of RTOS (not Linux) support
T-6	HAL MUST support a description of the chip using a standardized syntax
T-7	HAL SHOULD define a configuration file that can indicate to the IDE low level chip parameters such as memory space and allow it to display/read/write the registers of peripherals
T-8	HAL MAY be able to be extended to support the CORE-V X Coprocessor Interface (CV-X-IF)
T-9	HAL MAY be able to be extended to support the CV-VEC coprocessor
Industry Adoption Rqmtns	IA-1	HAL SHOULD be adopted/implemented for other RISC-V devices
Specification Rqmtns	S-1	HAL Specification License for CORE-V MUST be open-source or freely licensed		T-2
S-2	Proprietary extensions to the HAL Specification and Implementation, such as for custom ISA extensions or proprietary chip, MUST be supportable/allowable under open-source license
S-3	HAL Specification, user documentation, and system implementation documentation for CORE-V HAL MUST be available in English
S-4	HAL Specification MUST be published and managed by an industry open source or standards body, such as OpenHW, RISC-V International, or FOSSi
Implementation Rqmtns	IM-1	A complete open source reference implementation of the HAL for CORE-V MUST be a project deliverable
IM-2	FreeRTOS SHOULD be supported in the open source reference implementation of HAL for CORE-V
IM-3	Newlib SHOULD be supported in the open source reference implementation of HAL for CORE-V
IM-3	The HAL reference implementation for CORE-V SHOULD be published by the body publishing the Specification (previous page)
