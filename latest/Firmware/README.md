## Transponder firmware

This is a vanilla Eclipse CDT project. Import it into your workspace and (assuming you have ARM cross compiler installed) it should be straightforward.

The application is mainly interrupt driven, with a single event queue being dispatched by an RTOS task. 

### Key updates

 - Starting with board 6.1 you have the option of using FreeRTOS 10, but not by default
 - DFU can be achieved by jumping directly into the ROM bootloader, so there is no need for hardware to manipulate the BOOT0 pin
 - The TX_DISABLE signal is now supported
 - Board 9.3 adds 3 "status" (LED driving) signals for GPS, RX and TX

 
