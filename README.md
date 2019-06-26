# openOcd-Commands
## STM32
#### Set RDP to Level 0:  
    openocd -f interface/stlink.cfg -f target/stm32f0x.cfg -c init -c "halt" -c "stm32f1x unlock 0" -c "reset" -c "exit"
#### Program and set RDP to Level1:
    openocd -f interface/stlink.cfg -f target/stm32f0x.cfg -c init -c "halt" -c "flash write_image erase F:/stm32.hex" -c "stm32f1x lock 0" -c "reset" -c "exit"
  
