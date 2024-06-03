# EVAL_PMG1_S3_DUALDRP BSP

## Overview

The EVAL_PMG1_S3_DUALDRP Prototyping Kit is a development platform that enables the design and development of  EZ-PD™ PMG1-S3 (CYPM1321-97BZXI)-based embedded USB-C Power Delivery (PD) products. These products are capable of  providing and consuming high voltage power to/from two USB PD ports, and also require a microcontroller with  CAPSENSE™ capability to implement various applications.

![](docs/html/board.png)

To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Kit Features:

* Supports USB PD DRP operation on both the USB-C ports.
* Supports SPR (Standard Power Range) in source mode and can provide upto 100W (20V@3A) on both ports.
* Supports EPR (Extended Power Range) in sink mode up to 140W (28V@5A) power on both ports.
* Support for two self-capacitance based CAPSENSE™ buttons and one 5-segment slider.
* Kit can be powered from either an external DC adapter (24V) or from USB-C Bus power. 
* KitProg3 based programming and debug interface.
* Access to the pins of PMG1-S3 silicon (CYPM1321-97BZXIT) in hardware and support for BSP, PDL and         Middleware in Modus Toolbox.
* The kit can provide two fixed voltage supplies - 5V/2.5A and 3.3V/400mA to enable users to power external peripherals/sensors if required. 
* The kit provides an option to bypass the onboard PD regulator and connect an external PD regulator for 140W (28V@5A) source operation.

### Kit Contents:

* EZ-PD™ CYPM1321-97BZXIT based board
* Quick Start Guide

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the EVAL_PMG1_S3_DUALDRP.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.

### Clock Configuration

| Clock    | Source    | Output Frequency |
|----------|-----------|------------------|
| CLK_HF   | CLK_IMO   | 48 MHz           |

### Power Configuration

* System Idle Power Mode: Deep Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The EVAL_PMG1_S3_DUALDRP Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [EVAL_PMG1_S3_DUALDRP BSP API Reference Manual][api]
* [EVAL_PMG1_S3_DUALDRP Documentation](https://www.infineon.com/EVAL_PMG1_S3_DUALDRP)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_EVAL_PMG1_S3_DUALDRP/html/modules.html
[settings]: https://infineon.github.io/TARGET_EVAL_PMG1_S3_DUALDRP/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2024.